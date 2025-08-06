# Helm Chart Raw

A flexible Helm chart that allows you to define and render any Kubernetes resources directly in your values.yaml file.

## Purpose

This chart has been created to be a workaround for this Terraform issue:
  - https://github.com/hashicorp/terraform-provider-kubernetes/issues/1775

Although, I assume there are plenty of other cases where it could be suitable.

## Contribution guide

Thank you for considering contributing to the Helm Chart Raw project! This guide will help you get started with the development process.

### Prerequisites

- [Helm](https://helm.sh/docs/intro/install/) (v3.x)
- [pre-commit](https://pre-commit.com/#install)

### Development workflow

1. Fork the repository and clone your fork
2. Install pre-commit hooks:
   ```bash
   pre-commit install
   ```
3. Make your changes
4. Run pre-commit checks:
   ```bash
   pre-commit run --all-files
   ```
5. Submit a pull request

### Versioning

This project follows [Semantic Versioning](https://semver.org/). When making changes:

1. Update the `version` field in `raw/Chart.yaml` according to:
   - PATCH (0.0.x): Bug fixes and minor changes that don't affect functionality
   - MINOR (0.x.0): New features in a backward-compatible manner
   - MAJOR (x.0.0): Incompatible API changes

### Release process

Releases are automated through GitHub Actions:

1. Changes merged to the `main` branch can be released by triggering the "Release Helm Chart" workflow
2. The workflow packages the chart and publishes it to:
   - GitHub Container Registry (OCI): `oci://ghcr.io/hiddenmarten/charts/raw`
   - GitHub Releases

### Documentation

When making changes, please update the relevant documentation:

- Chart README (`raw/README.md`) is automatically generated using [helm-docs](https://github.com/norwoodj/helm-docs)
- Update examples in the `raw/examples/` directory for new features
