FROM python:3.6.8-alpine3.8

RUN apk add --no-cache --repository http://dl-3.alpinelinux.org/alpine/edge/testing/ \
  py3-lxml \
  py3-pycryptodome \
  py3-requests \
  py3-attrs

ENV PYTHONPATH $PYTHONPATH:/usr/lib/python3.6/site-packages

# install python dependencies manually for much smaller image
RUN pip3 install future mini-amf ConfigArgParse==0.13.0 && \
  rm -rf /root/.cache/pip

RUN pip3 install --no-deps yle-dl

ENTRYPOINT yle-dl
