FROM python:3-alpine
MAINTAINER William Stewart <zoidbergwill+docker@gmail.com>

VOLUME ~/.cache

RUN mkdir -p /usr/src/app
WORKDIR /usr/src/app

COPY requirements.txt /usr/src/app/

RUN pip install -r requirements.txt

COPY . /usr/src/app

EXPOSE 8080
CMD ["gunicorn" , "-b", "0.0.0.0:8000", "-w", "3",  "main:app"]
