FROM python:3.6.15-alpine3.15
WORKDIR /opt/server
EXPOSE 8080
ENV AMQP_USER=roboshop \
    AMQP_PASS=roboshop123
COPY *.py .
COPY payment.ini .
COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt
#RUN pip3.6 install -r requirements.txt
CMD ["uwsgi", "--ini", "payment.ini"]