# Local MQTT and Kafka stack

This Compose stack runs Eclipse Mosquitto as the MQTT broker and Apache Kafka in single-node KRaft mode.

## Start

From this project directory, run:

```sh
docker compose up -d
```

If `docker compose` is unavailable, install or enable the Docker Compose v2 plugin in Docker Desktop, then retry.

## Endpoints

- MQTT from this computer: `localhost:1883`
- Kafka from this computer: `localhost:9092`
- Kafka from another Compose container: `kafka:29092`

Mosquitto allows anonymous connections for local development only. Add authentication and access controls before exposing it outside a trusted local environment.

## Stop

```sh
docker compose down
```

The named volumes retain broker data. To remove the containers and their stored data, use `docker compose down -v`.