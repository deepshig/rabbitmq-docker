# basic python image
FROM python:3.7

# install pika to access rabbitmq
RUN pip install pika

# Without this setting, Python never prints anything out.
ENV PYTHONUNBUFFERED=1

# declare the source directory
WORKDIR /usr/src/app/consumer

# copy the file
COPY consumer.py .

# start command
CMD [ "python", "consumer.py" ]
