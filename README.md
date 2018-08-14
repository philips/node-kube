# node-kube

Quick presentation of a node.js workflow with Kubernetes.

[Slides](https://speakerdeck.com/philips/node-dot-js-workflow-with-minikube-and-skaffold)

## Pre-reqs

- [minikube](https://github.com/kubernetes/minikube#what-is-minikube)
- [skaffold](https://github.com/GoogleContainerTools/skaffold#installation)
- docker client (e.g. `brew install docker`)

## Simple Example

Download the repo

```
git clone https://github.com/philips/skaffold-nodejs-example
```

Manually build the container 

```
eval $(minikube docker-env)
docker build .
```

Start the workflow

```
skaffold dev
```

View in browser

```
minikube service node-app
```

Hack

```
vim index.js
```

## Fancy Vue.js Example

```
git clone https://github.com/philips/vue-starter
```
Start the workflow

```
skaffold dev
```

View in browser

```
minikube service vue-app
```

Hack

```
vim src/server/routes/CounterRoutes.ts
```
