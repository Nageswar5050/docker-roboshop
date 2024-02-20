FROM python:3.6.15-alpine3.15
WORKDIR /opt/server
EXPOSE 8080
ENV AMQP_USER=roboshop \
    AMQP_PASS=roboshop123
COPY *.py .
COPY payment.ini .
COPY requirements.txt .
RUN apk add python3-dev build-base linux-headers pcre-dev
RUN pip3.6 install -r requirements.txt
CMD ["uwsgi", "--ini", "payment.ini"]