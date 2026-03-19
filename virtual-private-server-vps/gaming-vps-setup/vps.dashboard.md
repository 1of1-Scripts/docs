---
description: Server setup, exploring the building blocks of your VPS server
---

# Deploy your Operating System

## Step 3

Now that you have linked your Discord, it's time to build your VPS and complete the setup.

{% hint style="success" %}
Log into your [client area](https://billing.1of1servers.com/clientarea.php?action=products) and click on your Gaming VPS.&#x20;
{% endhint %}

Click on **Manage**, this will take you to a portal where you initially navigate to your VPS Dashboard by clicking **Open Control Panel**.

<figure><img src="../../.gitbook/assets/image (273).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (274).png" alt=""><figcaption></figcaption></figure>

## Step 4

Welcome to the building stage of your VPS where you compile the core building blocks of your server:

{% hint style="success" %}
**Server Name**\
**-** Give your server a name to easily identify it in your account, we recommend your typical username or the name of the project you're currently working on. Don't worry, it can be changed later!
{% endhint %}

<figure><img src="../../.gitbook/assets/Server Name .png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
**Hostname (OPTIONAL)** \
**-** Enter a Hostname, this is optional, **we recommend you skip it!** For easier identification of your VPS on a network, not just on your account (it can be the same as your server name).\
\- Select your Timezone, this is the time that is displayed on your server. \
\
Not to worry, these can also be changed later!
{% endhint %}

<figure><img src="../../.gitbook/assets/Host Name Time Zone.png" alt=""><figcaption><p>Hostname and Timezone Selection</p></figcaption></figure>

{% hint style="success" %}
**Operating System**\
\- Select your desired operating system to be installed with your VPS from the following options:
{% endhint %}

<figure><img src="../../.gitbook/assets/Operating System List.png" alt=""><figcaption><p>Operating System List</p></figcaption></figure>

{% hint style="success" %}
Windows - We **strongly** suggest choosing this option, it provides a **user-friendly** and **seamless** connection process to your VPS through Windows' Remote Desktop.  It also delivers the **most optimal experience** when locally hosting your FiveM city.
{% endhint %}

<details>

<summary>Debian</summary>

This option is recommended for experienced users who are familiar with Linux, and those endeavoring to host websites. It is tried and true and a more stable and flexible Linux option, it is lightweight making it run better than Ubuntu on older hardware, however, the software is older and less user-friendly compared to Ubuntu. **\*Do not** add a Secure Shell (SSH) key if you are unsure of how to use it. See [Creating SSH Key for VPS Install](https://app.gitbook.com/o/5YLMlSyyQwxiSl3dRjE9/s/eumEUQOkJ3WJyd55eMi8/~/changes/276/vps/gaming-vps-setup/remote-desktop-and-ssh-guides/logging-into-vps-with-linux-os/creating-ssh-key-for-vps-install) for how to create SSH key.**\***

</details>

<details>

<summary>Ubuntu</summary>

This option is recommended for experienced users who are familiar with Linux and sudo commands, and those endeavoring to host websites. If you're not confident in using Linux, we advise against selecting this option. **\*Do not** add a Secure Shell (SSH) key if you are unsure of how to use it. See [Creating SSH Key for VPS Install](https://app.gitbook.com/o/5YLMlSyyQwxiSl3dRjE9/s/eumEUQOkJ3WJyd55eMi8/~/changes/276/vps/gaming-vps-setup/remote-desktop-and-ssh-guides/logging-into-vps-with-linux-os/creating-ssh-key-for-vps-install) for how to create SSH key.**\***

</details>

<details>

<summary>Self-Install</summary>

This option enables you to install your own International Organization of Standardization (ISO) file via Virtual Network Computing (VNC). This is not recommended if you are not confident in this topic!

</details>

{% hint style="warning" %}
**Advance Options** - If you are **not** an **experienced** user, please **do not** modify **any settings** within this section.

**Experienced Users**: if you need any other ISO, we have templates available. Please contact us via Discord or open a ticket to request your desired ISO and we will be happy to add it as a template for you!
{% endhint %}

**Example of selecting Windows OS before installation**:

<figure><img src="../../.gitbook/assets/Operating System Windows Example.png" alt=""><figcaption><p>Windows OS Option Example</p></figcaption></figure>

**Example of selecting Debian (identical for Ubuntu) OS before instillation**:

<figure><img src="../../.gitbook/assets/Operating SystemDebian Example.png" alt=""><figcaption><p>Debian OS Option Example</p></figcaption></figure>

4. After clicking "**Install with \[Debian, Ubuntu, Windows]**", a pop will appear to confirm your install option, click "**Install Now**". Example shows installation with Windows 2022.

<figure><img src="../../.gitbook/assets/Install confirmation with OS.png" alt=""><figcaption><p>Install Confirmation with Windows 2022</p></figcaption></figure>

5. You will then be taken to a new page that displays the building progress of your VPN. **Do not touch!** **Allow the process to finish**. (Example shows installation with Windows 2022)

<div data-full-width="true"><figure><img src="../../.gitbook/assets/Build install progress module start to end.png" alt=""><figcaption></figcaption></figure></div>

{% hint style="danger" %}
You will receive an email within 3-5 minutes titled "Your VPS Server is Ready at 1of1 Servers!" that contains your initial login details for your VPS
{% endhint %}
