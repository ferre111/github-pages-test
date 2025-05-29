FROM ubuntu:24.04
RUN apt-get update && \
    DEBIAN_FRONTEND=noninteractive \
    apt-get -y install make python3 python3-venv
COPY ./../requirements.txt .
RUN python3 -m venv /venv
RUN . /venv/bin/activate && \
    pip install --upgrade pip && \
    pip install -r requirements.txt
ENV VIRTUAL_ENV=/venv \
    PATH="/venv/bin:${PATH}"
