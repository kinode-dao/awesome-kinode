# Awesome Hyperware

## Contents

* [Projects](#projects)
  * [Packages](#packages)
  * [Extensions](#extensions)
  * [Rollups](#rollups)
  * [Scripts and Tools](#scripts-and-tools)
  * [Libraries](#libraries)
* [Useful Regexes](#useful-regexes)
* [Documentation](#documentation)

## Projects

### Apps

* [Barter](https://github.com/bitful-pannul/auctioneer/), allows you to trade your NFTs through a telegram LLM chatbot, end to end.
* [Work in Progress - Filter](https://github.com/jaxs-ribs/filter), chrome extension using NN to filter out web content of your choice by semantic meaning.
* [MemeDeck](https://github.com/holium/kinode-memedeck), meme a better future with frens.
* [dartfrog](https://github.com/assemblycapital/dartfrog), a Hyperware app framework and browser.
     * [df-clicker](https://github.com/bacwyls/df-clicker), a game built with dartfrog-lib.
* [crdt-crm](https://github.com/dr-frmr/crdt-crm), an app using CRDTs to sync contact data.
* [kimap-explorer](https://github.com/dr-frmr/kimap_explorer), a tool to browse all entries in `hypermap`, Hyperware's onchain namespace.

### Packages

* [eth_template](https://github.com/Uncentered-Systems/eth_template), a template for using Ethereum with Hyperware.
* [folder_transfer](https://github.com/Uncentered-Systems/folder_transfer), a template for sending a folder from one node to another.
* [file_transfer](https://github.com/bitful-pannul/file_transfer), a package that allows nodes to share files between one another and serves a simple frontend to manage your shared files. Under active development by [@0x70b1a5](https://github.com/0x70b1a5).
* [sdapi](https://github.com/dr-frmr/sdapi), a simple package that serves a public HTTP API for fetching random Steely Dan lyrics.
* [kinode-prove-fib](https://github.com/nick1udwig/kinode-prove-fib), an example of using [SP1](https://github.com/succinctlabs/sp1) inside a Hyperware package.
* [kcard](https://github.com/dr-frmr/kcard), a package that generates node information as a public image file served over HTTP.

### Extensions

* [Hyperware Python](https://github.com/nick1udwig/kinode-python), an untrusted code runner.
* [Hyperware ML](https://github.com/nick1udwig/kinode-ml), a machine learning model runner.

### Rollups

* [Chess](https://github.com/hyperware-ai/chess-rollup), wager on your p2p chess matches.

### Scripts and Tools

* [kit](https://github.com/hyperware-ai/kit), the developer tool**kit** for Hyperware.

### Libraries

* [`process_lib`](https://github.com/hyperware-ai/process_lib), the UX-improving library for processes.
* [`process_macros`](https://github.com/hyperware-ai/process_macros), a library with procedural Rust macros for Hyperware processes.
* [Telegram Bot API for processes](https://github.com/hyperware-ai/telegram-bot)
* [Discord Bot API for processes](https://github.com/hyperware-ai/discord_api)
* [LLM API](https://github.com/hyperware-ai/llm), for Groq, OpenAi, as well as llama.cpp.
* [A Rust app framework for Hyperware apps, currently under development](https://github.com/hyperware-ai/app-framework).

## Useful Regexes

| Type                   | Regex                                                                   | Example input                               | Example output                                       | Description                                                            |
| ---------------------- | ----------------------------------------------------------------------- | ------------------------------------------- | ---------------------------------------------------- | ---------------------------------------------------------------------- |
| full process addresses | `^([a-z0-9-.]+)@([a-z0-9\-]+):([a-z0-9-]+):([a-z0-9-.]+)$`              | `undefined.os@process:package:publisher.os` | `undefined.os`, `process`, `package`, `publisher.os` | Separates a process address into node, process, package and publisher. |
| process IDs            | `^([a-z0-9-]+):([a-z0-9-]+):([a-z0-9-.]+)$`                             | `process:package:publisher.os`              | `process`, `package`, `publisher.os`                 | Separates a process address into process, package and publisher.       |
| package IDs            | `^([a-z0-9-]+):([a-z0-9-.]+)$`                                          | `package:publisher.os`                      | `package`, `publisher.os`                            | Separates a process address into package and publisher.                |
| KNS names              | `^[a-z0-9\-.]+$`                                                        | `undefined.os`                              |                                                      | Separates a KNS name into name and TLZ.                                |

To ensure forward compatibility, these regexes do not require any TLD such as `.os` or `.eth` (except for the KNS name regex).
Additionally, only lowercase alphanumeric characters and `-` are allowed within names.
[Test them on RegExr.](https://regexr.com)

## Documentation

* [The Hyperware Book](https://book.hyperware.ai)
