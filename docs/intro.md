---
slug: /
sidebar_position: 1
title: Introduction
---

# Nethermind's RPC Service for Starknet builders

Keen to get started? You can send your first few requests to one of our open endpoints, without the need for an API key.

```
https://free-rpc.nethermind.io/mainnet-juno/
```

```
https://free-rpc.nethermind.io/goerli-juno/
```

Try this.

```bash
curl --location 'https://free-rpc.nethermind.io/mainnet-juno/' \
--data '{
	"jsonrpc":"2.0",
	"method":"starknet_blockNumber",
    "id":1
}'
```

Read on for details of our full service endpoints.
