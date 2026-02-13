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
# Search stable versions
helm search repo lychee

# Search all versions (including pre-release versions like -test, -alpha, -beta)
helm search repo lychee --devel

# Show all available versions
helm search repo lychee --versions
```

Install a chart:

```bash
# Install latest stable version
helm install my-release lychee/lychee-moments-plus

# Install with custom values
helm install my-release lychee/lychee-moments-plus -f values.yaml

# Install specific version
helm install my-release lychee/lychee-moments-plus --version 1.0.0

# Install pre-release version
helm install my-release lychee/lychee-moments-plus --version 0.1.0-test --devel
```

View chart information:

```bash
# Show chart details
helm show chart lychee/lychee-moments-plus

# Show chart values
helm show values lychee/lychee-moments-plus

# Show all chart information
helm show all lychee/lychee-moments-plus
```

## Available Charts

- **lychee-moments-plus**: Lychee Moments Plus backend service - DDD-based social moments platform built with Go and CloudWeGo Hertz

## Chart Versions

All available chart versions are listed in the [index.yaml](https://juanjitech.github.io/lychee-charts/charts/index.yaml) file, or you can browse the [charts directory](https://github.com/juanjiTech/lychee-charts/tree/main/charts) on GitHub.

To see all versions:

```bash
helm search repo lychee --versions --devel
```

## Development

This repository is automatically updated by CI/CD pipelines from source repositories. When a version tag (e.g., `v1.0.0`) is pushed to a source repository, the workflow automatically:

1. Builds and pushes the Docker image
2. Packages the Helm chart
3. Publishes the chart to this repository
4. Updates the chart index

Charts are served via GitHub Pages at https://juanjitech.github.io/lychee-charts/charts/

## Contributing

This repository is managed automatically. To publish a new chart version:

1. Update the chart in your source repository
2. Push a version tag (e.g., `git tag v1.0.0 && git push origin v1.0.0`)
3. The CI/CD pipeline will automatically publish the chart here

## License

Charts in this repository follow the licenses of their respective source projects.