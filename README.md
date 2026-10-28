# Docker & Container Security — CA-2

| Field | Value |
|---|---|
| Name | Akshat Srivastava |
| REGNO | 202401100200032 |
| PORT | 8032 |
| Docker Hub user | akshonite |
| Docker Hub repo | https://hub.docker.com/r/akshonite/fest-backend |

## AI tools used

- Claude Code: wrote the starter files, Dockerfile, compose.yaml and README, and explained Trivy findings. All commands for the screenshots were run by me in my own terminal.

## Digest of 1.0.0 as pushed to Docker Hub

`sha256:a256e5a8c6b386d6123a50c4f9bd99575ad6352d674cbe56fd5c70721031f4e5`

## Before and after (Trivy)

| Image | Base | CRITICAL | HIGH | Size |
|---|---|---|---|---|
| fest-backend:0.1 | python:3.9 | 234 | 2249 | 1.6 GB |
| fest-backend:0.2 | python:3.12-slim, non-root, upgraded libraries | 0 | 44 | 283 MB |

`trivy image --severity CRITICAL --ignore-unfixed --exit-code 1 fest-backend:0.2` exits with code 0.

## Steps not completed

- None.
