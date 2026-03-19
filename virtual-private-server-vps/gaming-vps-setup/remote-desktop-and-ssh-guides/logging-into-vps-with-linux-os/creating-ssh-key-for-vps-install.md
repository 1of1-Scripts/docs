---
description: Creating an SSH Key for Debian or Ubuntu OS Install on VPS
---

# Creating SSH Key for VPS Install

If you are looking to install the Debian or Ubuntu OS on your VPS, you will need an SSH key. When you select your desired Debian or Ubuntu OS, a section will appear called SSH Keys.&#x20;

<figure><img src="../../../../.gitbook/assets/SSH Key Add.png" alt=""><figcaption><p>SSH Key Section, Add Key</p></figcaption></figure>

1. **Select "Add Key"**&#x20;

* If you already have an SSH Key, enter it in the box titled "Public Key", give the key a name or click Random Name, the key will be saved under this identifier for future use (in the cases of restarts, rebuilds, etc).

<figure><img src="../../../../.gitbook/assets/SSH Key enter.png" alt=""><figcaption></figcaption></figure>

* If you do not have an SSH Key, click the Generate Key Pair option. This option will generate you a SSH Key at no additional cost.
  * RSA2 is the most compatible Key Type for most systems, it is secure but is a larger Key Size at 4096 bit.
  * ED25519 is the most secure, it is less compatible with Linux OS dating older than V 6.5 or systems from 2014. It is a smaller Key Size at 2048 bit, faster, and extremely secure.
  * OpenSSH is the most standard and secure Format, only select PuTTY if you are confident and familiar with it.
* Select your preferences, **ensure you have added a Name**, then click "**Generate**"
* Example with RSA2, 4096 bit, OpenSSH

<figure><img src="../../../../.gitbook/assets/SSH Generate.png" alt=""><figcaption><p>Generating SSH Key</p></figcaption></figure>

2. After clicking "**Generate**", the key that is created will automatically paste into the **Public Key Box**.&#x20;

**There is a Private Key generated as well, copy (click the clipboard icon beside "Private Key") and save in a safe place for later steps.** \
Key file path for Private Key based on your local machine's OS:

* **Windows**: Save it in `C:\Users\YourUser\.ssh\id_rsa` or another secure location.
* **Linux**: Save it in `~/.ssh/id_rsa`.

3. Click "**Save**" to proceed with the installation process.

<figure><img src="../../../../.gitbook/assets/SSH Generate Result.png" alt=""><figcaption><p>Generated Key Pair Results</p></figcaption></figure>

4. Once saved, your new key will appear as an option to select. **Select your desired key** and click "**Install with \[Debian or Ubuntu**]"

<figure><img src="../../../../.gitbook/assets/Selecting SSH key Install.png" alt=""><figcaption><p>Install with Debian or Ubuntu</p></figcaption></figure>

5. The following steps after clicking "**Install with \[Debian or Ubuntu]**" are standard, they can be found in the [Deploy Your Operating System Page](https://app.gitbook.com/o/5YLMlSyyQwxiSl3dRjE9/s/eumEUQOkJ3WJyd55eMi8/~/changes/276/vps/gaming-vps-setup/deploy-your-operating-system) at step #4.
