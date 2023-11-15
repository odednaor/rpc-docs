---
slug: /spec
sidebar_position: 4
title: RPC spec versions
---

# Using a specific version of the RPC spec

The service will support each version of the RPC spec from version `v0.4.0` onwards. Specifying the spec version on the path is optional.

Use `v0_5` on the path to specify version `v0.5.0`.

### Latest version

By default, we serve the latest version of the spec implemented by the full nodes.

```bash
curl --location 'https://limited-rpc.nethermind.io/mainnet-juno/' \
--data '{
	"jsonrpc":"2.0",
	"method":"starknet_specVersion",
    "id":1
}'
```

### Specific version

If you need a specific version of the spec, you can add it to the path, like this.

```bash
curl --location 'https://limited-rpc.nethermind.io/mainnet-juno/v0_5' \
--data '{
	"jsonrpc":"2.0",
	"method":"starknet_specVersion",
    "id":1
}'
```
