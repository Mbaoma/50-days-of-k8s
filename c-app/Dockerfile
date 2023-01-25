FROM ubuntu:18.04

WORKDIR /opt/facebooc

COPY . /opt/facebooc

RUN apt-get -y update
RUN apt-get -y upgrade
RUN apt-get install -y build-essential make sqlite3 libsqlite3-dev

EXPOSE 16000

RUN make all

CMD ["bin/facebooc"]