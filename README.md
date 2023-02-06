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
