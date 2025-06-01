# serverless-proxy-server-cloudflare-vless

Short description
a serverless proxy server that run on cloudflare worker, running this proxy server allow you to create proxy server run on edge by custom ip.
README
Serverless Proxy Server on Cloudflare (vless)
Overview
This repository contains a serverless proxy server deployed on Cloudflare Workers. It acts as a relay between clients and external APIs, handling request forwarding, security measures, and response modification.

# Serverless Proxy Server on Cloudflare

## Overview
This repository contains a **serverless proxy server** deployed on **Cloudflare Workers**. It acts as a relay between clients and external APIs, handling request forwarding, security measures, and response modification.

## Features
- **Serverless**: Runs entirely on Cloudflare Workers, eliminating the need for traditional servers.
- **Proxy Support**: Routes requests from clients to external APIs with modifications.
- **Logging**: Implements basic logging mechanisms for debugging purposes.
- **Error Handling**: Includes robust error handling for failed requests.

## Prerequisites
Ensure you have:
- A **Cloudflare account** with Workers enabled.
- **Wrangler CLI** installed (`npm install -g wrangler`).
- An API to proxy requests to.

## Installation
git clone <repository-url>
cd serverless-proxy-cloudflare
Just make the cf worker and copy this _worker.js
make sure the uuid is unique

# VLESS Proxy Configuration Guide

## Overview
This guide provides instructions on setting up a **VLESS proxy server** using the provided configuration. VLESS is a lightweight proxy protocol commonly used with **Xray-core** for improved privacy and bypassing network restrictions.

## Configuration Breakdown
```
vless://6513bc58-71a3-4593-bb23-5113ddf2fc22@quiz.int.vidio.com:443?path=%2F51.79.158.126%3A443&security=tls&encryption=none&host=nganu.anjadvpn.my.id&fp=randomized&type=ws&sni=nganu.anjadvpn.my.id#shinyf
```
| **Parameter**  | **Description** |
|---------------|----------------|
| `vless://` | Protocol type, indicating use of **VLESS** (a proxy without built-in encryption). |
| `6513bc58-71a3-4593-bb23-5113ddf2fc22` | **UUID** used for authentication. |
| `quiz.int.vidio.com:443` | **Server domain** and port (`443` for TLS support). |
| `path=%2F51.79.158.126%3A443` | Routing path; `%2F` represents `/`, redirecting to `51.79.158.126:443`. |
| `security=tls` | Enables **TLS encryption** for secure communication. |
| `encryption=none` | No additional encryption beyond TLS. |
| `host=nganu.anjadvpn.my.id` | The **SNI hostname**, required for TLS verification. |
| `fp=randomized` | Randomized fingerprint, improving stealth against detection. |
| `type=ws` | Transport type is **WebSocket** (`ws`), ensuring compatibility. |
| `sni=nganu.anjadvpn.my.id` | Specifies **Server Name Indication (SNI)** for TLS authentication. |
| `#shinyf` | A custom tag for distinguishing configurations. |

## Prerequisites
- A **VLESS-compatible client** (Xray-core, V2Ray, or Clash).
- A properly configured **TLS certificate** (if using a custom domain).
- A stable **network connection**.

## Setup Instructions
### 1. Install Xray-core or VLESS-Compatible Client
Download and install **Xray-core** using: v2rayNG
Import configuration and start
