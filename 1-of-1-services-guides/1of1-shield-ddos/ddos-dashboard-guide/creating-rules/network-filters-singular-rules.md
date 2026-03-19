# Network Filters (Singular Rules)

### Network Filters

After you have set up and applied the base filters above, or if you would like to create rules one at a time, go to "**Create Network Filters**".

<figure><img src="../../../../.gitbook/assets/image (264).png" alt=""><figcaption><p>Manage Filters - Create Network Filters</p></figcaption></figure>

You will have the following settings:

{% tabs %}
{% tab title="Protocol" %}
* **TCP**&#x20;

**(Transmission Control Protocol)** – A connection-based protocol that ensures data is sent and received correctly. It’s reliable but slightly slower due to error checking

**OR**

* **UDP**

**(User Datagram Protocol)** – A connectionless protocol that sends data quickly without checking if it arrives. It’s faster but less reliable, games and streaming services primarily use this protocol.
{% endtab %}

{% tab title="Rules" %}
**Rule 2 options will change based on which Rule 1 you select**

Rule 1 options:

* Game Filters
* Network Filters

<figure><img src="../../../../.gitbook/assets/image (265).png" alt=""><figcaption><p>Network/Game Filters Options</p></figcaption></figure>

**Rule 2 options IF - Network Filters**

* &#x20;FiveM L7 TCP Only&#x20;
* FTP
* Syncookies
* Synproxy
* Drop
* Pass

**Rule 2 options IF - Game Filters**

* FiveM Synproxy
* Fivem
* Fivem Syncookies
* Fivem Experimental
* The Isle
* Syncookies
* Synproxy
* TxAdmin
{% endtab %}

{% tab title="Port" %}
Any port you need.

Standard for FiveM:

* 30120 (default server port)
* 40120 (txAdmin port)

Other:

* 22 (SFTP/FTP like WINSCP, FileZilla, etc)
* 3306 (Heidi SQL)
{% endtab %}

{% tab title="IP Address" %}
Inputting an IP in this section means that these rules only apply to traffic from that specific IP, so **leave this blank**!

This section is for rules to be applied to one specific IP, so if you are not wanting one particular IP managed by the rule, **then leave this blank**.

If you are wanting players to fly in to your city, then you need 30120 and 40120 to be open to all IPs, if you input an IP to this section no one else will be able to connect except the IP that you put in.
{% endtab %}
{% endtabs %}

Once you have input the above information, click "**Add**".

<figure><img src="../../../../.gitbook/assets/image (39).png" alt=""><figcaption><p>Add button</p></figcaption></figure>

Example: Adding a Network Filter for WINSCP

<figure><img src="../../../../.gitbook/assets/image (266).png" alt=""><figcaption><p>Example, adding filter for WINSCP</p></figcaption></figure>

{% hint style="danger" %}
Remember that **when you create and apply/add any new rules/filters to your game ports (ex. 30120), then all players will be dropped** if your server is currently online.
{% endhint %}

{% hint style="success" %}
Removing rules does not drop players.&#x20;
{% endhint %}
