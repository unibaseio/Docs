# Stream Node

#### Network Requirements

High network requirements, requires an external IP address.

**standard**

* CPU: 16 core
* Memory: 32GB
* Storage: 4TB HDD
* Network: public IP, 100mbps

**minimal**

* CPU: 8 core
* Memory: 16GB
* Storage: 1TB HDD
* Network: public IP, 10mbps

#### Run

Initialize, using the \~/.stream directory by default

```shell
./stream-edge init
```

Using port 8083 by default, port 8083 needs to be accessible from the external network

```shell
./stream-edge daemon run -e EXPOSE_URL
```

For example, if the external IP is 1.2.3.4

```bash
./stream-edge daemon run -b 0.0.0.0:8083 -e http://1.2.3.4:8083
```
