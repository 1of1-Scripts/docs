---
description: How to setup pma-voice in a different server.
icon: gamepad-modern
---

# External pma-voice server

## Who should be setting up an external pma-voice server? &#x20;

This tutorial will show you how to run [pma-voice](https://github.com/AvarianKnight/pma-voice) on a separate server from your main one.&#x20;

* Doing this can improve voice quality and reduce lag, especially with a lot of players online. It can also maintain voice chat stability during DDoS attacks.

{% hint style="info" %}
If you're not hosting at least 60 players or experiencing issues during DDoS attacks, then this guide might not be necessary for you. In that case, setting up pma-voice on a separate server may not be required.
{% endhint %}

### Tutorial

{% stepper %}
{% step %}
### Acquire a new server, separate from your current one

First off, you'll need a new server that's different from the one you're currently using.

* There are several options for this. You could use our [Budget VPS](https://www.1of1servers.com/?filter/search=budget%20vps).
* However, you're not limited to these servers, feel free to use any server of your choosing.
{% endstep %}

{% step %}
### Clean installation of preferred framework

Once you've set up your secondary server, you'll need to install a fresh copy of your preferred framework, whether that's QBCore, ESX, or a standalone version.

The key is to ensure that pma-voice is up and running on this new server.

* This approach is great because it helps avoid compatibility problems or configuration mistakes.
* Make sure you choose a new port other than default, 30120, and use that on the server.cfg of your new server.
{% endstep %}

{% step %}
### Make your server private for the time being

In the server.cfg file of your newly set up server, you can include the following line to keep the server unlisted.

```
sv_master1 ""
```

It might also be a good idea to set your txAdmin to admin-only access, which can help avoid any mix-ups with players attempting to join the wrong server.

* By following these suggestions, you ensure that the server isn't visible in public listings and manage your administrative access to prevent unintended player connections.
{% endstep %}

{% step %}
### Edit your main servers sever.cfg

On your main server, you will edit your server.cfg to the following:

```
setr voice_allowSetIntent 1
setr voice_externalAddress ip_address
setr voice_externalPort 30199
setr voice_hideEndpoints 1
```

Substitute 'ip\_address' with the IP of the server you set up earlier, and ensure that the ports are opened in the firewall for this new server.
{% endstep %}
{% endstepper %}

{% hint style="danger" %}
<mark style="color:red;">**We do not offer any support other than what is found on this guide. Please do not ask us for any support or open tickets about this, they will be auto closed.**</mark>&#x20;
{% endhint %}
