# Containerization

Instructions for building and running SP-Dev Sample Application in container.


## Build instructions for Dockerfile:
podman build -t xfs4iot_sp-dev-samples-host:latest --layers=false .

## Run instructions:
podman run -d --network=host --name xfs4iot_sp-dev-sample xfs4iot_sp-dev-samples-host:latest

## Red Hat Universal Base Image
The container image is build with Red Hat's Universal Base Image. More information on UBI is specified at:
https://developers.redhat.com/products/rhel/ubi

