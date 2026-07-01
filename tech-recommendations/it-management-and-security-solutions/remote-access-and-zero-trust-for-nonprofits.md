---
description: >-
  Compare simple, nonprofit-friendly tools for secure remote access to internal
  systems and networks.
icon: road-lock
---

# Remote Access & Zero Trust for Nonprofits

Remote access should not require exposing your network to the public internet. We recommend zero trust platforms instead of traditional VPNs because they verify users and devices before granting access.

{% hint style="info" %}
If you only need safer internet access on laptops and phones, start with [Cloudflare WARP](../../tech-guides/security-guides/securing-network-traffic-on-your-pc-using-cloudflare-warp.md). If users need access to office resources, use a zero trust platform.
{% endhint %}

## Why we no longer recommend traditional VPNs

Traditional VPNs are no longer our recommended first choice for most nonprofits. They usually rely on a public-facing VPN gateway and exposed services, which increases your attack surface and security risk considerably.

Zero trust platforms are safer because they can limit access to specific apps, servers, and networks without broadly exposing internal systems.

## Recommended platforms

### Twingate

<div align="left"><img src="https://cdn.simpleicons.org/twingate" alt="Twingate logo" width="188"></div>

[Twingate](https://www.twingate.com/) is our easiest recommendation for small nonprofits that want secure remote access with minimal setup.

* Free for up to **5 users**.
* Easy to configure for small IT teams and network admins.
* Works well with **Google**, **Microsoft**, and other identity providers.
* Uses a simple connector-and-client model.
* Can add DNS protection on managed endpoints.

**Best fit**

* Small teams
* A few internal apps or servers
* Organizations that want faster setup and simpler administration

Install the connector where your internal resources live. Then install the client on each device that needs access.

[Twingate website](https://www.twingate.com/)\
[Sign up for Twingate Starter](https://auth.twingate.com/signup?flow=starter\&useCase=hobby) (free tier)

### Cloudflare Zero Trust

<div align="left"><img src="https://cdn.simpleicons.org/cloudflare" alt="Cloudflare logo" width="188"></div>

[Cloudflare Zero Trust](https://www.cloudflare.com/products/zero-trust/) is a strong fit when you want remote access plus broader security controls.

* Free for up to **50 users**.
* Supports private network access and published internal web apps.
* Works well with Microsoft 365 and Google sign-in.
* Can also add DNS filtering and broader endpoint protections.

**Best fit**

* Organizations already using Cloudflare
* Teams that want one platform for remote access and web security
* Setups that need tunnels, policies, or app-level controls

Cloudflare Zero Trust is more flexible than Twingate. It also takes more setup.

[Cloudflare Zero Trust Setup](../../tech-guides/security-guides/cloudflare-zero-trust-setup.md)\
[Logging Into Cloudflare Zero Trust](../../tech-guides/security-guides/logging-into-cloudflare-zero-trust.md)

## Quick recommendation

For most small nonprofits, start with **Twingate** if you want the simplest rollout and 5 or less users. Choose **Cloudflare Zero Trust** if you need more controls or already use Cloudflare. Add [Cloudflare WARP](../../tech-guides/security-guides/securing-network-traffic-on-your-pc-using-cloudflare-warp.md) for safer internet access on laptops and phones, but not as a replacement for remote access.

{% hint style="warning" %}
Avoid exposing Remote Desktop, file shares, admin portals, or VPN services directly to the internet.
{% endhint %}
