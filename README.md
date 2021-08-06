# Use Cloudflare Workers KV from Rust

This repository contains an example Cloudflare Worker which demonstrates how to
call Workers KV directly from Rust. The Worker forwards `GET` and `PUT` calls to
KV and thus acts as a very simple Key-Value store.

## Example Usage

Once the Worker is started using `wrangler dev` and listening on localhost, you
can put and get value to and from Workers KV:

```sh
$ curl 'localhost:8787/foo'
""
$ curl -X PUT 'localhost:8787/foo?value=bar'
$ curl 'localhost:8787/foo'
"bar"
```
