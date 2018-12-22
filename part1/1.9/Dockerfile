FROM alpine:3.8

RUN apk add --no-cache \
  python3 \
  nodejs \
  jq \
  postgresql-dev \
  libffi-dev \
  build-base \
  python3-dev \
  zsh

RUN pip3 install --upgrade pip

RUN pip3 install \
  requests \
  flask \
  pgcli \
  mycli \
  mypy \
  pip-tools

WORKDIR /root

CMD zsh
