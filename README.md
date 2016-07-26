# Modbus TCP Slave simulator in Node.js

[![Dependency Status](https://www.versioneye.com/user/projects/57600572433d18002c19d67e/badge.svg?style=flat)](https://www.versioneye.com/user/projects/57600572433d18002c19d67e)

Dummy modbus slave server in node.js

## Recommended alternative

[c-modbus-slave](https://github.com/taka-wang/c-modbus-slave)


## Installation
```bash
sudo npm install 
```

## Test
```bash
sudo node server
```

## Docker

### From the scratch
```bash
# build docker image 
docker build -t takawang/node-modbus-slave .

# run the image (host_port:container_port)
docker run -p 502:502 -d --name slave takawang/node-modbus-slave
# Print app output
docker logs <container id>
# Enter the container
docker exec -it <container id> /bin/bash
```

### Pull pre-built docker image
```bash
docker pull takawang/node-modbus-slave

# arm version
#docker pull arm-node-modbus-slave
```

## Credit
According to [node-modbus-tcp package](https://github.com/dresende/node-modbus-tcp), I rewrite some handle functions for testing.