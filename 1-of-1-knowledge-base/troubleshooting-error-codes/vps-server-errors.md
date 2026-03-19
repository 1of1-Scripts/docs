---
description: Common VPS Server Errors
icon: circle-info
---

# VPS Server Errors

### VPS Server

<details>

<summary>Your VPS Server is crashing intermittently with the message "System is shutting down"</summary>

* When logged into your VPS through RDP, look in the bottom right corner of the virtual desktop.
* If it says the "Windows Licence has expired" or anything similar to that effect, do the following:
  * Launch a command prompt and input the command: slmgr /rearm
  * After receiving a confirmation message, reboot your VPS

![](<../../.gitbook/assets/image (236).png>)

* Once the VPS is operational again, verify the Windows License on the bottom right corner of the screen; it should display as valid for a period of 180 days or the message should not be present.

</details>
