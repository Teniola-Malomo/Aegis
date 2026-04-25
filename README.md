# Aegis

A cybersecurity system that uses federated learning and blockchain to detect threats. It shares threat data in a decentralized way and monitors network traffic in real time to identify attacks like DDoS and botnets, while keeping data private.

**Final Year Project - Dublin City University**

## How it works

- An ML model watches network traffic and picks up on DDoS, botnets, and command-and-control (C&C) activity
- Federated learning lets multiple nodes train the model together without sharing raw data
- A blockchain ledger (Hyperledger Fabric) keeps a secure, tamper-proof record of shared threat data
- A React dashboard shows what's happening in real time
- Zeek handles the network monitoring and telemetry
- Everything runs in Docker containers for easy setup and testing

## Built with

Python, PyTorch, React, Hyperledger Fabric, Zeek, MongoDB, InfluxDB, Grafana, Telegraf, Docker

## Docker

The whole system is containerized - 6 services, all on [Docker Hub](https://hub.docker.com/r/panichb2/aegis/tags):

| Container | What it does | Size |
|-----------|-------------|------|
| `panichb2/aegis:p2pfl` | Federated learning node - trains and shares ML models across peers | ~1 GB |
| `panichb2/aegis:slips` | Network intrusion detection - watches traffic for threats | ~1.5 GB |
| `panichb2/aegis:hiero-ledger` | Blockchain ledger - stores shared threat data securely | ~545 MB |
| `panichb2/aegis:grafana` | Dashboard - visualizes network metrics and alerts | ~173 MB |
| `panichb2/aegis:influxdb` | Time-series database - stores telemetry and metrics | ~174 MB |
| `panichb2/aegis:telegraf` | Metrics collector - gathers data from services and pushes to InfluxDB | ~118 MB |

```bash
# Pull all containers
docker pull panichb2/aegis:p2pfl
docker pull panichb2/aegis:slips
docker pull panichb2/aegis:hiero-ledger
docker pull panichb2/aegis:grafana
docker pull panichb2/aegis:influxdb
docker pull panichb2/aegis:telegraf
```
