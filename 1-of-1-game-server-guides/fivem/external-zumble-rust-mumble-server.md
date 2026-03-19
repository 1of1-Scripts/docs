---
description: >-
  An external Mumble server that runs your voice artifact for players to talk in
  game.
icon: gamepad-modern
---

# External Zumble/Rust Mumble Server

[**Zumble**](https://github.com/AvarianKnight/rust-mumble), is an alternative Mumble voice system. Also created and maintained by [**AvarianKnight**](https://github.com/AvarianKnight).

Zumble runs the voice server on a separate machine or VPS, significantly reducing voice lag, robotic audio, and other common issues, making it a must-have for high-population servers.

**This does not replace pma-voice, you still need to have pma-voice ensured on your scripts.**&#x20;

{% hint style="success" %}
### We offer a VPS package to host the Mumble server only at $9.99 per month.

1. **Go** [**here**](https://billing.1of1servers.com/store/bulks/vps-3g-4u-zumble)**, purchase the special service, then;**
2. **Set up the special VPS server within minutes using our quick and painless set up guide found** [**here**](https://docs.1of1servers.com/1-of-1-knowledge-base/vps-servers/gaming-vps-setup)**, or a video guide found below**
{% endhint %}

{% hint style="warning" %}
The Zumble VPS Package has a **3TB/month bandwidth limit,** if you exceed this limit you may **upgrade** to the **8GB-4-BUD VPS** which has **unlimited** bandwidth.

If you need assistance with the upgrade, **reach out via a ticket** and we will happily assist!
{% endhint %}

{% embed url="https://www.youtube.com/watch?t=&v=SGxRcynaTW4" %}
YT Tutorial VPS Set Up
{% endembed %}

#### The following set up guide is for those strictly using <mark style="color:purple;">**Debian OS**</mark>

{% stepper %}
{% step %}
## Install Git

**Install Git:**

```bash
sudo apt install git -y
```
{% endstep %}

{% step %}
### Install Zumble

#### I**nstall and set up Rust-Mumble**:.

```bash
git clone https://github.com/1-of-1-Servers/setup-rust-mumble.git && cd setup-rust-mumble && chmod +x setup_rust_mumble.sh && sudo ./setup_rust_mumble.sh
```
{% endstep %}

{% step %}
## FiveM Server Setup

#### Open Ports&#x20;

On the server that is hosting your FiveM Server make sure that you have opened port 55500 for both TCP/UDP and for incoming and outbound connections.

#### server.cfg Changes

Make sure that you remove all convars in your server.cfg that relates to voice and replace them with these and ONLY these:

```lua
setr voice_useNativeAudio true
setr voice_useSendingRangeOnly true
setr voice_defaultCycle "GRAVE"
setr voice_defaultVolume 0.3
setr voice_enableRadioAnim 1
setr voice_syncData 1
setr voice_externalAddress YourVoiceServerIPAddressHere
setr voice_externalPort 55500
setr voice_hideEndpoints 1
```

Replace "YourVoiceServerIPAddressHere" with the IPv4 address, do not add quotations ("") or (''). Ex:

```
setr voice_externalAddress 123.456.789.1
```
{% endstep %}

{% step %}
### Optional: Restart Zumble service periodically

**Set up a cron job to automatically restart the script whenever the FiveM server reboots.**\
This helps mitigate a known issue with Zumble where the service can become unresponsive after exceeding the maximum client limit. To prevent this, schedule periodic automatic restarts ideally triggered during server reboot to reduce the likelihood of this occurring and ensure continued stability.
{% endstep %}
{% endstepper %}

<figure><img src="../../.gitbook/assets/image (246).png" alt=""><figcaption><p>Success installation of the script</p></figcaption></figure>

{% hint style="danger" %}
**We do not offer any support other than what is found on this guide. Please do not ask us for any support or open tickets about this, they will be auto closed.**
{% endhint %}

#### Credits:&#x20;

MajorMayhem - For script setup\
MonkeyWhisper - For making script setup pretty\
[AvarianKnight - Rust-Mumble creator](https://github.com/AvarianKnight/rust-mumble)
