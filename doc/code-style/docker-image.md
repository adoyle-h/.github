---
parent: Code Styles
---
# Docker Image Style

## Use only well maintained images FROM a trusted registry

We trust "Docker" and "ourselves". As a consequence, you can pull images from `hub.docker.com`, `docker.io` or `quay.io`.

## Image names and versions

1. Image names should not contain version info "in themselves".

    Example: There is no `mysql4:1.0` or `ubuntu14:0.4` but only `mysql:4.x.x` and `ubuntu:14.0.4`

2. you **MUST** use `latest` only with the most recent **STABLE** version (not necessarily the latest being build).

    Example: `php:latest`

3. container:major - this is for a specific version/featureset.

    Example: `php:4`, `php:5`

4. container:major.minor - this is for a specific (compatible) version with a compatible featureset

    Example: `mysql:5.6`, `mysql:5.7`

5. container:major.minor.patch - this is/must be EXACTLY THE current container. If anybody needs THIS container he has to use this tag.

    Example: `mysql:5.6.28`, `mysql:5.7.10`

## Adding information to version

Examples:

- `php:5.6.17-cli` It is IDENTICAL to php:5.6.17 and so the default
- `php:5.6.17-apache` It is an php container installation that provides the apache webserver WITH php
- `php:5.6.17-fpm` It is an php container that can be used with nginx (FPM=FastCGI Process Manager)

## Building Multi-Architecture Images

You **SHOULD** build images for `amd64` and `arm64` architectures at least.

Follows this [article](https://www.docker.com/blog/how-to-rapidly-build-multi-architecture-images-with-buildx/).
