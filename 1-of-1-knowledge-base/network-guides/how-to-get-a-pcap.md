---
description: A brief tutorial on how to get a pcap using  Wireshark.
icon: circle-info
---

# How to get a pcap

Wireshark is a helpful tool for capturing network traffic in real-time. \
\
It helps us identify and diagnose issues more clearly, such as which ports are causing problems or analyzing data packets, including their source, destination, protocol, and content.\
\
We have put together an easy tutorial on how to use Wireshark, you can following in video format or documentation format below!

{% embed url="https://youtu.be/9BJ4pZflytI" %}
Wireshark pcap Tutorial
{% endembed %}

{% stepper %}
{% step %}
### Download & Install Wireshark

In the majority of cases, you will only need to use this tool when having issues connecting to your server through RDP.&#x20;

* Go to the [Wireshark website](https://www.wireshark.org/download.html) and click "Download" on the top navigation bar.

<figure><img src="../../.gitbook/assets/image (225).png" alt="" width="486"><figcaption></figcaption></figure>

* Locate the "Stable Releases: 4.4.2" list and select [Windows x64 Installer](https://2.na.dl.wireshark.org/win64/Wireshark-4.4.2-x64.exe).

<figure><img src="../../.gitbook/assets/image (226).png" alt="" width="563"><figcaption></figcaption></figure>

* Open the .exe file.
* A prompt will appear asking if you would like Wireshark to make changes to your device, simply click "Yes".
* The installer .exe will open, click "Next", read through their TOS and select "Noted", then continue to click "Next" until you are presented with "Install", click it then wait for the program to install.
* Click "Next" then "Finish"
{% endstep %}

{% step %}
### Capturing & Recording Network Traffic

You have now installed Wireshark, now how do you use it?

* Open the program
* A prompt will open for admin-mode, always click "Yes".
* You will be presented with the following:

<figure><img src="../../.gitbook/assets/image (227).png" alt="" width="563"><figcaption></figcaption></figure>

* In the filter textbox, write: host \[your server IPv4 address]
* Proceed to double-click the network connection you are using \[typically Wifi if you are not using an ethernet cable].
* A new window will open for the recorder that is capturing the network traffic.

<figure><img src="../../.gitbook/assets/image (228).png" alt="" width="375"><figcaption></figcaption></figure>

* After this step with the recorder open, attempt the task that is causing problems.&#x20;
  * If it is connecting to your server, attempt to connect through RDP.
* After you have attempted the task that is causing problems, like attempting to connect to your server through RDP, allow about 5 seconds, and then click the red square "Stop" button on the top left corner.

<figure><img src="../../.gitbook/assets/image (229).png" alt=""><figcaption></figcaption></figure>

* Click "File" and "Save as", name the file and click "Save".

<figure><img src="../../.gitbook/assets/image (230).png" alt="" width="563"><figcaption></figcaption></figure>

Send us the saved .pcapng file in your ticket.
{% endstep %}
{% endstepper %}

You can now open the file and view the network traffic, protocols that were run, and their sources and destinations.

Problems will be identified and highlighted in red for when a protocol fails, this is what we are looking for to resolve!
