# Helm Charts Repository

This repository contains Helm charts for applications used across. It provides a centralized location for deploying consistent, versioned applications to Kubernetes clusters.

## Overview

- **Repository URL**: https://nstarx.github.io/NstarX_helmcharts/
- **GitHub Repository**: https://github.com/nstarx/NstarX_helmcharts

## Using These Helm Charts

### 1. Add the Helm Repository

helm repo add nstarx-charts https://nstarx.github.io/NstarX_helmcharts/

### 2. Update Your Local Repository Cache

helm repo update

### 3. Search for Available Charts

helm search repo nstarx-charts


### 4. Install a Chart

#### Basic installation
helm install myapp nstarx-charts/sample-webapp --namespace my-namespace

#### Install with custom values
helm install my-release nstarx-charts/sample-webapp --set replicaCount=3 --namespace my-namespace

#### Install with a values file
helm install my-release nstarx-charts/sample-webapp -f my-values.yaml --namespace my-namespace

#### Install a specific version
helm install my-release nstarx-charts/sample-webapp --version 1.2.3 --namespace my-namespace

### 5. Managing Deployments

#### List all Helm releases in a namespace
helm list --namespace my-namespace

#### Get details about a release
helm status myapp --namespace my-namespace

#### Upgrade an existing release
helm upgrade myapp nstarx-charts/sample-webapp --namespace my-namespace

#### Uninstall a release
helm uninstall myapp --namespace my-namespace

#### Roll back to a previous release version
helm rollback myapp 1 --namespace my-namespace
