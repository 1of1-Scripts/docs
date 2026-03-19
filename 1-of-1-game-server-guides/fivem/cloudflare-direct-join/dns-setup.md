# DNS Setup

#### Step 1: Add an A Record

1. Navigate to the **DNS** section of your domain registrar or Cloudflare dashboard.
2. Create a new **A Record** with the following details:
   * **Type:** A
   * **Name:** `play` (or any subdomain you prefer)
   * **IPv4 Address:** Your server's IP address (e.g., `123.45.67.89`)
   *   **Proxy Status:** You may need to **disable proxying (DNS Only)** to allow FiveM connections.

       > ⚠️ _Disabling the proxy will expose your server IP. If you're using our DDoS protection, it's safe to do so._
3. Click **Save**.

***

#### Step 2: Add an SRV Record

This SRV record allows users to connect without typing the port number.

1. Create a new **SRV Record** with the following configuration:
   * **Type:** SRV
   * **Name:** `play.yourdomain.com` (e.g., `play.projectsloth.org`)
   * **Service:** `_cfx`
   * **Protocol:** `UDP`
   * **TTL:** Auto
   * **Priority:** `10`
   * **Weight:** `10`
   * **Port:** `30120` (or your server’s custom port)
   * **Target:** `play.yourdomain.com`
2. Click **Save**.

***

#### Final Step: Connect Using Your Custom Domain

Once both records are set:

* Players can now connect using your custom URL (e.g., `play.projectsloth.org`) instead of a raw CFX or IP address.

> _Please allow 2–4 hours for DNS propagation before the connection works globally._

{% hint style="danger" %}
We do not offer any support other than what is found on this guide. Please do not ask us for any support or open tickets about this, they will be auto closed.&#x20;
{% endhint %}
