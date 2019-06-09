# Author: Air
# Practice version 1.0
# Time: 2019.06.08

FROM debian:latest

ENV KMS_BIN_URL https://github.com/Wind4/vlmcsd/releases/download/svn1112/binaries.tar.gz

ENV BIN_NAME=binaries.tar.gz

WORKDIR /kms

RUN apt-get -y update && apt-get install -y \
    wget \
    && mkdir /kms/temp \
    && wget ${KMS_BIN_URL} \
    && tar -axf ${BIN_NAME} -C /kms/temp \
    && mv /kms/temp/binaries/Linux/intel/static/* /kms \
    && apt-get -y remove wget \ 
    && rm -rf /var/lib/apt/lists/* \ 
    && rm -rf /kms/temp

EXPOSE 1688

CMD ["./vlmcsdmulti-x64-musl-static", "vlmcsd", "-D"]
