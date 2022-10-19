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
