# Microservice in go

## Introduction

-
📚 [Course Build highly available, scalable, resilient distributed applications using Go](https://novopayment.udemy.com/course/working-with-microservices-in-go)

This is a simple microservice in go. It is a simple REST API that returns a JSON object with a message.

- [Web Frontend](http://localhost/)
- [Mail hog](http://localhost:8025/)

## Installation

- [Installation](https://grpc.io/docs/protoc-installation/)
- [gRPC Protobuf](https://github.com/protocolbuffers/protobuf/releases)

## Develop

Generate the protobuf files

```bash
cd logger-service/logs
protoc --go_out=. --go_opt=paths=source_relative --go-grpc_out=. --go-grpc_opt=paths=source_relative logs.proto
```

Build Caddy

```bash
cd project
docker build -f caddy.dockerfile -t tsawler/caddy:1.0.0 .
```

### Swarm

Init the swarm

```bash
swarm init
```

Deploy the stack

```bash
cd project
stack deploy -c .\swarm.yml myapp
```

Up scale the service

```bash
docker service scale myapp_authentication-service=3
```

Delete stack

```bash
stack rm myapp
```

Exit the swarm

```bash
swarm leave
```

Force exit the swarm

```bash
swarm leave --force
```
