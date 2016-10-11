---
title: ""
---

Snyk can be used with private GitHub Enterprise installations via a [custom proxy](https://github.com/Snyk/broker), referred to as the Snyk "broker". A Snyk broker can also be used between Snyk and github.com itself, to reduce Snyk's access to your GitHub repositories.

The Snyk broker is made up of two web servers that proxy requests over a secure web socket connection. The broker "client" runs within your network, in a location with connectivity to your GitHub Enterprise. On start-up it establishes a secure web socket connection to a broker "server" running at https://broker.snyk.io. Both requests from Snyk to your GitHub Enterprise, and web-hook initiated requests from your GitHub Enterprise to Snyk, are sent over this tunnel.

The client has a white list of allowed requests (expressed as a JSON file), ensuring that only requests which are required for Snyk to function are proxied. All other requests are dropped. Requests are filtered on both request path, and JSON body.

These instructions will get you up and running with a Snyk broker, allowing your private GitHub Enterprise to connect to Snyk.io.
