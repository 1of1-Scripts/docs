---
description: How to run two servers in one machine.
icon: gamepad-modern
---

# Two Servers in One

{% stepper %}
{% step %}
### Duplicate your server to create a "dev server"

* Make an exact copy of the server files that you'll be using for your dev server.&#x20;
* You can make an exact copy by just duplicating your current files from your live server, to make sure everything matches.&#x20;
{% endstep %}

{% step %}
### Modify your ports

* Open your new server files that you duplicated server.cfg and edit your TDC and UCP to "0.0.0.0:30121".&#x20;
* This is going to be the default port for your developer server for FiveM.
{% endstep %}

{% step %}
### Change your new servers license key

* Change your license key so it's not the same as your main server and add it to the new server.cfg file.
{% endstep %}

{% step %}
### Create a batch file to run the new "dev server"

We need to create a batch file in order to run the new server:

1. Create a new **Notepad** document and click the top result to open the text editor.
2. Type the following lines in the text file to create a batch file:

{% code overflow="wrap" lineNumbers="true" fullWidth="true" %}
```
@echo off
"C:\QBCoreDev//FXServer.exe" +set serverProfile "dev_server" +set txAdminPort 40125
pause
```
{% endcode %}

3. Keep in mind that you need to replace "C:\QBCoreDev" to where you currently have your FXServer.exe file for the server that you duplciated and as you can see above, the port is 40125 for txAdmin.
4. Save as and enter devserver.bat
5. Save to Desktop and run it to get started deploying your server files.&#x20;
{% endstep %}

{% step %}
### Install txAdmin on your server

* Follow the prompts to install txAdmin on your new dev server.
* If txAdmin says that ports are in use already, just try a different port.&#x20;
* You will need to open ports 40125 and 30121 to allow people to connect. If you need help on how to open your FiveM, [follow this guide.](../../../1-of-1-knowledge-base/network-guides/opening-your-windows-ports.md)
* You may also want to run a different database other than your main one, remember to rename it on server.cfg.
* Keep in mind that since this is a developer server, it's going to be using your database for your live server. I'd recommend just exporting your current database, then importing it under a different name so that there's nothing wrong with your current one.&#x20;
{% endstep %}
{% endstepper %}

{% hint style="danger" %}
This is the SAFEST WAY to run a dev server. If you do not know how to Virtualize your server, we offer installation of it, [click here to order it, is called "Virtualization".](https://billing.1of1servers.com/cart.php?gid=addons)&#x20;
{% endhint %}

{% hint style="danger" %}
We do not offer any support other than what is found on this guide. Please do not ask us for any support or open tickets about this, they will be auto closed.&#x20;
{% endhint %}
