# UbiPoller Helm Chart

This Helm chart deploys UbiPoller to a Kubernetes cluster.

## Prerequisites

- Kubernetes 1.16+
- Helm 3.0+

## Installation

1. Create the namespace:
```bash
kubectl create namespace teamwald
kubectl create secret generic poller-secret \
  --from-literal=mqtt_password=your_mqtt_password \
  --from-literal=mqtt_username=your_mqtt_username \
  --from-literal=ubi_api_key=your_ubi_api_key \
  -n teamwald

helm install ubipoller ./ubipoller-chart
```