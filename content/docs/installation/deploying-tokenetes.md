---
Title: "Deploying Tokenetes Service"
weight: 2
toc: true
---

[Tokenetes Service](https://github.com/tokenetes/tokenetes) is an open source [Transaction Tokens (TraTs)](/docs/transaction-token) Service, which is responsible for issuing TraTs. 

While [Tconfigd](/docs/installation/installing-tconfigd) runs in its own dedicated namespace and is cluster-specific, Tokenetes service operates in the application namespace and must be deployed seperately for different application environments or namespaces.

Please follow the instructions from [Tokenetes's deployment readme](https://github.com/tokenetes/tokenetes/tree/main/kubernetes) to deploy Tokenetes service.

After successfully deploying Tokenetes service, you should be able to see running Tokenetes service pods in the application namespace. For example, below is the running Tokenetes pods from the [Tokenetes example application's](https://github.com/tokenetes/example-application) dev environment. 

```bash
kubectl get pod -n alpha-stocks-dev | grep tokenetes
```

Output:

```bash
tokenetes-7b89b4f498-6kgd2   1/1     Running   0          22m
tokenetes-7b89b4f498-hgxct   1/1     Running   0          22m
tokenetes-7b89b4f498-tlrqd   1/1     Running   0          22m
```


Next, proceed to [Setting up Tokenetes agents](/docs/installation/setting-up-tokenetes-agents), a sidecar for verifying Transaction Tokens (TraTs).

