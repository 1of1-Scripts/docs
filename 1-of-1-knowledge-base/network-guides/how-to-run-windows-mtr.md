---
description: How to run a Windows MTR.
icon: circle-info
---

# How to run Windows MTR

1. **Download**: Grab the Windows MTR tool from [here](https://sourceforge.net/projects/winmtr/).
2. **Extract**: Unzip the files and navigate to `WinMTR_x64`.
3. **Launch**: Double-click on `WinMTR.exe` to open it.
4. **Run the MTR. Depending on what is needed, client to server or server to client or both.**&#x20;
   1. **client to server (player to server) to be ran from the player's PC.**
      1. In the "Host" field, type in your VPS/dedicated server IP. Then hit **Start**.
   2. **server to client (server to player) to be ran inside of the VPS/dedicated server.**
      1. In the "Host" field, type in your player's public IP (IPv4). Then hit **Start**.
5. **Wait**: Allow it to run for about 30 seconds before clicking **Stop**. See below for MTR preview.&#x20;

<figure><img src="../../.gitbook/assets/image (275).png" alt=""><figcaption></figcaption></figure>

6. **Export**: After stopping, click on **Export HTML**. Save this file.
7. **Share**: Share the HTML file with the team.



