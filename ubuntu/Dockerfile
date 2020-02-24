ARG BASE_CONTAINER=ubuntu:18.04
FROM $BASE_CONTAINER

LABEL maintainer="Singh Sukhjnder <ss.singh@hotmail.it>"

ENV DEBIAN_FRONTEND noninteractive

ENV TZ=UTC
ENV AUTOVACUUM=on
ENV UPDATES=disabled
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone

# Install dependencies
RUN apt-get update \
  && apt-get install build-essential wget curl git -y \
  && apt-get update \
  && apt-get install -y apt-transport-https ca-certificates

CMD ["/bin/bash"]