---
description: Common Remote Desktop Connection Errors
icon: circle-info
---

# Remote Desktop Connection Errors

## Remote Desktop Connection (RDP)

One of the most common issues happens with the RDP program on windows, the tool you use to remotely log into your server(s).&#x20;

You will run into the following error message:

<figure><img src="../../.gitbook/assets/image (232).png" alt=""><figcaption></figcaption></figure>

This error can occur for a list of reasons including, but not limited to:

<details>

<summary>Your VPS Server was only just built and is still establishing a connection.</summary>

* Allow 5-30 minutes, and try again
* If the error message still appears, proceed to the following

</details>

<details>

<summary>Your VPS Server experienced an issue with the automatic building process.</summary>

* You have now waited up to 30 minutes and tried but failed to connect through RDP with the same error as a result.
* Go to your [VPS Dashboard](https://dashboard.1of1servers.com/) and rebuild your VPS

![](<../../.gitbook/assets/image (234).png>)

* Go through the rebuilding process, then attempt to connect through RDP once more (after up to 30 minutes!)

</details>

<details>

<summary>Your VPS Server has been established for a while with no prior issue, but you are experiencing this error randomly.</summary>

* Your VPS Server may simply require a restart! That's right, the reliable "turn it off and turn it back on" method.&#x20;
* Go to your [VPS Dashboard](https://dashboard.1of1servers.com/) and restart your VPS

![](<../../.gitbook/assets/image (235).png>)

* Allow a couple of minutes for the restart, then try your connection again

</details>

<details>

<summary>However unlikely, it is still a possibility that our networks may be having hiccups which could block you from establishing a connection to your server. </summary>

To check on the status of our networks, go to our [Network Status Page](https://status.1of1servers.com/), find your servers location on the list and verify the network status in real time.

</details>
