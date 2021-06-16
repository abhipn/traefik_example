FROM python:3.7-slim

ARG DEBIAN_FRONTEND=noninteractive

ENV PYTHONUNBUFFERED=1

RUN pip3 install -U pip setuptools wheel && \
    pip3 install gunicorn fastapi uvloop httptools "uvicorn[standard]"

COPY . /app

ENV PORT=7777 

ENTRYPOINT /usr/local/bin/gunicorn -b 0.0.0.0:$PORT -w 1 -k uvicorn.workers.UvicornWorker app.main:app --chdir /app