---
description: VNC enabling and use
---

# Virtual Network Computing (VNC)

## Virtual Network Computing (VNC)

{% hint style="danger" %}
Please **do not change these settings** unless you are an **experienced or advanced user** or are otherwise **told to do so by a staff of 1of1 Servers.**

**You can do more harm than good.**
{% endhint %}

{% hint style="info" %}
You should only enable this option if you are having issues or need to install using CD/DVD media.
{% endhint %}

* By enabling VNC Access you can:
  * Connect to the server as if you were in front of it
  * Access the Terminal Command Prompt instead of using SSH
  * Detect and fix server unavailability issues
  * Install or reinstall the OS using a custom image

{% embed url="https://youtu.be/rc6i8IkljaM" %}
VNC Tutorial
{% endembed %}

* Start by clicking to the Options tab on the VPS Dashboard.
* Then "**Enable VNC Access**", you can see that the current status is "Disabled"

<figure><img src="../../.gitbook/assets/VNC Access Enable.png" alt=""><figcaption><p> VNC Access</p></figcaption></figure>

{% hint style="warning" %}
VNC access is over an unencrypted connection. An attacker suitably positioned to view the network traffic could record and monitor your activity.
{% endhint %}

* Once enabled, the status will reflect the change (top right). By clicking "**Browser VNC**"  a terminal will open where you can manually customize your server beyond our dashboard's settings.

<figure><img src="../../.gitbook/assets/VNC Enabled.png" alt=""><figcaption><p>VNC Access Enabled</p></figcaption></figure>

* If you want to paste into the VNC, use the clipboard feature. This will input your commands directly to the server.

<figure><img src="../../.gitbook/assets/image (118).png" alt=""><figcaption><p>Clipboard Feature</p></figcaption></figure>
