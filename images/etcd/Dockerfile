FROM ubuntu:latest
MAINTAINER Miclefeng <miclefengzss@gmail.com>

RUN apt-get update && apt-get install -y curl 
WORKDIR /usr/local/src/
RUN curl -L  https://github.com/coreos/etcd/releases/download/v3.2.10/etcd-v3.2.10-linux-amd64.tar.gz -o etcd-v3.2.10.tar.gz \
        && tar -zxvf etcd-v3.2.10.tar.gz \
        && ln -s /usr/local/src/etcd-v3.2.10-linux-amd64 /usr/local/etcd
WORKDIR /usr/local/

ENTRYPOINT ["/bin/bash", "-c", "/usr/local/etcd/etcd"]
