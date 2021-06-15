# Containerization

Instructions for building and running SP-Dev Sample Application in container:

## Build instructions for Dockerfile:
podman build -t XFS4IoT_SP-Dev-Samples-Host:latest --layers=false .

## Run instructions:
podman run -d -p 8088:8088 xfs4iot_sp-dev-samples-host:latest
