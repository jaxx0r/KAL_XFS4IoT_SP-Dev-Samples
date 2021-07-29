# Based on Red Hat Universal Base Image for .Net 5.0. Image details at: https://catalog.redhat.com/software/containers/ubi8/dotnet-50/
FROM registry.access.redhat.com/ubi8/dotnet-50:latest

MAINTAINER Daniel Schaefer <daniel.schaefer@redhat.com>

# Here should be meaningful labels. At least "name", "vendor", "version", "release", "summary" and "description" are required for Red Hat image certication.
LABEL name="XFS4IoT_SP-Dev-Samples-Host" \
      vendor="KAL & Red Hat" \
      version="0.0.2-alpha.2" \
      release="SP-Dev 0.0.2" \
      summary="XFS4IoT server image with simulated card reader" \
      description="XFS4IoT server image with simulated card reader based on KAL XFS4IoT SP-Dev Framework samples."

USER root

# Update for latest security patches (certification recommendation)
RUN yum -y update-minimal --security --sec-severity=Important --sec-severity=Critical

# Include all license files  (certification requirement)
COPY licenses /licenses

# Include application
COPY app /opt/app-root/app

# Exposed Ports
EXPOSE 5846-5856
EXPOSE 80
EXPOSE 443

# Good practice not to run as root
USER 1001

WORKDIR /opt/app-root/app

CMD ["dotnet", "XFS4IoT.SP.ServerHostSample.dll", "$@"]
