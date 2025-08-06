![Version: 0.0.5](https://img.shields.io/badge/Version-0.0.5-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 0.0.1](https://img.shields.io/badge/AppVersion-0.0.1-informational?style=flat-square)

A flexible Helm chart that allows you to define and render any Kubernetes resources directly in your values.yaml file.

This chart provides a simple way to deploy custom resources without creating traditional Helm templates.

## Features

- Deploy any Kubernetes resources by defining them in values.yaml
- Full Helm templating support within your resource definitions

## Installation

```bash
helm install my-release oci://ghcr.io/hiddenmarten/charts/raw
```

## Usage

Define your Kubernetes resources in the `templates` array within your values.yaml file.
Each item in the array should be a complete Kubernetes resource definition.

## Examples

See the `examples/` directory for more usage examples:

  - `basic.yaml` - Simple ConfigMap and Service deployment

## License

This project is licensed under the terms specified in the LICENSE file.

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| templates | list | `[]` |  |
