---
icon: pen-to-square
---

# Discord Bot Setup

{% stepper %}
{% step %}
## Create a Discord bot

Go to the [Discord Developer Portal](https://discord.com/developer/applications) and login.

Create a Discord bot on the Discord bot portal by clicking "New Application" (top right), name the application and click "Create".


{% endstep %}

{% step %}
## Bot Permissions

Go to the **Bot** page of your Discord application.

<figure><img src="../../../../.gitbook/assets/image (211).png" alt="" width="170"><figcaption></figcaption></figure>

In the menu, scroll down to the "Priviledged Gateway Intents" sections and enable the following:

#### Intents

* Presence Intent
* Server Members Intent

<figure><img src="../../../../.gitbook/assets/image (198).png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
## Invite Discord Bot&#x20;

1. Go to the **OAuth2** page of your Discord application.

<figure><img src="../../../../.gitbook/assets/image (194).png" alt="" width="167"><figcaption></figcaption></figure>

2. In the menu, scroll down to URL Generator.

Under OAuth2 URL Generator, select:

* `bot`
* `applications.commands`

<figure><img src="../../../../.gitbook/assets/image (195).png" alt=""><figcaption></figcaption></figure>

#### Bot Permissions

* **`Manage Roles`**
* **`View Channels`**

<figure><img src="../../../../.gitbook/assets/image (196).png" alt=""><figcaption></figcaption></figure>

3. Copy and paste the **generated URL** into your browser’s address bar.

<figure><img src="../../../../.gitbook/assets/image (197).png" alt=""><figcaption></figcaption></figure>

4. Choose the **server (guild)** where you want to invite your bot.
5. Click **Continue**, then follow the remaining prompts to authorize it.

{% hint style="danger" %}
Once the bot joins your server, move its role **all the way to the top** of your role list.
{% endhint %}

{% hint style="danger" %}
All verification bots must be **paused or temporarily removed**.\
\
If the bot gets kicked or removed, you may encounter errors such as **“Guild not found”** or **“Bot is not a member.”**
{% endhint %}

{% hint style="danger" %}
Only the **Discord server owner** can invite this bot. If an admin tries to invite it, the bot will join and then immediately leave more than likely.[](http://127.0.0.1:30120/1of1-webqueue/api/health)
{% endhint %}
{% endstep %}

{% step %}
## Discord Setup Configuration

In the Web Queue Dashboard, go to the Discord Setup menu

<figure><img src="../../../../.gitbook/assets/image (210).png" alt="" width="361"><figcaption></figcaption></figure>

Obtain your newly create Discord Bots Bot Token in the `Bot` tab of the Application in the Discord Developer Portal.

<figure><img src="../../../../.gitbook/assets/image (212).png" alt="" width="170"><figcaption></figcaption></figure>

Click Reset to obtain a new Bot Token.

<figure><img src="../../../../.gitbook/assets/image (199).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../../.gitbook/assets/image (201).png" alt=""><figcaption></figcaption></figure>

Paste the Bot Token into the textbox

<figure><img src="../../../../.gitbook/assets/image (209).png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
## Discord Guild ID

This is the **Discord Server ID** of the server where you’ll be inviting your bot. In most cases, this will be your **RP server**, where players will need a specific role in order to join the queue.

Right-click your servers icon in your Discord Servers List, at the bottom click **Copy Server ID**, paste the ID into the Discord Guild ID text box.

<figure><img src="../../../../.gitbook/assets/image (213).png" alt="" width="163"><figcaption></figcaption></figure>

<figure><img src="../../../../.gitbook/assets/image (214).png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
### Test Connection

Click "Test Connection" If you get a message like below, then you're all set.&#x20;

{% hint style="success" %}
Successfully connected to Discord guild '1of1 Scripts' with bot ID 1437512876565987458
{% endhint %}

<figure><img src="../../../../.gitbook/assets/image (243).png" alt=""><figcaption></figcaption></figure>

Save the Configuration

<figure><img src="../../../../.gitbook/assets/image (215).png" alt=""><figcaption></figcaption></figure>
{% endstep %}
{% endstepper %}
