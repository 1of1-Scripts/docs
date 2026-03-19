---
icon: pen-to-square
---

# Custom Domain

{% hint style="danger" %}
This guide assumes you already own a custom domain (for example, `myrpserver.com`).&#x20;

Do **not** buy a separate domain like `yourrpserver-queue.com` (or anything similar). Since you’ll be using a **subdomain**, you don’t want two different domains like that.

If you **don’t** have one yet, no problem. You can purchase a domain from [**1of1 Servers here**](https://billing.1of1servers.com/cart.php?a=add\&domain=register) or any domain provider you prefer.

Once you have your domain, come back to this page and follow the steps below to complete the setup.

A free domain is provided during this setup, more info below.
{% endhint %}



{% stepper %}
{% step %}
## Add your domain in the panel

In the **Custom Domain** section, enter the **subdomain** you want to use (without `http://` or `https://`) and save it.

{% hint style="danger" %}
You must use a **subdomain**. We do **not** support connecting on a root domain.

Example: `queue.yourdomain.com` (supported)

Not: `yourdomain.com` (not supported)
{% endhint %}

&#x20;Subdomain only, such as:

```
queue.yourdomain.com
```

<figure><img src="../../../../.gitbook/assets/image (247).png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
## DNS settings

* Log in to your domain registrar (Cloudflare, GoDaddy, Namecheap, etc.).
* Go to the **DNS** management page for your domain.

<figure><img src="../../../../.gitbook/assets/image (246).png" alt=""><figcaption></figcaption></figure>

[](http://127.0.0.1:30120/1of1-webqueue/api/health)
{% endstep %}

{% step %}
## Add the TXT verification record (if shown)

* In the panel, you may see a **TXT record** listed for verification.
* Create that TXT record exactly as shown to prove you own the domain.
{% endstep %}

{% step %}
## Create the CNAME record

* Add a **CNAME** record for the hostname you’re using (for example, `queue` if your domain is `queue.yourserver.com`).
*   Point it to:

    ```
    pages.waitqueue.com
    ```
{% endstep %}

{% step %}
## Wait for DNS to propagate

DNS changes can take up to **24–48 hours** to fully propagate, though it’s often instant.
{% endstep %}

{% step %}
## **Access your landing page**

Once DNS has propagated and the domain is validated, your landing page will be live on your custom domain.

{% hint style="danger" %}
**Note:** SSL certificates are issued automatically by Cloudflare after your domain is verified, so HTTPS will start working without any extra steps from you.
{% endhint %}
{% endstep %}
{% endstepper %}

<figure><img src="../../../../.gitbook/assets/image (245).png" alt=""><figcaption></figcaption></figure>

## Your Landing Page URL

We’ve also provided a **free landing page URL** for you. You can find your unique link at the very bottom of the page, just copy it and share it with your players.

## Final Setup Information

You’ve successfully completed the full setup for your web queue. If you ever need to adjust your configuration, you can do that anytime through our [main domain](https://waitqueue.com/).

To manage your live web queue, including joining the queue, handling applications, reviewing tickets, and everything else you’ll need to log in using **your custom domain** or the **free landing page URL** we provided. Optional convars you can use to further customize your server can be found [here.](../initial-essential-setup/server-convars.md)

For clarity, here’s how roles function within the system:

* **Customer** – This is you, the Tebex purchaser (most likely the server owner). As a customer, you can be a moderator, and player.
* **Moderator** – These are any staff members you assign to view applications and tickets. Moderators are also treated as players.
* **Player** – These are your general community members who use the queue. A player can also be a moderator if given that role.
