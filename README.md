# Apache APISIX Grafana Dashboard

Grafana dashboard for monitoring **Apache APISIX API Gateway** using Prometheus metrics.

## Features

- HTTP request monitoring
- HTTP status code monitoring
- Request latency
- Bandwidth / traffic monitoring
- Active connections
- APISIX instance-level metrics
- Service and route-level monitoring
- Consumer-level metrics
- Node-level metrics
- Prometheus-based monitoring
- Namespace-based filtering

## Environment Support

The dashboard supports multiple APISIX environments/clusters using Kubernetes namespace filtering:

- `apisix-pg`
- `apisix-pg-chandigarh`

A single Prometheus instance can be used to collect metrics from both APISIX deployments while keeping the dashboards separated using the `kubernetes_namespace` label.

## Requirements

- Grafana
- Prometheus
- Apache APISIX with Prometheus plugin enabled
- Kubernetes

## APISIX Prometheus Configuration

APISIX exposes Prometheus metrics through:

```text
/apisix/prometheus/metrics
