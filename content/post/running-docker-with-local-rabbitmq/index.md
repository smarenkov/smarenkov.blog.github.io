---
title: Running Docker Compose with Local RabbitMQ
date: 2024-10-19
description: A quick guide to running Docker Compose with your local RabbitMQ setup.
tags: 
    - Docker
    - RabbitMQ
categories:
    - Docker
    - RabbitMQ
---

If you want to run Docker Compose and use your local RabbitMQ instance, you'll need to modify the RabbitMQ configuration to specify the IP address.

1. Open the RabbitMQ configuration file `rabbitmq.conf`. If it doesn't exist, create it in the RabbitMQ directory `/etc/rabbitmq/`.

2. Add the following line to specify the IP address:

```
listeners.tcp.default = [your ip address]:5672
```

3. Restart RabbitMQ