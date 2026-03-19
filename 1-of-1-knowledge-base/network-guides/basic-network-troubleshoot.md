---
icon: circle-info
---

# Basic Network Troubleshoot

## **Tier 1 Troubleshooting Guide**

This guide exists so we can rule out everything else **first**, not to gaslight you or suggest it’s _never_ our fault. We just need to eliminate the most common causes so we can focus on what really matters.

If you've been directed to this guide, it means we need you to do some basic troubleshooting _before_ reaching out to us. Here's why:

We handle **hundreds of support tickets every day**, and truthfully, only a very small percentage of them turn out to be actual network-side issues. So when someone says "a player can't connect" or "something is broken," we take it seriously but also with a grain of salt.

It's not that we don't trust you or want to ignore your problem. W**e're absolutely here to help** but you also need to understand a very simple truth:

> **The internet is not perfect.**

A lot of problems stem from things totally outside of our control: ISPs, regional outages, routing problems, etc. That’s why we ask that you follow the steps below before sounding the alarm.

## **Step-by-Step Troubleshooting Checklist**

**1. Run an MTR from your server to the player’s IP**

* **What’s an MTR?**\
  MTR (My Traceroute) is a network diagnostic tool that combines the functionality of `ping` and `traceroute`. It helps you see where packets are being dropped between your server and another IP (in most cases, your player's IP). [Full guide located here on how to run an MTR.](how-to-run-windows-mtr.md)

**Why it matters:** If there’s packet loss or high latency along the route, it’s a strong indicator the issue is network-related not server-related or our network.

* **How to run Windows MTR:**&#x20;
  1. Download [WinMTR](how-to-run-windows-mtr.md) inside of your server.
  2. Open it and paste the player’s IP.
  3. Click "Start" and let it run for a minute or two.
  4. Look for **packet loss** or **high latency** at any hops.
  5. Take a screenshot and save it for reference.&#x20;
* Example of an ISP issue with packet loss:
  * As you can see below, the player is currently experiencing **14.3% packet loss** between their ISP and the server. This indicates a network issue on their ISP end. To further confirm this, you can ask the player to run an MTR from their system to your server’s IP address (a reverse MTR). This helps verify where the packet loss is occurring and confirms whether it’s an issue on their side or somewhere along the route.

<figure><img src="../../.gitbook/assets/Screenshot 2025-04-01 at 1.41.45 PM.png" alt=""><figcaption></figcaption></figure>

**2. Run a standard traceroute**

*   Open Command Prompt and type:

    ```
    tracert Player's IP
    ```
* This shows you the path data takes to get to the player. Do not stop it, lend it fully complete. If it fails or shows a big delay somewhere in the middle, it’s likely a routing or ISP issue.

**3. Run a pcap:**

**Learn how to run a pcap using Wireshark** [**here**](how-to-get-a-pcap.md)**.**

* Have the player run a pcap while attempting to connect to the server using Wireshark.
* While the player is attempting to connect to the server, also run a pcap directly from inside of your server using Wireshark. This will capture the player's traffic and then we'll be able to compare both.

**4. Ask the player(s) a few questions:**

* Are they using a specific ISP? (e.g. Spectrum, Comcast, AT\&T)
  * Does their IP change dynamically or is it always the same no matter what IP check website they visit? What patterns do you see?&#x20;
* Are multiple players having issues? If so, do they all share:
  * The same **ISP**?
  * The same **region** or country?
* Is their area affected by:
  * **Weather events** (storms, wildfires, etc)?
  * **Outages** (ISP issues, maintenance)?
  * **Satellite-based internet** (which can be unstable)?

If one player is having trouble it’s probably on their end. If multiple players from the same area or ISP are affected it’s likely an ISP, routing issue or it might be an issue with our DDoS protection, who knows, that's why we ask all of these questions.

**5. Change DNS to Google or Cloudflare**

* ISPs sometimes have bad or slow DNS servers. Can be done via Network Adapter settings or router config.
* Recommend they switch to:
  * Cloudflare: `1.1.1.1` and `1.0.0.1`
  * Google: `8.8.8.8` and `8.8.4.4`&#x20;

**6. Disable VPNs / Proxies / Firewall Software**

* Some VPNs or firewalls interfere with connections.
* Ask them to temporarily disable these to test if it helps.

**7. Check for Background Programs Using Bandwidth**

* Apps like Steam, torrents, game launchers, or Windows Updates running in the background can cause connection issues.
* Suggest closing unnecessary apps and monitoring with Task Manager (`Ctrl+Shift+Esc` > Performance > Network).

**8. Use FiveM’s built-in F8 Console**

* Ask them to press `F8` after loading FiveM.
* They can look for messages like:
  * `Could not connect to server`
  * `Timed out after 10 seconds`
  * These logs often include helpful error codes and info to pass along to us. Have the player record a video.&#x20;

**9. Try Another Server**

* If the player is having issues connecting to your server only, but not others, it could still be routing-related.
* If they can't connect to _any_ server, it points more to a FiveM or local/ISP network problem.

**10. FiveM & GTA File Verification**

* Corrupted files can cause crashes or failed connections.
* Ask them to:
  * Verify GTA files via Rockstar or Steam.
  * Reinstall FiveM (or delete the FiveM application data folder).

### **After You’ve Completed All the Steps Above...**

If you’ve gone through **all the troubleshooting steps above**, you should already have a good idea of **where the issue lies** whether it’s the player’s ISP, a routing issue, a regional outage, or something else.

But if you're still stuck and need assistance, **do not just say "it’s broken" or "need help."**\
Instead, open a support ticket and **include everything you’ve gathered** in a **well-formatted and shareable format**.

> ⚠️ **Important:**\
> Do **not** say you've done a step if you haven't. That is **not helpful**, delays support, and especially with network-related issues we will **know** if you didn’t actually run the tests. Be honest, be thorough.

***

#### **What to include in your tickets:**

✅ All the steps you completed from the guide above.\
✅ The **player’s IP address** (for MTR/traceroute checks)\
✅ **Screenshots or videos** of errors or connection attempts.\
✅ The full output/logs from MTR, ping, traceroute, etc.\
✅ Any patterns you noticed (e.g. only players from a certain ISP are affected)\
✅ FiveM console output (`F8` screen) with video or screenshot.

> The **more useful, clear, and complete** your ticket is, the **faster and better** we can help you.

Tickets that just say **"need help no work"** or provide **zero context** will just be rerouted back here.

Example of a well structured and helpful ticket:

> Hi, \
> \
> I have a few players unable to load into the server. We went through all the troubleshooting steps from the guide, including restarting their PC and router, flushing DNS, verifying game files through FiveM and Rockstar, and disabling firewalls, antivirus, VPNs, and proxies, but the issue persists. \
> \
> The affected players' IPs are 75.222.145.69, 83.132.25.52, and 63.62.145.54. \
> \
> I’ve noticed that the issue primarily affects users on Comcast, while players on other ISPs seem unaffected. The problem began around the same time yesterday evening. \
> \
> I've attached MTR and traceroute results along with a video showing the connection attempt and error. \
> \
> Let me know if any additional information is needed.

We never want to dismiss your concerns or make you feel like we're just shifting blame. If the issue is on our end, **we’ll own it** and fix it, no excuses.\
\
We’re always here to help but support is a two-way street. The more effort you put into providing clear and complete information, the faster and more effectively we can assist you.

**We’ll match your effort! I**f you work with us, we’ll work just as hard with you. And if the issue turns out to be on our end, you can rest assured we’ll take responsibility and get it fixed.
