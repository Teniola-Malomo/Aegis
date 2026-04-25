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

Python, PyTorch, React, Hyperledger Fabric, Zeek, MongoDB, Docker

## Docker

Pre-built containers are on Docker Hub:

```
docker pull panichb2/aegis
```

[View all tags on Docker Hub](https://hub.docker.com/r/panichb2/aegis/tags)
