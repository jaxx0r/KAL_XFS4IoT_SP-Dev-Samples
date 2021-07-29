# Containerization

Instructions for building and running SP-Dev Sample Application in container.


## Build instructions for Dockerfile:
podman build -t cardreader-sample:latest --layers=false .

## Run instructions:
podman run -d --network=host --name cardreader1 cardreader-sample:latest

## Red Hat Universal Base Image
The container image is build with Red Hat's Universal Base Image. More information on UBI is specified at:
https://developers.redhat.com/products/rhel/ubi

