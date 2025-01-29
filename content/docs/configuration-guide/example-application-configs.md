---
title: "Example Application Configurations"
weight: 4
toc: true
---

Below are the Tokenetes Kubernetes resources for the [Tokenetes example application](https://github.com/tokenetes/example-application). These examples can serve as references when writing the resources for your microservices application.

### TraTs

The Tokenetes example application has four external APIs; consequently, there are four TraT resources.

`stock-details-api-trat.yaml:`

```yaml
apiVersion: tokenetes.io/v1alpha1
kind: TraT
metadata:
  name: stock-details-api-trat
  namespace: alpha-stocks-dev
spec:
  path: "/api/stocks/details/{#stockId}"
  method: "GET"
  purp: stock-details
  azdMapping:
    stockId:
      required: true
      value: "${stockId}"
  services:
    - name: stocks
  accessEvaluation:
    subject:
      id: "${subject_token.email}"
    action:
      name: "stock-details"
    resource:
      stockId: "${stockId}"
```

`stock-holdings-api-trat.yaml:`

```yaml
apiVersion: tokenetes.io/v1alpha1
kind: TraT
metadata:
  name: stock-holdings-api-trat
  namespace: alpha-stocks-dev
spec:
  path: "/api/stocks/holdings"
  method: "GET"
  purp: stock-holdings
  services:
    - name: stocks
  accessEvaluation:
    subject:
      id: "${subject_token.email}"
    action:
      name: "stock-holdings"
```

`stock-search-api-trat.yaml:`

```yaml
apiVersion: tokenetes.io/v1alpha1
kind: TraT
metadata:
  name: stock-search-api-trat
  namespace: alpha-stocks-dev
spec:
  path: "/api/stocks/search"
  method: "GET"
  purp: stock-search
  azdMapping:
    query:
      required: true
      value: "${queryParameters.query}"
  services:
    - name: stocks
  accessEvaluation:
    subject:
      id: "${subject_token.email}"
    action:
      name: "stock-search"
    resource:
      query: "${queryParameters.query}"
```

`stock-trade-api-trat.yaml:`

```yaml
apiVersion: tokenetes.io/v1alpha1
kind: TraT
metadata:
  name: stock-trade-api-trat
  namespace: alpha-stocks-dev
spec:
  path: "/api/order"
  method: "POST"
  purp: stock-trade
  azdMapping:
    stockId:
      required: true
      value: "${body.stockId}"
    action:
      required: true
      value: "${body.orderType}"
    quantity:
      required: true
      value: "${body.quantity}"
  services:
    - name: order
    - name: stocks
      path: "/internal/stocks"
  accessEvaluation:
    subject:
      id: "${subject_token.email}"
    action:
      name: "${body.orderType}"
    resource:
      stockId: "${body.stockId}"
```

## TraTExclusion

There are two services, the stocks and order service, that verify TraTs in the example application; consequently, there are two TraTExclusion resources.

`order-service-tratexcl.yaml`

```yaml
apiVersion: tokenetes.io/v1alpha1
kind: TraTExclusion
metadata:
  name: order-service-tratexcl
  namespace: alpha-stocks-dev
spec:
  service: order
  endpoints:
    - path: "/health"
      method: "GET"
```

`stocks-service-tratexcl.yaml:`

```yaml
apiVersion: tokenetes.io/v1alpha1
kind: TraTExclusion
metadata:
  name: stocks-service-tratexcl
  namespace: alpha-stocks-dev
spec:
  service: stocks
  endpoints:
    - path: "/health"
      method: "GET"
```

### TokenetesConfig

`tokenetescfg.yaml:`

```yaml
apiVersion: tokenetes.io/v1alpha1
kind: TokenetesConfig
metadata:
  name: alpha-stocks-tokenetescfg
  namespace: alpha-stocks-dev
spec:
  token:
    issuer: "https://alphastocks.com/tokenetes"
    audience: "https://alphastocks.com/"
    lifeTime: "15s"
  subjectTokens:
    OIDC:
      clientId: alpha-stocks-client
      providerURL: http://dex:5556/dex
      subjectField: email
    selfSigned:
      validation: false
      jwksEndpoint: "http://alphastocks.com/oidcprovider/.well-known/jwks.json"
  accessEvaluationAPI:
    enableAccessEvaluation: false
    endpoint: "https://alphastocks.authzen.com/access/v1/evaluation"
    authentication:
      method: "Bearer"
      token:
        value: "${AUTHORIZATION_API_BEARER_TOKEN}"
  tokenGenerationAuthorizedServiceIds:
      - "spiffe://dev.alphastocks.com/gateway"
```
