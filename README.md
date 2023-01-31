# chronocollector-trace-chart

The helm chart installs Chronosphere Collector with Otel Tracing capability in kubernetes cluster.

## Prerequisites

- Kubernetes 1.23+
- Helm 3.9+

## Installing the Chart

To install the chart with the release name oteldemo, run the following command:

```console

export CHRONOSPHERE_API_TOKEN=<token>
export CHRONOSPHERE_ORG_NAME=<name>

helm install oteldemo ./chronocollector-trace-chart --set orgName=$CHRONOSPHERE_ORG_NAME --set apiToken=$CHRONOSPHERE_API_TOKEN -n [namespace]
```
The exposed service endpoint is [namespace]-chronocollector-tracing, which is the target endpoint for oTel collector or oTel client.
