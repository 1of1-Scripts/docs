---
description: CURL 28 Error code
---

# CURL 28 ERROR

### **What is CURL 28?**

**CURL 28 error** in **FiveM** means that a **network operation timed out** — essentially, the client tried to connect to the server or fetch data, but didn’t get a response **within the timeout limit**.

* **Error 28 message**:
  * "Timeout was reached."

This usually points to a **slow server response**, a **blocked request**, or **network-level delays**.

### Common Causes & Fixes

#### Slow or Overloaded Server

<details>

<summary>Server takes too long to respond (e.g., due to high CPU/RAM usage or slow scripts).</summary>

* Restart the server to clear up processes.
* Check for heavy scripts causing delays in startup or response.
* Monitor your server CPU/RAM usage.

</details>

<details>

<summary>Bad or infinite loops in resources.</summary>

* Use profiling tools like `txAdmin`'s profiler or `sv_profile 1` in console.

</details>

#### Internet or Routing Issues

<details>

<summary>The client (player) can’t reach the server within the timeout period.</summary>

* Restart router/modem.
* Test with a different network or VPN.
* Try connecting using direct IP (`F8` console → `connect <IP>:30120`).

</details>

<details>

<summary>ISP routing delays or packet loss.</summary>

* Check for packet loss using `ping` or `tracert` or `MTR` to the server IP.
  * See how to do these here: [**Basic Network Troubleshoot**](https://docs.1of1servers.com/1-of-1-knowledge-base/networking-guides/basic-network-troubleshoot)**.**

</details>

<details>

<summary>Port forwarding not set correctly.</summary>

On the servers Windows Firewall, ensure the following Inbound Rules are properly created:

* Ensure **port 30120** (UDP and TCP) are open and properly forwarded.
* Ensure **port 40120** (TCP) is open and properly forwarded.

</details>

#### Misconfigured Reverse Proxy or Nginx/Apache Timeout

<details>

<summary>If using reverse proxies (e.g., Nginx), their timeout settings could be too low or misconfigured.</summary>

* Increase timeout settings like `proxy_read_timeout` in Nginx config.
* Avoid reverse proxies unless absolutely needed for web UI.

</details>

#### DNS Resolution Delays

<details>

<summary>The domain name the server is trying to reach (like for server license checks or endpoints) is slow to resolve.</summary>

* Try using Google's DNS (8.8.8.8 and 8.8.4.4).
* Try using Cloudflare's DNS (1.1.1.1 and 1.0.0.1)
* Flush DNS cache: `ipconfig /flushdns` (Windows).
* On server, edit `/etc/resolv.conf` and set nameserver to 8.8.8.8. (Google) or 1.1.1.1 (Cloudflare).

</details>

#### Client Cache Issues

<details>

<summary>Corrupted client-side cache can stall the request process.</summary>

* Have the player clear their FiveM cache:
  * Close FiveM
  * Go to `%localappdata%\FiveM\FiveM.app\data\cache` and delete everything **except** the `game` folder.

</details>

#### Bonus Tips!

* **Check server logs** (especially startup logs and any long load times).
* Use `curl -v https://cfx.re/join/...` to test response speed manually.
* On the server, try `ping` and `curl` to external services (like `google.com`) to test internet responsiveness.
