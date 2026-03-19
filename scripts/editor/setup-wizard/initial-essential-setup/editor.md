---
icon: pen-to-square
---

# FiveM API Configuration

{% stepper %}
{% step %}
## Webqueue Login

Navigate [here](https://waitqueue.com/) and log in using your Discord account, authorize the login and proceed to the dashboard.

{% hint style="danger" %}
The link above is for **you only** (our Tebex customer), not your players. Your players should use either the **free URL** shown at the end of the install, or **your custom domain** if you’ve set one up.

Don’t share the [`https://waitqueue.com`](https://waitqueue.com/)link with your players. That link is admin-only and meant just for you.
{% endhint %}
{% endstep %}

{% step %}
## API URL:&#x20;

Enter the FiveM API Configuration menu.

<figure><img src="../../../../.gitbook/assets/image (171).png" alt=""><figcaption></figcaption></figure>

This URL should use **your server’s IP** and **your FiveM port**, with `http://` in front of it.

For example, if your server IP is `145.15.14.14` and your port is `30121`, then your API URL will be:

`http://145.15.14.14:30121`<br>

<figure><img src="../../../../.gitbook/assets/image (187).png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
## API Key:

`1of1webqueue_api_key` is your **secret API key**, set in your `server.cfg` in the previous step.\
Make sure you **changed it to your own secure value** and are not using the default from the docs.&#x20;

<figure><img src="../../../../.gitbook/assets/image (193).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../../.gitbook/assets/image (188).png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
## Test Connection

Everything is working correctly — you’re ready to continue to the next step.

{% hint style="success" %}
Successfully connected to FiveM API (Status: 200)[](http://127.0.0.1:30120/1of1-webqueue/api/health)[](http://127.0.0.1:30120/1of1-webqueue/api/health)
{% endhint %}
{% endstep %}
{% endstepper %}

<figure><img src="../../../../.gitbook/assets/image (269).png" alt=""><figcaption></figcaption></figure>
