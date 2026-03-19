---
description: Logging into your VPS using a Linux OS
---

# Logging into VPS with Linux OS

If you chose to install either Debian or Ubuntu OS on your VPS and have located your login credentials via the email from 1of1 Severs titled "Your VPS Server is Ready at 1of1 Servers!", please proceed to the next steps.

{% hint style="info" %}
### If your personal computer is equipped with the Linux Operating System, follow these steps to log in to your VPS:
{% endhint %}

{% stepper %}
{% step %}
Log in to Your VPS by inputting the following command:



`ssh -i ~/.ssh/id_rsa username@your_vps_ip`

**Replace**:

* `~/.ssh/id_rsa` with the path to your private key (as previously mentioned to save in a safe place for later, which is now).
* Look for files named `id_rsa` (private key) and `id_rsa.pub` (public key). If these exist:
  * **Private Key Path**: `~/.ssh/id_rsa`
  * **Public Key Path**: `~/.ssh/id_rsa.pub`
* If you&#x20;
* `username` with your VPS username (found in the email with your credentials)
* `your_vps_ip` with your VPS's IPv4 address (found in the email with your credentials)
{% endstep %}

{% step %}
Run the command in step #1 with the correct information filled in.
{% endstep %}

{% step %}
Enter the password provided in your email when prompted to do so
{% endstep %}
{% endstepper %}

{% hint style="info" %}
### If your personal computer is equipped with Windows OS, follow these steps to log in to your VPS:
{% endhint %}

{% stepper %}
{% step %}
Ensure OpenSSH is installed, the client is built into Windows 10/11.&#x20;

Open PowerShell and enter this command:

`ss -V`

\*If not installed, go to **Settings > Apps > Optional Features** and add "OpenSSH Client."\*
{% endstep %}

{% step %}
Log in to your VPS

Open PowerShell or Command Prompt and enter this command:

`ssh -i C:\path\to\your\privatekey username@your_vps_ip`

Replace:

* `C:\path\to\your\privatekey` with the path to your private key (e.g., `C:\Users\YourUser\.ssh\id_rsa`).
* `username` with your VPS username (found in the email with your credentials)
* `your_vps_ip` with your VPS's IP address (found in the email with your credentials)
{% endstep %}

{% step %}
Run the command in step #2 with the correct information filled in.
{% endstep %}

{% step %}
Enter the password provided in your email when prompted to do so.
{% endstep %}
{% endstepper %}

{% hint style="success" %}
**Congratulations**! If all steps were followed, all i's were dotted and t's were crossed, you would now be successfully logged into your VPS Server!
{% endhint %}

{% hint style="info" %}
To Disconnect or Logout:&#x20;

* You can simply click the "X" on the blue taskbar at the top of your screen, or;
* You can follow the same process as shutting down your computer and click the Windows logo at the bottom left of your screen and click "Disconnect".
{% endhint %}

### Additional Resources

Your new powerful VPS has been set up. We <mark style="color:red;">**strongly**</mark> recommend taking a look at the following guides to help you understand a lot of the options we offer.

* [Product Addons](../../../../1-of-1-knowledge-base/general-knowledge/product-addons.md)
* [Server Transfer](../../../../dedicated-servers/dedicated-server-additional-guides/server-transfers-guide-for-fivem-dedicated-servers.md)
* [Authorized Users](https://docs.1of1servers.com/1-of-1-knowledge-base/customer-guides/adding-developer-access)
* [Opening Ports](../../../../1-of-1-knowledge-base/network-guides/opening-your-windows-ports.md)

### Please Note:

{% hint style="danger" %}
Do not use VNC to access your server for work.&#x20;

\
No, By default, your username is Administrator.\
\
Your VPS password is the one you received in your email. If you need to reset it, follow the instructions provided [here](https://app.gitbook.com/s/gKTFt9mGD7H32xa7OmD1/).\
\
<mark style="color:red;">**We do not provide support for any FiveM related scripts or issues.**</mark> \
\- Please note that we do not provide support for any FiveM related scripts or issues. We kindly ask that you refrain from requesting assistance with game-related issues within your VPS.\
\- Our support services are strictly for server-related concerns, including issues such as difficulty connecting to Remote Desktop, lack of internet connection, and slow internet speed.
{% endhint %}
