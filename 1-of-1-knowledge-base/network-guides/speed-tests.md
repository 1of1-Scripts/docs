---
description: A quick guide on how to do proper speed test in our servers.
icon: circle-info
---

# Speed Tests

{% hint style="info" %}
Use iPerf to do network speed tests. Google Speed tests & Speedtest.net limit the network speed.
{% endhint %}

{% hint style="success" %}
* Click [here](https://iperf.fr/download/windows/iperf-3.1.3-win64.zip) to download iPerf.
* Extract the zip folder and put it on your desktop.
{% endhint %}

{% hint style="success" %}
* Open the folder where iperf-3.1.3-win64 is.&#x20;
* Click on iperf3 to run the application
* Right click the folder on top
* Click on "Copy address as text"
* Open Command Prompt and type cd and right click.
* Press enter to go to the directory
{% endhint %}

![cd + right click](<../../.gitbook/assets/image (143).png>)

{% hint style="success" %}
Replace IPHere for your server IP.
{% endhint %}

```sql
iperf3 -c YourServerIP
iperf3 -c YourServerIP -R
```



