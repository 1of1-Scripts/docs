---
description: Players stuck on "Downloading server manifest..." when loading into the city.
---

# "Downloading server manifest..."

### **What does** "Downloading server manifest..." mea&#x6E;**?**

Getting **stuck on "Downloading server manifest"** in **FiveM** usually means your client **connected to the server**, but **couldn’t retrieve the list of resources** to download and load. This step is essential — if the manifest fails to load, the game can't proceed to load resources, maps, or scripts.

The **server manifest** is a **JSON** file that lists:

* All the resources (scripts, maps, etc.)
* Resource metadata (version, dependencies)
* Instructions on how to download/load them

If you’re stuck here, something is **blocking or stalling that fetch request**.

### Common Causes & Fixes

#### Resource/Manifest File Corruption

<details>

<summary>A resource has an invalid or missing <code>fxmanifest.lua</code> / <code>__resource.lua</code>.</summary>

Go to the affected resource(s) and check:

* The file is **named correctly** (`fxmanifest.lua` or `__resource.lua`)
* Syntax is clean
* No stray BOM (Byte Order Mark) at the top — use a clean text editor like VS Code or Notepad++
* Run `ensure` or `start` on only a few resources and test — isolate the problematic one.

</details>

<details>

<summary>Incorrect file encoding or syntax error in the manifest.</summary>

Go to the affected resource(s) and check:

* The file is **named correctly** (`fxmanifest.lua` or `__resource.lua`)
* Syntax is clean (especially for `fxmanifest.lua`)
* No stray BOM (Byte Order Mark) at the top — use a clean text editor like VS Code or Notepad++

</details>

#### Client-Server Communication Timeout

<details>

<summary>Your client (player) is trying to connect but the server is too slow or blocked.</summary>

* Restart router/modem.
* Switch networks (e.g., use hotspot or VPN to test).
* Disable firewall
* Try connecting using direct IP (`F8` console → `connect <IP>:30120`).

</details>

<details>

<summary>High latency or packet loss.</summary>

* Check for packet loss using `ping` or `tracert` or `MTR` to the server IP.
  * See how to do these here: [**Basic Network Troubleshoot**](https://docs.1of1servers.com/1-of-1-knowledge-base/networking-guides/basic-network-troubleshoot)**.**

</details>

<details>

<summary>The server is not properly reachable on required ports/out allowing HTTP/UDP traffic.</summary>

On the servers Windows Firewall, ensure the following Inbound Rules are properly created:

* Ensure **port 30120** (UDP and TCP) are open and properly forwarded.
* Ensure **port 40120** (TCP) is open and properly forwarded.

If all is correct, create a ticket inquiring if there are rules on your IP, only **AFTER** following and providing **all information** within the [**Basic Network Troubleshoot**](https://docs.1of1servers.com/1-of-1-knowledge-base/networking-guides/basic-network-troubleshoot) **guide.**

</details>

#### **Incorrect or Incomplete `server.cfg`**

<details>

<summary>You haven’t <code>ensure</code>'d all required base resources, or a broken script is referenced.</summary>

Clean up your `server.cfg`:

* Comment out all custom `ensure` lines.
*   Test with only core resources like:

    ```cfg
    ensure mapmanager
    ensure chat
    ensure spawnmanager
    ensure sessionmanager
    ensure hardcap
    ensure baseevents
    ```
* Re-enable resources one by one to find the problem.

</details>

#### Corrupted Cache

<details>

<summary>Broken cache files on the client prevent proper communication.</summary>

Have the player clear their FiveM cache:

* Close FiveM
* Go to `%localappdata%\FiveM\FiveM.app\data\cache` and delete everything **except** the `game` folder.

</details>

#### Mismatched or Outdated Artifacts

<details>

<summary>Old FXServer build, artifacts, or client not synced with current FiveM version.</summary>

* Make sure your client is updated (FiveM auto-updates, but check manually if needed).
* Update your server:
  * Download latest FXServer artifacts.
  * Rebuild or update all resources to match modern standards.
* Have player running same version of FiveM/GTAV as your server.
  * Have the player verify their game files (FiveM & GTAV)

</details>

#### Bonus Tips!

* Check **txAdmin console** or `run.cmd` logs for errors.
* Use **developer console (F8)** on client to see where it gets stuck.
* Temporarily **whitelist your IP** on all firewalls/security settings.
