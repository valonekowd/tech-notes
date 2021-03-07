# Directory Structure

[Example](https://github.com/valonekowd/clean-architecture)

```bash
├── api
│   ├── openapi
│   └── proto
├── cmd
│   ├── app
│   ├── cli
│   └── testclient
├── config
│   ├── default.yml
│   ├── development.yml
│   ├── testing.yml
│   └── production.yml
├── domain
│   ├── entity
│   ├── factory
│   └── error
├── usecase
│   ├── interfaces
│   │   ├── gateway
│   │   └── presenter
│   ├── interactor
│   ├── request
│   └── response
├── adapter
│   ├── delivery
│   │   ├── http
│   │   ├── grpc
│   │   └── amqp
│   ├── endpoint
│   ├── formatter
│   ├── repository
│   └── middleware
├── infrastructure
│   ├── auth
│   ├── datastore
│   ├── router
│   ├── validator
│   ├── log
│   └── config
└── util
    └── helper
```