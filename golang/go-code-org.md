# Code Organizing for A Go Project

```
Project Root
├── cmd         for multi-application projects, make them go get-table, like go-tools project
├── pkg         public libraries that can also be used by external projects
├── internal    codes inside cannot be access from outside the project, or files not in its parent directories
├── third_party imported external codes with modifications
└── vendor      imported external codes as is
```

```
Clients:    PC | applet | Android | iOS
APIs:       HTTP, gRPC | authentication | exceptions & alarms | logs of request and response | health checks
Service:    gRPC | authentication | exceptions & alarms | logs of request and response | health checks | service-register-and-discovery
Database:   MySQL, Redis, Mongo
Middelware: Apollo(config center) | RabbitMQ (MQ) | visualized logs (ELK) | Jaeger (full link tracker) | visualized monitoring and alarm platform

innerNet: service, database, middelware
```
