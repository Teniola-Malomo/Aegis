# Aegis

Blockchain-enabled federated learning framework for cyber threat detection.

Detects DDoS, botnets, and C&C activity while keeping data decentralized and private.

**Final Year Project - Dublin City University**

## Tech Stack

Python, PyTorch, React, Hyperledger Fabric, Zeek, MongoDB, Docker

## Docker

Pre-built containers available on Docker Hub:

```
docker pull panichb2/aegis
```

[View on Docker Hub](https://hub.docker.com/r/panichb2/aegis/tags)

## Architecture

- ML model for tracking network traffic, C&C activities, DDoS, and botnets
- Federated learning for decentralized model training
- Blockchain ledger (Hyperledger Fabric) for secure data sharing
- React dashboard populated with backend data
- Zeek for network monitoring and telemetry
- Docker for multi-environment network traffic testing
