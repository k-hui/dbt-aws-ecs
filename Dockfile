FROM python:3.9.15-slim-bullseye

# System setup
RUN apt-get update \
  && apt-get dist-upgrade -y \
  && apt-get install -y --no-install-recommends \
    git \
    ssh-client \
    software-properties-common \
    make \
    build-essential \
    ca-certificates \
    libpq-dev \
  && apt-get clean \
  && rm -rf \
    /var/lib/apt/lists/* \
    /tmp/* \
    /var/tmp/*

# Env vars
ENV PYTHONIOENCODING=utf-8
ENV LANG=C.UTF-8

WORKDIR /app

COPY main.py /app
COPY example /app/example

COPY requirements.txt /app
RUN pip install --no-cache-dir -r requirements.txt

CMD python -m uvicorn main:app --host 0.0.0.0 --port 80 --workers 1