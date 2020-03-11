# AstroKube Helm Charts

Applications provided by [AstroKube](https://astrokube.com) for Kubernetes using [Helm](https://github.com/helm/helm) and packaged as Charts.

## Requirements

You need to have Helm installed. Refer to the [Helm installation guide](https://github.com/helm/helm#install).

## Add the repository

Add this repository to your Helm installation:

```bash
$ helm repo add astrokube https://astrokube.github.io/helm-charts
```

## Search applications

List all available application with AstroKube repository:

```bash
$ helm search repo astrokube
```

## Install application

Install an application:

```bash
$ helm install my-release astrokube/<chart>
```

Example installing _factorio_ chart:

```bash
$ helm install factorio astrokube/factorio
```
