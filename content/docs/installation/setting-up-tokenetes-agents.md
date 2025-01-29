---
Title: "Setting Up Tokenetes Agents"
weight: 3
toc: true
---

[Tokenetes Agents](https://github.com/tokenetes/tokenetes-agent) are sidecar container agents that verify TraTs in microservices.

Tokenetes agents are injected into microservices pods to verify TraTs. To integrate Tokenetes agents into microservices, follow the instructions from [Tokenetes Agent's readme](https://github.com/tokenetes/tokenetes-agent/blob/main/README.md).

After successfully integrating Tokenetes Agents, you should be able to see running Tokenetes agent sidecars alongside your application microservices containers. For example, below are the running Order service pods from the [Tokenetes example application's](https://github.com/tokenetes/example-application) dev environment.

```bash
kubectl get pod -n alpha-stocks-dev | grep order
```

Output:

```bash
order-556d94cfdc-gs9ww       2/2     Running   0          63m
```

Order service has two containers. The second container is the Tokenetes agent sidecar container.

Next, proceed to writing Tokenetes Kubernetes resources for specifying how to generate and verify TraTs for your application APIs: [Generating and Verifying TraTs](/docs/generating-and-verifying-trats).

<br>

For a practical example of installing Tokenetes on a microservice application, refer to the [Tokenetes example application](https://github.com/tokenetes/example-application).