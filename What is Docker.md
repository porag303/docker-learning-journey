## What is Docker?

>Docker is an open-source platform that simplifies the process of `building`, `testing`, and `deploying` applications. It allows developers to package applications along with all their dependencies into lightweight containers, which can then be run consistently across different environments. Docker helps streamline the software delivery process by enabling isolation and portability, regardless of the underlying infrastructure.

## Key Components of Docker

### Docker Client
>The Docker client is the interface through which users interact with Docker. It's a command-line tool (CLI) that sends requests to the Docker daemon using the REST API. When you run a Docker command, the client sends that command to the Docker daemon for execution.

### Docker Daemon
>The Docker daemon is the core component that manages Docker containers. It is responsible for building, running, and distributing containers. It also manages data such as images, volumes, and configurations, storing them in a central directory.

## Docker vs Virtual Machines (VMs)

>Docker containers differ significantly from traditional virtual machines. Unlike VMs, which require their own operating system, Docker containers share the host system's `kernel` and `resources`. This shared architecture allows for more efficient use of system resources like CPU, memory, and storage. As a result, you can run more containers on the same hardware compared to VMs, leading to lower overhead and faster performance.

## Checking Docker Status

`systemctl status docker`

## Checking Docker Version

`docker --version`
