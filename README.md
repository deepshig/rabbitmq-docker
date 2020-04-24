# RabbitMQ implementation in Python using Docker
This is a basic example to implement RabbitMQ in Python, and deploy using Docker.

It uses `pika` in python to connect to RabbitMQ.

Producer producer a 100 messages of text `Hello World` to the queue

Consumer consumes these messages, prints them and sleeps for 2 seconds before acking each of them.

We have used docker to run the program. Docker Compose has been used to spawn the multiple containers needed. We spawn one container each for RabbitMQ and producer, while 2 containers for consumer. This to exhibit parallel consumption from the same queue.

## Dependencies

* [Python 3.7](https://www.python.org/downloads/release/python-370/)
* [Docker](https://www.docker.com/)
* [RabbitMQ 3.8.3-rc.1](https://github.com/rabbitmq/rabbitmq-server/releases/tag/v3.8.3-rc.1)
* [Pika 1.1.0](https://github.com/pika/pika)

## Run the program

* To run `docker-compose up`

* To clean up `docker-compose down -v --rmi all --remove-orphans`

* We can run separate container by `docker-compose up producer` and so on

* While the containers are running, we can monitor the queue on the dashboard http://localhost:15672/ with [Username/Password] as [guest/guest]
