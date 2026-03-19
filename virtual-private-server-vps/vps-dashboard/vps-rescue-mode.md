---
description: >-
  Rescue Mode is a feature integrated into the VPS Dashboard, it's designed to
  help you troubleshoot and fix issues with your VPS.
---

# VPS Rescue Mode

### What is Rescue Mode?

> Rescue Mode boots a minimal operating system independent of the server's main disk. \
> \
> It's designed to help you troubleshoot and fix issues such as boot failures, misconfigurations, or corrupted filesystems. \
> \
> Once your issue is resolved, you can disable rescue mode and the server will return to its standard operating environment.
>
> \
> This is an amazing tool if you run into the Blue Screen of Death, were hacked, or your VPS is facing other issues rendering it inaccessible or inoperable.

{% hint style="warning" %}
This feature requires you to know the basics of Linux, or you may use an SFTP program like FileZilla or WinSCP.

Please note that these are third-party applications and therefor fall outside of our scope of support, you will need to operate these independently.
{% endhint %}

### How to use Rescue Mode

{% stepper %}
{% step %}
### Go to the VPS Dashboard

**in the Home Page of your client portal, c**lick **View Details** on your VP&#x53;**.**

<figure><img src="../../.gitbook/assets/image (7).png" alt="" width="563"><figcaption></figcaption></figure>

Select **Open Control Panel.**

<figure><img src="../../.gitbook/assets/image (8).png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
### Go to the Options Tab

Click on the Options tab in the VPS Dashboard on the navigation bar.

<figure><img src="../../.gitbook/assets/image (9).png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
### Initiate a Rescue Mode Session

In the **Options** tab, click the **Create Rescue Session** button, _there is no need to select a rescue system as only Linux (Debian Live) Rescue V1 is available._

Creating a **Rescue Session** will essentially boot the server with a Debian operating system that is directly attached to the disc of your server so that you can access the core systems of the server even as it is inaccessible or inoperable.

<figure><img src="../../.gitbook/assets/image (10).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (11).png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
### Accessing the Rescue Session login credentials

Once the session is activated, you will receive an email containing your SSH login credentials to log into the session.&#x20;

* These are **temporary credentials** only valid for this Rescue Session and its duration, once the session is **disabled/closed** these credentials (username/password) will become **invalid** and you will return to using your **original credentials** to connect via RDP as you've done previously.

Go to your email inbox and search for an email titled **Rescue Session Activated.** Your credentials will be provided within this email.&#x20;

<figure><img src="../../.gitbook/assets/image (12).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (13).png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
### Logging in

You may login via SSH command with the credentials, if you have an SSH program. Or you may use the console within the VNC of your VPS on the Dashboard.

This documentation will demonstrate logging in using the **VNC console** on the VPS Dashboard, to enable and access VNC please view the [VNC guide](virtual-network-computing-vnc.md) and return here when it has been enabled.

* Open the VNC window, you will see that is now a command prompt environment. For the following lines, enter:

> `Rescue login: root`\
> `Password:` _enter the password provided in the email, the characters will be **invisible** as you type and the **underscore will not move**, this is **normal**! Simply hit **Enter** once you have finished typing the password._

If successful, the section <mark style="color:blue;">**Rescue System ENV v1.1**</mark> will populate.

<figure><img src="../../.gitbook/assets/image (14).png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
### Available tools & System info Options

The **Available tools** <mark style="color:green;">`rescue-tools`</mark> option will open a catalogue of tools at your disposal to troubleshoot, diagnose, and treat your server to repair it.&#x20;

* You can also simply pull all your files from the disc to your own PC using the lftp or sftp command (see below), then rebuild the VPS to start anew and import your files back to the VPS using the SFTP program.

<figure><img src="../../.gitbook/assets/image (15).png" alt=""><figcaption></figcaption></figure>

The System info tool <mark style="color:green;">`rescue-info`</mark> will enable the user to install any software temporarily on the server using `apt.` commands.

<figure><img src="../../.gitbook/assets/image (16).png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
### Ending a Rescue Session

Once you have completed all that you need to do, and your system is recovered or on the way to a speedy recovery, and you are finished with the rescue session:

* Go back to the VPS Dashboard,&#x20;
* Click **End Rescue Session** on the banner, or the button within the Options tab,
* Then confirm the task by clicking **End Rescue Session** again in the pop-up modal.

{% hint style="warning" %}
Note that anything that you have installed or added when within the Rescue Session (such as installed software) will be deleted once the session has ended, only modifications to the system/server itself will remain the same (such as OS updates, firewall rules, etc).
{% endhint %}

<figure><img src="../../.gitbook/assets/image (17).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (18).png" alt=""><figcaption></figcaption></figure>
{% endstep %}
{% endstepper %}
