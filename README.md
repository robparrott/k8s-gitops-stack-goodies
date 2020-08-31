# Overview

Provides a set of kubernetes manifests that stand up a set of demos and other "goodies" using GitOps via ArgoCD.

See the base repositories for this GitOps example:

* For launching a cluster and boostrapping GitOps: https://github.com/parrottr/gitops-example
* For defining a GitOps-based distribution model: https://github.com/robparrott/k8s-gitops


Useful for testing deployments. settings, and learning.

Components:

* *podinfo* single pod demo
* istio's *bookinfo* app
* *petclinic* from Solo.io for the Gloo project
* *petstore* from Solo.io for the Gloo project

# Access

## Podinfo


Port-forward:

```
kubectl port-forward service/podinfo -n default 9898:9898
```

Then access:

* http://localhost:9898

See: https://github.com/stefanprodan/podinfo for more information.

## Bookinfo

Ssee the documentation here: https://istio.io/latest/docs/examples/bookinfo/ for more information.

Port-forward:

```
kubectl port-forward service/productpage -n default 9080:9080
```

Then access:

* http://localhost:9080/productpage

## Petclinic