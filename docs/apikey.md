---
slug: /apikey
sidebar_position: 3
title: API key
---

# Passing your API key

You may pass your API key in a header or in the query string.

Some client SDKs situations like the Starknet React providers only work with the query string approach. Everywhere else, it's preferable to use the header approach.

### Header

Pass an HTTP header called `x-apikey`. Do not prefix the value with `Bearer`, just pass the value of your API key.

```bash
curl --location 'https://rpc.nethermind.io/mainnet-juno/' \
--header 'x-apikey: API_KEY' \
--data '{
	"jsonrpc":"2.0",
	"method":"starknet_blockNumber",
    "id":1
}'
```

### Query string

Pass the value in a query string parameter called `apikey`, eg. `/mainnet-juno/?apikey=API_KEY`.

```bash
curl --location 'https://rpc.nethermind.io/mainnet-juno/?apikey=API_KEY' \
--data '{
	"jsonrpc":"2.0",
	"method":"starknet_blockNumber",
    "id":1
}'
```
