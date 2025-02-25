---
title: Setup headscale on free-tier VPS - Introduction
description: Article Template
draft: false
tags: 
date: 2025-02-06 17:48
---
## Purpose

For everyone who embark in the adventure of self-hosting, there is always the problematic of accessing our server at distance without exposing it publicly.
To answer this problematic, we need a [VPN](https://en.wikipedia.org/wiki/Virtual_private_network). It exists a plenty of [VPN](https://en.wikipedia.org/wiki/Virtual_private_network) solutions you can use for your self-hosting :
- [OpenVPN](https://openvpn.net/)
- [Wireguard](https://www.wireguard.com/)
- [Tailscale](https://tailscale.com/)
- ...

In these articles, we will focus on the last one [Tailscale](https://tailscale.com/) with his open-source version [Headscale](https://headscale.net/stable/).

## Tailscale

[Tailscale](https://tailscale.com/) work with a [client](https://github.com/tailscale/tailscale) (open source) you install on the device you want to connect to your Tailnet (Tailscale network) and a [server](https://tailscale.com/) (proprietary) hosted by Tailscale. The client create a tunnel to the server so you don't need to open any port on your firewall. 
They propose a free tier offer for personal use who propose to connect maximum 100 devices which is pretty decent, but only 3 users can connect on your network. So, in case you want to give access at your network to family and friends or using it in a professional, the free tier will not be enough.

Fortunately, thanks to the open source community, there is an alternative to this proprietary server who use the same client : [Headscale](https://headscale.net/stable/).

## Headscale

[Headscale](https://headscale.net/stable/) is an open source alternative for the control server of [Tailscale](https://tailscale.com/) which can be self-hosted and configured like you want (number of users and devices unlimited).

The disadvantage of using [Headscale](https://headscale.net/stable/) instead of [Tailscale](https://tailscale.com/) is that because you need to host the server yourself, you need to open a port (443) so server can be reach from outside your home network. So, hosting [Headscale](https://headscale.net/stable/) on your home network can be not convenient.

There is an alternative to this. It's to host [Headscale](https://headscale.net/stable/) outside your network. Fortunately, there is some VPS provider who propose a free tier. In these article, I'm going to present the setup with [Oracle cloud](https://www.oracle.com) free tier VPS.

## Resources
These articles are inspired by the two guides :
- [How To VPN Without Port Forwarding Using Headscale & Tailscale - Complete Tutorial](https://www.youtube.com/watch?v=u_6Zd7Bo6J4)
- [How to combine Headscale with Nginx Proxy Manager and Cloudflare to form a self-hosted VPN on Ubuntu 22.04](https://silicon.blog/2023/05/14/how-to-combine-headscale-with-nginx-proxy-manager-and-cloudflare-to-from-a-self-hosted-vpn-on-ubuntu-22-04/)

These two guides lack of some steps so I decided to write my own guide




