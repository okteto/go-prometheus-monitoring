# Develop and Monitor your Go service with Okteto and Prometheus

This example shows how to use Okteto to develop a Go Service directly in Kubernetes, and then use Prometheus to monitor it.

## Deploy Prometheus

The `prometheus.yaml` file contains the manifests needed to deploy an instance of Prometheus with a Service. It's already configured to read the metrics from the `hello-world` service.

```
kubectl apply -f prometheus.yaml
```

## Deploy the Hello-World service

The `prometheus.yaml` file contains the manifests needed to deploy an instance of a simple `hello-world` service. The service has to endpoints:

- `/`: returns a string message
- `/metrics`: exposes golang and application metrics 

The `prometheus.yaml` file contains the manifests needed to deploy an instance of Prometheus with a Service. It's already configured to read the metrics from the `hello-world` service.

```
kubectl apply -f hello-world.yaml
```

```
kubectl apply -f prometheus.yaml
```