FROM ubuntu:18.04

WORKDIR /user/src/app

COPY ./curler.sh .

RUN chmod +x curler.sh

RUN apt-get update; apt-get install -y curl; curl --version;

CMD ./curler.sh
