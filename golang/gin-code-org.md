# Code Organizing for A Gin Project

```
Project Root
├── config         config files
├── controller	   controller layer: verify submitted-data, then pass it to `service`
├── entity		   entities: structures of returned-data, and controller
├── main.go		   entry
├── model		   database ORM
├── proto		   protobuf files: gRPC, *.pb.go
├── repository	   database operations
├── router		   router: authentication, logging, exceptions
│   └── middleware router middleware
├── service		   business layer: business logic only, do NOT operate database
├── util		   tools: generic tools
└── vendor         extension packages
```

```
Clients:    PC | applet | Android | iOS
APIs:       HTTP, gRPC | authentication | exceptions & alarms | logs of request and response | health checks
Service:    gRPC | authentication | exceptions & alarms | logs of request and response | health checks | service-register-and-discovery
Database:   MySQL, Redis, Mongo
Middelware: Apollo(config center) | RabbitMQ (MQ) | visualized logs (ELK) | Jaeger (full link tracker) | visualized monitoring and alarm platform

innerNet: service, database, middelware
```
