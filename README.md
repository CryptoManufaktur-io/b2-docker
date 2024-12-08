# Archived repo

Please use [Optimism Docker](https://github.com/CryptoManufaktur-io/optimism-docker) for B^2 RPC nodes

# Overview

Docker Compose for B^2 rollup

`cp default.env .env`, then `nano .env` and adjust values, particularly SNAPSHOT

This repo does not support B^2 on Sepolia at present

Meant to be used with [central-proxy-docker](https://github.com/CryptoManufaktur-io/central-proxy-docker) for traefik
and Prometheus remote write; use `:ext-network.yml` in `COMPOSE_FILE` inside `.env` in that case.

If you want the op-geth RPC ports exposed locally, use `rpc-shared.yml` in `COMPOSE_FILE` inside `.env`.

The `./b2d` script can be used as a quick-start:

`./b2d install` brings in docker-ce, if you don't have Docker installed already.

`cp default.env .env`

`nano .env` and adjust variables as needed, particularly `SNAPSHOT`

`./b2d up`

To update the software, run `./b2d update` and then `./b2d up`

This is B2 Docker v1.0.0
