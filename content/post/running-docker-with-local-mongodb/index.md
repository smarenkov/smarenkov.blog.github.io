---
title: Running Docker Compose with Local MongoDB
date: 2024-10-19
description: A quick guide to running Docker Compose with your local MongoDB setup.
tags: 
    - Docker
    - MongoDB
categories:
    - Docker
    - MongoDB
---

If you want to run Docker Compose and use your local MongoDB, you'll need to modify the MongoDB configuration to allow external connections.

1. Open the MongoDB configuration file `mongod.conf`.

2. Edit the following line to enable connections from any IP address:

```yaml
net:
  # Other configurations...
  
  # Enable connection from any IP address
  bindIp: 0.0.0.0
```

3. Restart MongoDB