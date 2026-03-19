---
description: How to rebuild your VPS and why it may be necessary.
icon: circle-info
---

# Rebuilding VPS

What does rebuilding your VPS mean?

* Rebuilding your VPS wipes all of the data that was hosted on the server. You start completely anew, even without an Operating System.
* You only retain your assigned IP.

Why rebuild your VPS?

* You were hacked,
* There is an issue with your OS/OS image,
* You wanted to change operating systems, or,
* You want to start fresh and wipe the server clean.

There are other reasons, but lets keep it simple!

How to rebuild your VPS

{% stepper %}
{% step %}
### Create a backup of your data

Save all data that you feel is safe (not corrupted or a backdoor for a hacker).

Save the data OFFSITE, we cannot stress this enough, once the rebuild process is complete ALL data is wiped from the server, if you do not have a backup you will lose everything.

Offsite meaning not on the VPS, like: your personal PC, a cloud service like Google Drive or One Drive, etc.&#x20;

DO NOT use the Backup feature on the VPS Dashboard (Premium VPS feature), this will not work because it saves the VPS entirely as is (like a snapshot); including the Operating System image, settings, data, etc.&#x20;

If there is an issue and you use this backup after rebuilding instead of reimporting all safe data that you would have stored offsite, then all the issues you had will simply return, why? Because technically nothing changed.
{% endstep %}

{% step %}
### Click the Rebuild button

On the VPS dashboard, you will see the red Rebuild button.&#x20;

You may have enable the safety to prevent you accidentally clicking this, so disable that by clicking the padlock icon. If it is gold it is enabled, if it is grey then it is disabled.

<figure><img src="../../.gitbook/assets/image (257).png" alt=""><figcaption><p>Rebuild button</p></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (258).png" alt=""><figcaption><p>Safety enabled</p></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (260).png" alt="" width="262"><figcaption><p>Disable safety</p></figcaption></figure>

Then you will proceed with selecting your OS, timezone, etc. (See how in our [quick guide](https://docs.1of1servers.com/vps-servers/gaming-vps-setup/vps.dashboard))
{% endstep %}

{% step %}
### New credentials

Once the VPS is rebuilt your new credentials will be sent via email "Your VPS Server is Ready at 1of1 Servers!".
{% endstep %}

{% step %}
### Reimport all your data (backup from step #1)

If you were hacked, it is your responsibility to ensure that the data you are hosting on the server is safe.&#x20;

We recommend starting fresh and only downloading vetted, trusted, scripts/assets/resources.
{% endstep %}
{% endstepper %}
