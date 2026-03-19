---
description: >-
  Players getting stuck on "Fetching server variables..." when trying to fly
  into your city.
---

# "Fetching server variables..."

### **What does** "Fetching server variables..." mea&#x6E;**?**

It’s the stage where your FiveM client is:

1. Connecting to the server.
2. Downloading basic info (server config, player slots, resources, etc.).
3. Getting ready to load in.

If it **hangs here**, it means your client isn't getting a valid response from the server in time, or something is blocking the request.

### Common Causes & Fixes

#### Server Resource Error / Broken Config

<details>

<summary>Server’s <code>server.cfg</code> is misconfigured.</summary>

* Double-check your `server.cfg`:
  * Ensure `start`/`ensure` lines are correct and ordered properly.
  * Make sure `server.cfg` ends with `start sessionmanager` (core resource).

</details>

<details>

<summary>Required resource is crashing or not loading properly.</summary>

* Check server logs (`console` or `txAdmin`) for errors or crashes.

</details>

<details>

<summary>Essential scripts missing or crashing during init.</summary>

* Restart server and test in dev mode with fewer scripts to isolate
* Check server logs (`console` or `txAdmin`) for errors or crashes.

</details>

#### Client-Server Communication Timeout

<details>

<summary>Your client is trying to connect but the server is too slow or blocked.</summary>

* Restart router/modem.
* Switch networks (e.g., use hotspot or VPN to test).
* Try connecting using direct IP (`F8` console → `connect <IP>:30120`).

</details>

<details>

<summary>High latency or packet loss.</summary>

* Check for packet loss using `ping` or `tracert` or `MTR` to the server IP.
  * See how to do these here: [**Basic Network Troubleshoot**](https://docs.1of1servers.com/1-of-1-knowledge-base/networking-guides/basic-network-troubleshoot)**.**

</details>

<details>

<summary>The server is not properly reachable on required ports.</summary>

On the servers Windows Firewall, ensure the following Inbound Rules are properly created:

* Ensure **port 30120** (UDP and TCP) are open and properly forwarded.
* Ensure **port 40120** (TCP) is open and properly forwarded.

</details>

#### Custom Resources Causing Timeouts

<details>

<summary>Bad or heavy scripts (like bad MySQL async calls or infinite loops).</summary>

* Comment out all `start` lines in `server.cfg`, then re-add one by one to isolate the problematic resource.
* Ensure all scripts are updated and compatible with current FiveM builds.

</details>

<details>

<summary>Server gets stuck loading a resource and never responds.</summary>

* Watch the console: if it hangs on a specific resource, fix or remove it.
* Ensure all scripts are updated and compatible with current FiveM builds.

</details>

#### Corrupted Cache

<details>

<summary>Broken cache files on the client prevent proper communication.</summary>

Have the player clear their FiveM cache:

* Close FiveM
* Go to `%localappdata%\FiveM\FiveM.app\data\cache` and delete everything **except** the `game` folder.

</details>

#### Outdated Server or Client

<details>

<summary>Old FXServer build, artifacts, or client not synced with current FiveM version.</summary>

* Make sure your client is updated (FiveM auto-updates, but check manually if needed).
* Update your server:
  * Download latest FXServer artifacts.
  * Rebuild or update all resources to match modern standards.
* Have player running same version of FiveM/GTAV as your server.
  * Have the player verify their game files (FiveM & GTAV)

</details>

#### Reverse Proxy / SSL / TLS Conflicts

<details>

<summary>Reverse proxy or Cloudflare tunnels on the server mess with FiveM’s fetch requests.</summary>

* Avoid reverse proxies unless you know exactly how to configure them.
* If using Cloudflare tunnels or TCPShield, make sure FiveM ports are correctly proxied and not filtered.
* Ensure HTTPS or TLS is properly configured (if you're using endpoints like webhooks or APIs in scripts).

</details>

#### Bonus Tips!

* **Run server locally** (on same machine) with minimal resources to test.
* **Check client F8 console** for errors during load.
* **Use network sniffers** like Wireshark or logs from `txAdmin` to track stuck connections.
  * See how to do these here: [**Basic Network Troubleshoot**](https://docs.1of1servers.com/1-of-1-knowledge-base/networking-guides/basic-network-troubleshoot)**.**
* **Temporarily disable all firewall/AV** (client side) to test connectivity.
