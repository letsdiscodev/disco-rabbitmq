# RabbitMQ on Disco

Fork this repository. Create a projet on Disco, and set the environment variables while creating the project (not after).

## Environment Variables

### RABBITMQ_NODENAME

Give it a unique name that represents the project you're working on. E.g. `myproject1`. This is used internally by RabbitMQ to store data in a consistent directory that won't change over time.

### RABBITMQ_DEFAULT_USER

Generate a username. E.g. `VBDe42Dfhse66J3b`.

### RABBITMQ_DEFAULT_PASS

Generate a password. E.g. `TjyyCbkcZg5jqgg3`.


### RABBITMQ_DEFAULT_VHOST

Generate a vhost. E.g. `CAW8kHVBUPdNszmU`.


## Management Interface

You can connect to the management interface by going to the domain name you set while creating the project and entering the username and password you set as environment variables.

## Sending/Receiving Messages

The connection string uses the parameters above and the project name.

```
amqp://{RABBITMQ_DEFAULT_USER}:{RABBITMQ_DEFAULT_PASS}@{PROJECT_NAME}-web:5672/{RABBITMQ_DEFAULT_VHOST}
```

E.g. using the variables above and the project name `rabbitmq-example`:

```
amqp://VBDe42Dfhse66J3b:TjyyCbkcZg5jqgg3@rabbitmq-example-web:5672/CAW8kHVBUPdNszmU
```