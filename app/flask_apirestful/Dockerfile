FROM python:3.6-alpine

RUN apk update
RUN apk add --no-cache build-base 
RUN apk add --no-cache postgresql-dev

WORKDIR /usr/src/app

COPY entrypoint.sh /root
COPY requirements.txt /root 

RUN pip install --no-cache-dir -r /root/requirements.txt

EXPOSE 5000
ENTRYPOINT ["/root/entrypoint.sh"]
