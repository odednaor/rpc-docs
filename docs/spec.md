---
slug: /spec
sidebar_position: 4
title: RPC spec versions
---

# RPC spec versions

The RPC service will support only the latest and the previous versions of the RPC spec. Specifying the spec version on the path is optional but recommended.

Use `rpc/v0_5` on the path to specify version `v0.5.0`.

### Latest version

By default, we serve the latest version of the spec implemented by the full nodes.

Using this approach means that when we upgrade to a new full node version with a higher spec version supported, any breaking changes in Starknet may break your code.

```bash
curl --location 'https://limited-rpc.nethermind.io/mainnet-juno/' \
--data '{
	"jsonrpc":"2.0",
	"method":"starknet_specVersion",
    "id":1
}'
```

### Specific version

To request a specific version of the spec, you can add it to the path, like this. This way there's no doubt which spec version you're calling, but you'll need to keep up with new spec versions as we support them.

```bash
curl --location 'https://limited-rpc.nethermind.io/mainnet-juno/rpc/v0_5' \
--data '{
	"jsonrpc":"2.0",
	"method":"starknet_specVersion",
    "id":1
}'
```
