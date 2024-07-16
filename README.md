# Awesome Kinode

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
* [MemeDeck](https://github.com/holium/kinode-memedeck), Meme a better future with frens.
* [dartfrog](https://github.com/assemblycapital/dartfrog), a kinode app browser

### Packages

* [file_transfer](https://github.com/bitful-pannul/file_transfer), a package that allows nodes to share files between one another and serves a simple frontend to manage your shared files. Under active development by [@0x70b1a5](https://github.com/0x70b1a5).
* [sdapi](https://github.com/dr-frmr/sdapi), a simple package that serves a public HTTP API for fetching random Steely Dan lyrics.
* [kinode-prove-fib](https://github.com/nick1udwig/kinode-prove-fib), an example of using [SP1](https://github.com/succinctlabs/sp1) inside a Kinode package.
* [safe](https://github.com/kinode-dao/safe), a Gnosis Safe frontend (plus a little backend!). Under active development by [@jurassic.technology](https://github.com/jurassic-technology).
* [crdt-crm](https://github.com/dr-frmr/crdt-crm), a simple example of a contacts app using CRDTs to sync data between app users.

### Extensions

* [Kinode Python](https://github.com/nick1udwig/kinode-python), an untrusted code runner.
* [Kinode ML](https://github.com/nick1udwig/kinode-ml), a machine learning model runner.

### Rollups

* [Chess](https://github.com/kinode-dao/chess-rollup), wager on your p2p chess matches.

### Scripts and Tools

* [kit](https://github.com/kinode-dao/kit), the developer tool**kit** for Kinode.

### Libraries

* [`process_lib`](https://github.com/kinode-dao/process_lib), the UX-improving library for processes.
* [Telegram Bot API for processes](https://github.com/kinode-dao/telegram-bot)
* [Discord Bot API for processes](https://github.com/kinode-dao/discord_api)
* [LLM API](https://github.com/kinode-dao/llm), for Groq, OpenAi, as well as llama.cpp.

### Useful Regexes

| Type                   | Regex                                                                   | Example input                               | Example output                                       | Description                                                            |
| ---------------------- | ----------------------------------------------------------------------- | ------------------------------------------- | ---------------------------------------------------- | ---------------------------------------------------------------------- |
| full process addresses | `^([a-z0-9-_.]+)@([a-z0-9\-_]+):([a-z0-9-_]+):([a-z0-9-_.]+)$` | `undefined.os@process:package:publisher.os` | `undefined.os`, `process`, `package`, `publisher.os` | Separates a process address into node, process, package and publisher. |
| process IDs            | `^([a-z0-9-_]+):([a-z0-9-_]+):([a-z0-9-_.]+)$`                          | `process:package:publisher.os`              | `process`, `package`, `publisher.os`                 | Separates a process address into process, package and publisher.       |
| package IDs            | `^([a-z0-9-_]+):([a-z0-9-_.]+)$`                                        | `package:publisher.os`                      | `package`, `publisher.os`                            | Separates a process address into package and publisher.                |
| KNS names              | `^([a-z0-9-_]+)\.([a-z]+)$`                                             | `undefined.os`                              | `undefined`, `os`                                    | Separates a KNS name into name and TLD.                                |

To ensure forward compatibility, these regexes do not require any TLD such as `.os` or `.eth` (except for the KNS name regex).
Additionally, only alphanumeric characters, `-` and `_` are allowed within names.
[Test them on RegExr.](https://regexr.com)

## Documentation

* [The Kinode Book](https://book.kinode.org)
