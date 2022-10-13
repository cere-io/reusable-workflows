# Changelog

All notable changes will be documented in this file.

## [1.0.0] - 2022-10-08

### build-and-push-docker.yaml

- Build docker image and push it to ecr or public registry

### build-and-upload-static.yaml

- Build static content (can be skipped), upload it to cloudfront and run invalidation

### deploy-with-helm.yaml

- Download docker image and deploy it via helm to k8s

### tests-jdk-gradle.yaml

- Run tests via gradle
