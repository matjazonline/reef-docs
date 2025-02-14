---
title: "Troubleshooting"
description: "Here are the common errors new developers encounter, and their solutions."
lead: "Here are the common errors new developers encounter, and their solutions."
date: 2020-11-12T15:22:20+01:00
lastmod: 2020-11-12T15:22:20+01:00
draft: false
images: []
menu:
  docs:
    parent: "help"
weight: 620
toc: true
---

### FATAL: Unable to initialize the API: createType(CurrencyId):: Cannot construct unknown type CurrencyId
You are missing the [types.json](https://github.com/reef-defi/reef-chain/blob/master/assets/types.json) file in the developer settings of the console.

[>> Docs](/docs/developers/resources/#developer-console)

### Bootnode with peer id ... is on a different chain (our genesis: 0x... theirs: 0x...)
If you compiled the `reef-node` binary yourself you will have to initialize the chain with the chain
spec file, since the WASM builds are not deterministic. Just do `--chain chain-spec.json`.

[>> Docs](/docs/developers/nodes/#start-a-rpc-node)

### Weird database errors
Whenever you run into some sort of database error, `purge-cache` subcommand is your friend.
You can do a fresh sync after the purge, and things should just work.

[>> Docs](/docs/developers/resources/#reset-the-local-chain)


