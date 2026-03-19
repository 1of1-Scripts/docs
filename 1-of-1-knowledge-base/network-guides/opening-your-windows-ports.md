---
description: Opening your ports so players can connect to your new city.
icon: circle-info
---

# Opening your Windows Ports

{% hint style="success" %}
We have created a YouTube tutorial to help with this process! Found here:&#x20;
{% endhint %}

{% embed url="https://www.youtube.com/watch?t=&v=XneD8zhHOYw" %}

{% hint style="success" %}
Specifically FiveM ports, found here:&#x20;
{% endhint %}

{% embed url="https://youtu.be/XneD8zhHOYw?si=nYsMS8gENFapa-zc&t=190" %}

### Default Ports

If you are using non-default ports, make sure to open the specific ports you have configured.

{% hint style="warning" %}
30120 - To allow players to join your server.&#x20;
{% endhint %}

{% hint style="warning" %}
40120 - You may skip opening this port. This port allows your admins to connect to txAdmin using [http://YOUR.SERVER.IP.HERE:40120/](http://your.server.ip.here:40120/)
{% endhint %}

### Inbound Rules

{% hint style="success" %}
1. Navigate to Control Panel, System and Security and Windows Defender Firewall.
2. Select Advanced settings and click on Inbound Rules in the left pane.
3. Right click Inbound Rules and select New Rule.
4. Select Port > TCP > Specific Local Hosts > 30120 and click Next.
5. Select a New Role and repeat all the steps but for port 40120 under a different rule.&#x20;
{% endhint %}

<figure><img src="../../.gitbook/assets/image (104).png" alt=""><figcaption><p>New Rule - TCP </p></figcaption></figure>



{% hint style="success" %}
1. Select Allow the connection in the next window and hit Next.
{% endhint %}

<figure><img src="../../.gitbook/assets/image (124).png" alt=""><figcaption><p>Allow Connection</p></figcaption></figure>

{% hint style="success" %}
1. Select the network type as you see fit (you can leave as default) and click Next.
2. Click Next again.&#x20;
3. Name the rule something meaningful such as FiveM and click Finish.
4. <mark style="color:red;">**Repeat the same steps above**</mark> but instead of selecting TCP on Step 4, <mark style="color:red;">**select UDP**</mark>.
{% endhint %}

{% hint style="info" %}
We have certain limitations in place on default ports, allowing only ports 30120 and 40120 due to our DDoS protection measures.<br>

<mark style="color:red;">**PRIOR TO SUBMITTING A SUPPORT TICKET:**</mark> \
Take the initiative to open the desired ports on your firewall and check for any restrictions. Some IPs might not have restrictions due to earlier rules set in place.<br>

If there's a need to unblock additional ports, don't hesitate to submit a ticket to us. _**Please ensure to detail the specific ports you wish to open, whether you require TCP or UDP, and the rationale behind needing these ports open.**_<br>

Be aware that we will inquire about this information, which could seem annoying. Therefore, ascertain that the request made aligns with your actual needs. Opening ports indiscriminately, thinking that both UDP and TCP are necessary, could make your system vulnerable to potential DDoS attacks. Our role includes preventing such scenarios from happening.
{% endhint %}
