# Codelivery simulator + kafka producer

## Description

This repo will produce mock data into a kafka topic in order for it to be consumed by other kafka consumers. Besides that, this repo also contain the image to manage the kafka instance;

## How to use

execute the following commands

```bash
docker-compose up -d
# access container
docker-compose exec app bash
# Run Golang app
go run main.go
```

Set a kafka console consumer

```bash
kafka-console-consumer --bootstrap-server=localhost:9092 --topic=route-new-position --group=terminal
```

Set a kafka console producer

```bash
kafka-console-producer --bootstrap-server=localh:9092 --topic=route-new-direction
```

Post messages to the kafka producer console

```json
{"clientId":"1", "routeId": "1"}
{"clientId":"2", "routeId": "2"}
{"clientId":"3", "routeId": "3"}
```