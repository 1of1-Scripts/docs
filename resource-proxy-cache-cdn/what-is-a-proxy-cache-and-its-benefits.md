---
description: A quick crash-course on what a CDN/Proxy Cache is and what is does!
icon: circle-info
---

# What is a Proxy Cache & Its Benefits

A **C**ontent **D**elivery **N**etwork, AKA a **CDN**, AKA a **Proxy Cache**.... is a speedier way to transfer assets by using our databases spread out geographically to cache content much closer to your end users. A CDN will help:

### **Faster Resource Loading & Lower Latency**

A proxy cache/CDN stores static FiveM resources (e.g., textures, models, maps, clothing) closer to the client:

* Reduces the load time for players joining the server.
* Eliminates the need to download the same resources directly from the game server repeatedly.
* Delivers content from nearby edge locations, improving first-time load speeds significantly.

**Impact**: Players experience smoother and faster joins, improving server retention and first impressions.

### **Preloading & Persistent Caching for Frequent Assets**

By preloading common assets:

* Resources like maps, clothes, or vehicles can be cached in a browser-style manner.
* Players don’t have to re-download unchanged assets on every session.
* Smart caching with version control (e.g., file hashes) ensures players always get the right version.

**Impact**: Drastically reduces connection time for returning users and ensures content consistency.

### **Improved Scalability for High Player Counts**

A CDN enables handling large spikes in player connections:

* Allows hundreds of players to download large packs concurrently without degrading performance.
* Avoids bottlenecks at the server level during events or restarts.
* Helps serve regional players with equal performance using global caching nodes.

**Impact**: Keeps server performance stable even during mass player influx or during restarts.

### **Reduced Bandwidth & Server Load**

Offloading downloads to a CDN:

* Prevents the game server from being overwhelmed by resource requests during peak times or DDoS.
* Helps manage bandwidth costs by shifting delivery to an optimized network.
* Avoids resource duplication for every player session, especially with large MLO or clothing packs.

**Impact**: Frees up server resources to handle gameplay logic, leading to better in-game performance.

### FAQ

<details>

<summary>How many locations do you have?</summary>

For our CDN service, we upload and serve your files from over 330 locations globally!

</details>

<details>

<summary>Can I purge my cache in the CDN?</summary>

Yes, you can purge your uploaded cache whenever needed. Additionally, any changes you make will be automatically uploaded.

</details>

<details>

<summary>How can I determine the amount of bandwidth I need?</summary>

You can monitor your bandwidth usage on your VPS or Dedicated Server dashboard. If you need assistance location this information, have a look at these guides:

* [Dedicated Dashboard Server Management & Information](https://app.gitbook.com/o/5YLMlSyyQwxiSl3dRjE9/s/y4MjR46zLIGXhxZNWRvy/)
* [VPS Dashboard Server Management](../virtual-private-server-vps/vps-dashboard/server-management.md)

</details>
