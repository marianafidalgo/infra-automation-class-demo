## Check if Kubernetes is running

```bash
kubectl version
```

## Get namespaces

```bash
kubectl get namespaces
```

## Switch to a namespace

```bash
kubectl config set-context --current --namespace=<namespace-name>
```

## Get pods

```bash
kubectl get pods
```

## Get deployments

```bash
kubectl get deployments
```

## Get services

```bash
kubectl get services
```

## Describe a service

```bash
kubectl describe service <service-name>
```

## View logs of a pod

```bash
kubectl logs <pod-name>
```
