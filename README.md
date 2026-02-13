# Lychee Helm Charts

Official Helm charts repository for Lychee projects.

## Usage

Add the Helm repository:

```bash
helm repo add lychee https://juanjitech.github.io/lychee-charts/charts
helm repo update
```

Search available charts:

```bash
helm search repo lychee
```

Install a chart:

```bash
# Install lychee-moments-plus
helm install my-release lychee/lychee-moments-plus

# Install with custom values
helm install my-release lychee/lychee-moments-plus -f values.yaml

# Install specific version
helm install my-release lychee/lychee-moments-plus --version 0.1.0
```

## Available Charts

- **lychee-moments-plus**: Lychee Moments Plus backend service - DDD-based social moments platform

## Chart Versions

Visit the [Releases](https://github.com/juanjiTech/lychee-charts/releases) page to see all available chart versions.

## Development

This repository is automatically updated by CI/CD pipelines from source repositories. Charts are packaged and published when version tags are pushed.

## License

Charts in this repository follow the licenses of their respective source projects.