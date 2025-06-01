# serverless-proxy-server-cloudflare-vless

Short description
a serverless proxy server that run on cloudflare worker, running this proxy server allow you to create proxy server run on edge by custom ip.
README
Serverless Proxy Server on Cloudflare (vless)
Overview
This repository contains a serverless proxy server deployed on Cloudflare Workers. It acts as a relay between clients and external APIs, handling request forwarding, security measures, and response modification.

Features
Serverless: Runs entirely on Cloudflare Workers, eliminating the need for traditional servers.
Proxy Support: Routes requests from clients to external APIs with modifications.
Prerequisites
Ensure you have:

A Cloudflare account with Workers enabled.
Wrangler CLI installed (npm install -g wrangler).
An API to proxy requests to.
Installation
Clone the repository and navigate to the directory:

Just make the cf worker and copy this _worker.js
make sure the uuid is unique
