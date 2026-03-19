---
icon: shield
---

# txAdmin Proxy Cloudflare

## Secure txAdmin with Cloudflare Tunnel

This guide walks you through setting up a **Cloudflare Tunnel** for `txAdmin` so that you can safely expose your admin panel without revealing your IP address, helping prevent DDoS attacks.

### Requirements

* A domain added to your Cloudflare account.
* A FiveM server (VPS or dedicated).
* Cloudflared downloaded and installed on your VPS or dedicated server.

***

{% embed url="https://youtu.be/yir_2CE1iNI" %}
txAdmin Tunnel Tutorial
{% endembed %}

***

### Step 1: Setup Your Domain on Cloudflare

1. Make sure you have a domain in your Cloudflare account.
2.  Go to the Cloudflare dashboard and navigate to:

    ```
    Account Home > Zero Trust > Networks > Tunnels
    ```

{% hint style="warning" %}
If you haven’t set up a Zero Trust team before, you’ll be prompted to create one. You can name it after your RP server, for example, “1OF1 RP” or something similar. When asked about payment, just select the free plan, which includes 50 seats, more than enough for your needs.
{% endhint %}

***

### Step 2: Configure a Cloudflare Tunnel

1. Click **"Add a Tunnel"**.
2. Choose **Cloudflared** as the tunnel type.
3. Name the tunnel (e.g., `txadmin` or any name you prefer).

<figure><img src="../../.gitbook/assets/image (25).png" alt=""><figcaption></figcaption></figure>

***

### Step 3: Install Cloudflared

Download the `cloudflared` binary directly to the VPS or dedicated server your FiveM server is running.&#x20;

* Latest Windows binary [here](https://github.com/cloudflare/cloudflared/releases/latest/download/cloudflared-windows-amd64.exe).
* Alternate download options directly from Cloudflare located [here](https://developers.cloudflare.com/cloudflare-one/connections/connect-networks/downloads/).

***

### Step 4: Run the Tunnel

1. Open **Command Prompt** as Administrator.
2.  Use the `cd` command to navigate to the folder where **Cloudflared** was installed. By default, this is likely:

    ```
    C:\Program Files (x86)\cloudflared
    ```

    Your command might look like:

    ```cmd
    C:\Users\Administrator> cd "C:\Program Files (x86)\cloudflared"
    ```

    Once you're in the directory, your prompt should look blow, awaiting the copy/paste from Cloudflare.

    ```cmd
    C:\Program Files (x86)\cloudflared>
    ```

<figure><img src="../../.gitbook/assets/image (261).png" alt=""><figcaption><p>Preview of CMD</p></figcaption></figure>

3. Copy and paste the command shown in your Cloudflare dashboard to authenticate the tunnel and connect it to your account.

***

### Step 5: Configure Tunnel Routing

During setup:

* **Subdomain:** `txadmin`
* **Domain:** Select from your Cloudflare-managed domains.
* **Service Type:** `http`
* **URL:** `localhost:40120`

{% hint style="danger" %}
**Security Tip:** It’s strongly advised **not to use the default port `40120`** for txAdmin. Instead, choose a random, non-standard port to help protect against automated scans and potential exploits.&#x20;

***

#### Set Custom txAdmin Port&#x20;

To change the port txAdmin uses, set the following environment variable in your batch script:

```batch
set TXHOST_TXA_PORT=40125
```

This ensures txAdmin will bind to TCP port `40125`.\
For full documentation on environment variables and advanced configuration, visit the official [txAdmin docs](https://github.com/citizenfx/txAdmin/blob/master/docs/env-config.md).

Whatever port you choose to use, make sure that it is CLOSED on your firewall.&#x20;
{% endhint %}

This forwards traffic from `txadmin.yourdomain.com` to your local txAdmin panel.

***

### Step 6: Deploy and Access

Once deployed, your txAdmin panel will be securely accessible at:

```
https://txadmin.yourdomain.com
```

<figure><img src="../../.gitbook/assets/image (26).png" alt=""><figcaption><p>Custom Subdomain</p></figcaption></figure>

***

### Done!

You now have a secure way to manage your FiveM server using txAdmin without exposing your public IP address.

{% hint style="danger" %}
We do not offer any support other than what is found on this guide. Please do not ask us for any support or open tickets about this, they will be auto closed.&#x20;
{% endhint %}
