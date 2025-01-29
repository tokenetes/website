---
Title: "Installing Tconfigd"
weight: 1
toc: true
---

[Tconfigd](https://github.com/tokenetes/tconfigd) is a central daemon that manages Tokenetes configurations. To get started with Tokenetes, first install Tconfigd following the instructions from [Tconfigd's installation readme](https://github.com/tokenetes/tconfigd/tree/main/installation).

After successfully installing Tconfigd, you should be able to see a running Tconfigd pod in the tokenetes-system namespace.

```bash
kubectl get pod -n tokenetes-system
```

Output:

```bash
NAME                        READY   STATUS    RESTARTS   AGE
tconfigd-85c5697c9b-4lx4s   1/1     Running   0          88s
```

Next, proceed to [deploy Tokenetes service](/docs/installation/deploying-tokenetes), an open source [Transaction Tokens (TraTs)](/docs/transaction-token) Service.
