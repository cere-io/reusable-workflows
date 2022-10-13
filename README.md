# Reusable workflows

There are four types of reusable workflows:

1) [Build docker image using Dockerfile and push to docker registry](.github/workflows/build-and-push-docker.yaml)

2) [Build static content, upload to s3 and run cloudfront invalidation](.github/workflows/build-and-upload-static.yaml)

3) [Deploy docker image from registry to k8s via helm](.github/workflows/deploy-with-helm.yaml)

4) [Run jdk tests via gradle](.github/workflows/tests-jdk-gradle.yaml)

Versioning template: Major.Minor.Patch (1.0.0)

After implementing new functional needed to push new tag in case of changes size:

1) Small change like type change parameter ⇒ Patch (1.0.0 ⇒ 1.0.1)

2) Small change like adding new action or new parameter ⇒ Minor (1.0.0 ⇒ 1.1.0)

3) Medium or big change like adding new reusable workflow or reworking current ⇒ Major (1.0.0 ⇒ 2.0.0)

## How to use

```
uses: Cere-IO/reusable-workflows/.github/workflows/build-and-push-docker.yaml@<version>
with:
  <variables>
secrets:
  <secrets> or just inherit
```

Variables you can find in "inputs" block

Secrets you can find in "secrets" block

Version you can choose follow [changelog](CHANGELOG.md)