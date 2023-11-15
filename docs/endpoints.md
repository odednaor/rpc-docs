---
slug: /endpoints
sidebar_position: 2
title: Endpoints
---

# Endpoints

Nethermind's endpoints for Starknet RPC are as follows.

#### Mainnet

```
rpc.nethermind.io/mainnet-juno/
```

#### Goerli

```
rpc.nethermind.io/goerli-juno/
```

#### Integration

```
rpc.nethermind.io/integration-juno/
```

## Ports

`https` and `wss` are supported.

## Rate limits

Our gateway enforces a rate limit which is set as high as possible for our supporting infra. Most users will never hit this limit. If your application is ingesting on-chain historical data and you hit the limit, get in touch and we can discuss this.

No per-IP rate limit applies by default. If you need this, for example because you need your API keys to be on the client, get in touch and we can add one for you.

## Sticky sessions

Requests from the same client IP will be served by the same underlying full node implementation by default. This is to ensure a consistent state from one request to the next.

There are some data ingestion uses cases in which this is not what you want. Please get in touch if this is you.
