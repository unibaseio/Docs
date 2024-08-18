# Storage Node

#### Requirements

```
standard
    CPU: 8 core
    Memory: 16GB
    Storage: 4TB HDD
    Network: 100mbps

minimal
    CPU: 4 core
    Memory: 8GB
    Storage: 1TB HDD
    Network: 10mbps
```

#### Run

Initialize, using the \~/.store directory by default

```shell
./store-edge init
```

Using port 8082 by default

```shell
./store-edge daemon run -e EXPOSE_URL
```

For example, if the external IP is 1.2.3.4, port 8082 can be accessed from the external network

```shell
./store-edge daemon run -b 0.0.0.0:8082 -e http://1.2.3.4:8082
```

For example, if the external IP is 1.2.3.4, port 8082 cannot be accessed from the external network

```shell
./store-edge daemon run -b 0.0.0.0:8082
```
