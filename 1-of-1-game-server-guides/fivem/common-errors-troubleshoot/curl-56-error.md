---
description: CURL 56 Error code
---

# CURL 56 ERROR

The dreaded CURL 56 Error code... where to begin?

### **What is CURL 56?**

**CURL error code 56** in **FiveM** typically indicates a **failure in the network connection** between your game client and the server.&#x20;

* CURL is a tool used by FiveM to handle network requests.
* **Error 56 message**:&#x20;
  * "Failure with receiving network data."

This can happen due to a number of issues on either the client-side or server-side, so buckle in!

Now, **before coming to us**, please gather **all the information** using our [**Basic Network Troubleshoot**](https://docs.1of1servers.com/1-of-1-knowledge-base/networking-guides/basic-network-troubleshoot) guide. CURL 56 is a beast of its own, and it's best you come prepared so we have all the information to find a quick resolution to get your players back in your city.

Below is just to provide some context and simple DIY solutions on yours/your players end:

### Server-Side Issues

#### **Causes & Solutions:**

<details>

<summary>VPS/Dedicated Server is offline or not responding.</summary>

* Check if the server is online&#x20;
  * Try other players joining, or ping the IP using RDP
* Restart the server or VPS.

</details>

<details>

<summary>Misconfigured DDoS Filters/Firewall Rules.</summary>

* Verify server firewall (ensure port `30120` is open).
* Open a ticket to verify your DDoS protection (filter configuration).
  * Along with all the info from the [**Basic Network Troubleshoot**](https://docs.1of1servers.com/1-of-1-knowledge-base/networking-guides/basic-network-troubleshoot) guide.

</details>

<details>

<summary>Some custom scripts or resources may stall the server or cause improper HTTP responses.</summary>

* Disable custom scripts one-by-one and check.
* Validate resource manifest files and endpoints.

</details>

<details>

<summary>Hosting provider issues.</summary>

* Go through the [**Basic Network Troubleshoot**](https://docs.1of1servers.com/1-of-1-knowledge-base/networking-guides/basic-network-troubleshoot) guide prior to reaching out.
* Check our [Status Page](https://status.1of1servers.com/) to verify there are no outages or planned maintenance.&#x20;

</details>

#### Bonus Tips for Server-Side Issues

* Check if your **FXServer** has any recent console errors.
* Verify your FXServer artifacts are up-to-date.
* `netstat -an | find "30120"` on server to confirm listening port.
* Use `ping`, `tracert`, or `MTR` tools to test packet loss or route failure.
  * See how to do these here: [**Basic Network Troubleshoot**](https://docs.1of1servers.com/1-of-1-knowledge-base/networking-guides/basic-network-troubleshoot)**.**
* `curl -v https://yourserverurl` in terminal to test handshake/debug.

### Client-Side Network Issues

#### **Causes & Solutions:**

<details>

<summary>Internet Service Provider (ISP) is blocking or dropping packets</summary>

* Restart your router.
* Switch to a different network or use mobile hotspot to test.
* Try connecting using direct IP (`F8` console → `connect <IP>:30120`).

</details>

<details>

<summary>ISP is throttling or restricting specific ports.</summary>

* Use a VPN to bypass ISP restrictions.
* Run a pcap & connect to the FiveM server
  * See how to do these here: [**Basic Network Troubleshoot**](https://docs.1of1servers.com/1-of-1-knowledge-base/networking-guides/basic-network-troubleshoot)**.**

</details>

<details>

<summary>Corrupted game cache or files.</summary>

* Clear FiveM cache:
  * Go to `%localappdata%\FiveM\FiveM.app\data\cache` and delete everything **except** the `game` folder.
* Verify GTAV/FiveM files.

</details>

<details>

<summary>Outdated game version, or mismatched version compared to server.</summary>

* Reinstall or update FiveM.
* Use same game version as the server.

</details>

#### Bonus Tips for Client-Side Issues

* Whitelist FiveM in Windows Firewall or antivirus.
* Try connecting using direct IP (`F8` console → `connect <IP>:30120`).
