FROM ubuntu:16.04

MAINTAINER warg

RUN apt-get update
RUN apt-get install -y python3 python3-pip
RUN pip3 install --upgrade pip
RUN pip3 install tornado==4.4.3

RUN mkdir /usr/app
COPY index.py /usr/app/index.py

EXPOSE 8888
VOLUME ["/usr/app"]

ENTRYPOINT if [ -z "$ENTRY" ]; then python3 /usr/app/index.py; else python3 /usr/app/$ENTRY; fi