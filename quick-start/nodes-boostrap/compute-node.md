# Compute Node

Consists of compute-controller and compute-worker, currently these two are combined.

Compute nodes require high-performance GPUs and an external IP address.

#### Requirement

**standard**

* CPU: 16 core
* Memory: 32GB
* GPU: NVIDIA GPU with 12GB memory
* Storage: 1TB nvme
* Network: public IP, 10mbps

**minimal**

* CPU: 8 core
* Memory: 16GB
* GPU: NVIDIA GPU with 8GB memory
* Storage: 100GB ssd
* Network: public IP, 5mbps

#### Prepare

**GPU Driver**

1. Install the GPU driver

https://ubuntu.com/server/docs/nvidia-drivers-installation

After installation, check the graphics card information

```shell
> nvidia-smi
```

2. Install cuda require: cuda11.7.1

https://developer.nvidia.com/cuda-downloads

**Install Docker**

https://yeasy.gitbook.io/docker\_practice/install

* Add User

Create a docker group and add the user to this group

```shell
sudo groupadd docker
sudo usermod -aG docker $USER
sudo systemctl restart docker
docker info
```

* Install docker nvidia toolkit

https://docs.nvidia.com/datacenter/cloud-native/container-toolkit/latest/install-guide.html

* pull image

```shell
docker pull nvidia/cuda:11.7.1-cudnn8-runtime-ubuntu20.04
```

#### Run

Initialize, using the \~/.compute directory by default

```shell
./compute-edge init
```

Using port 8081 by default, port 8081 needs to be accessible from the external network

```shell
./compute-edge daemon run -e EXPOSE_URL
```

For example, if the external IP is 1.2.3.4

```shell
./compute-edge daemon run -b 0.0.0.0:8081 -e http://1.2.3.4:8081
```
