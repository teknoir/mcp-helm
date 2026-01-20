# MCP Helm Chart

This chart deploys Model Context Protocol applications to a Kubernetes cluster.

> The implementation of the Helm chart is right now the bare minimum to get it to work.
> The purpose of the chart is not to be infinitely configurable, but to provide a limited set of configuration options that make sense for the Teknoir platform.

# Helm usage

## Usage in Teknoir platform
Use the HelmChart to deploy the Model Context Protocol applications to a Namespace.

```yaml
---
apiVersion: helm.cattle.io/v1
kind: HelmChart
metadata:
  name: mcp
  namespace: demonstrations # or any other namespace
spec:
  repo: https://teknoir.github.io/mcp-helm
  chart: mcp
  targetNamespace: demonstrations # or any other namespace
  valuesContent: |-
    # Example for minimal configuration
    
```

## Adding the repository

```bash
helm repo add teknoir-mcp https://teknoir.github.io/mcp-helm/
```

## Installing the chart

```bash
helm install teknoir-mcp teknoir-mcp/mcp -f values.yaml
```
