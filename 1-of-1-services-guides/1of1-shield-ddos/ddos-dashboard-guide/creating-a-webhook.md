---
description: How to create a webhook in the DDoS Dashboard
---

# Creating a Webhook

This Dashboard is only available to those selected to have access, please do not request access as this is currently a Beta testing environment. Thank you for your understanding!

{% hint style="info" %}
If you were not selected to have access to the dashboard, but would like a webhook for your IP, then please create a ticket via your client portal and we will happily set that up for you!\
\
Simply provide us with the webhook URL and Role ID.
{% endhint %}

After going to your IP and clicking the link icon under Webhook, you will be sent to a new page.

### Adding a Webhook

On the top right beside "**Search Webhooks**", click the "**Add New..**." drop-down menu, then click "**Add Webhook**".

<figure><img src="../../../.gitbook/assets/image (40).png" alt=""><figcaption><p>Add webhook button</p></figcaption></figure>

You will be presented with the following options:

{% tabs %}
{% tab title="Name" %}
Typically named "DDoS Attacks", because... why not? :)&#x20;

Keep it simple!
{% endtab %}

{% tab title="URL" %}
The webhook URL for the channel in your Discord server where the notifications will be sent/populate.\
\
How to make a Webhook URL:

* Create a text-channel in your Discord server & go to it's settings

<figure><img src="../../../.gitbook/assets/image (41).png" alt=""><figcaption><p>ddos attacks</p></figcaption></figure>

* Go to "**Permissions**" tab and set it to "**Private**" so only a specific role will access the channel.
  * Do this before creating the Webhook, that way the role is integrated into the Webhook URL.
* Go to the "Integrations" tab

<figure><img src="../../../.gitbook/assets/image (42).png" alt=""><figcaption><p>Integrations</p></figcaption></figure>

* Create a Webhook

<figure><img src="../../../.gitbook/assets/image (43).png" alt=""><figcaption><p>Create Webhook button</p></figcaption></figure>

* Name it appropriately (DDoS Attacks, etc)

<figure><img src="../../../.gitbook/assets/image (44).png" alt=""><figcaption><p>Webhook settings</p></figcaption></figure>

* The role that has permissions to the channel will be pinged with the DDoS attack notification.

Paste the Webhook URL into the textbox in the DDoS Dashboard Webhooks Page.
{% endtab %}

{% tab title="Role ID" %}
The role that has permissions to the channel will be pinged in the DDoS notifications, but you need to copy the role's ID.

Create a new role for the channel, or use a current role to be pinged.

* Go to the **Discord server's settings** and go to "**Roles"**
* **Name** the role accordingly, make the role an **administrator**, **add the role to yourself** and any relevant users (your admins, etc).
* **Save** the role
* Go back to the "**Roles" tab**, click the **3 dots button** to the right of the role.
* Click "**Copy Role I**D"

<figure><img src="../../../.gitbook/assets/image (46).png" alt=""><figcaption><p>Copy Role ID</p></figcaption></figure>

Paste the Role ID into the textbox in the DDoS Dashboard Webhooks Page.
{% endtab %}
{% endtabs %}

The input would look something like this:

<figure><img src="../../../.gitbook/assets/image (19).png" alt=""><figcaption></figcaption></figure>

Once you have input the above information, click "**Add**".

<figure><img src="../../../.gitbook/assets/image (39).png" alt=""><figcaption><p>Add button</p></figcaption></figure>

And you're all set to receive notifications of any attacks on the selected IP!

You are able to use the same webhook information on any additional IP that you are assigned.

### Test Notification

Now that the Webhook would be populated in the Webhook Table, you can send a Test Notification to ensure the webhook was configured correctly. Click the test tube icon on the right-side (see below).

<figure><img src="../../../.gitbook/assets/image (20).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (21).png" alt=""><figcaption></figcaption></figure>

If successful, you should receive a notification within the channel that looks like this:

<figure><img src="../../../.gitbook/assets/image (22).png" alt=""><figcaption></figcaption></figure>

