# Game Filters (Batch Rules)

## Game Filters for FiveM City

* On the main page, go to "Manage IPs" in the "Overall Management" drop down menu.
* Click "Manage" on the top right and select "Create Filters", enter your IP into the search bar that appears and hit Enter.
* On the top right beside "**Manage Presets**", click the "**Manage Filters**" drop-down menu, then click "**Create Game Filters**".

<figure><img src="../../../../.gitbook/assets/image (263).png" alt=""><figcaption><p>Manage FIlters - Create Game Filters Button</p></figcaption></figure>

Once inside the new page to create game filters, you will see many settings. **DO NOT PANIC**!

* We have made the **default settings that appear to be the best standard filters for DDoS attacks**.&#x20;
  * If you need to make changes to the default ports, just do that here for each (i.e. you're using a different set of port(s) than 30120 &/or 40120).&#x20;
  * Once you have made the changes (if necessary),
* Scroll down and enable the UDP Holepunch setting.
* The click "**Create**".

<figure><img src="../../../../.gitbook/assets/image (36).png" alt=""><figcaption><p>Create</p></figcaption></figure>

{% hint style="danger" %}
Unless instructed by our team, do not modify the default rules. Only adjust the ports for your server—nothing else.
{% endhint %}

{% hint style="danger" %}
When you "**Create**" filters, **all players will be dropped from your server and must all reconnect again**.&#x20;

If you **delete** filters, **players are not dropped**, this is only when you create new filters and apply them.

This is so the firewall is able to filter the traffic according to all rules that have been applied, not just the past rules that were presently active prior to the newly applied rules.&#x20;
{% endhint %}

* Once you click "**Create**", the filters will automatically be applied.&#x20;
