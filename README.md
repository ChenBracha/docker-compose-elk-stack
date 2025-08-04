# ELK + Filebeat + Docker Log Simulation

This project runs a full ELK stack (Elasticsearch, Logstash, Kibana) with Filebeat and a log-generating container — all inside Docker Compose.

## Features

- ELK stack in Docker
- Filebeat shipping logs from a shared volume
- Fake VM container generating logs
- No install required on host

## Usage

```bash
docker-compose up -d

