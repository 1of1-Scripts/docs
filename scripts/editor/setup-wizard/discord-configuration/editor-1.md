---
description: >-
  Discord Roles Setup Configure Discord roles and their priority order for queue
  management. Drag roles to reorder them - higher positions get more priority
  points.
icon: pen-to-square
---

# Priority Roles Setup

{% stepper %}
{% step %}
## Priority Roles Setup

Create roles in your Discord Server, such as the ones purchasable via Tebex for higher role priority, these will populate in the Roles selection menu in the WebQueue Dashboard.

Enter the **Priority Roles Setup** menu.

<figure><img src="../../../../.gitbook/assets/image (258).png" alt=""><figcaption></figcaption></figure>

Click "**Add Roles**" to configure the priority for roles for the queue system.

<figure><img src="../../../../.gitbook/assets/image (259).png" alt=""><figcaption></figcaption></figure>

Select the roles you created in your Discord server for the web queue, then click "**Add Selected**"

<figure><img src="../../../../.gitbook/assets/image (260).png" alt=""><figcaption></figcaption></figure>

{% hint style="warning" %}
**Points on the roles are stackable!**
{% endhint %}

{% hint style="success" %}
If you just added new roles, go back to the Dashboard and open the **Discord Roles** section again  and your newly created roles will now appear there.
{% endhint %}
{% endstep %}

{% step %}
### Arranging Priority

Once your roles are added, you can drag and drop them to arrange their priority.

More points = higher priority in queue.

<figure><img src="../../../../.gitbook/assets/image (261).png" alt=""><figcaption></figcaption></figure>

### Bypass Privileges

{% hint style="danger" %}
**A role with "Bypass" privileges will be able to bypass all players waiting in the queue, at any time.**&#x20;
{% endhint %}

This is done by reserving a certain amount of slots out of your servers total capacity so that any individual with this, or these, role(s) will be able to join the server.

Example: Moderator (staff role)

Enter the amount of bypass slots to be reserved at all times (average amount of active staff, example). Our example will reserve 5 slots of the total 48 slots available for our server.

<figure><img src="../../../../.gitbook/assets/image (263).png" alt=""><figcaption></figcaption></figure>

Enable the "Bypass" toggle on the role in the list. Our example will be the Moderator role, however you can add multiple roles to this list (ie. Owner role, staff role, etc).

<figure><img src="../../../../.gitbook/assets/image (264).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../../.gitbook/assets/image (265).png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
### Negative Points&#x20;

You can assign **negative points** to a player as a punishment via a role. This pushes them **toward the back of the queue**, making it harder to join during peak/prime time. Negative points simply **offset** their total priority, so if they still have enough positive points from other roles, they’ll be placed accordingly.

**Intended uses:**&#x20;

* **Chargeback penalties (Tebex):** apply negative points to players who charge back.
* **Temporary punishments:** assign a role with negative points for a set period of time.
{% endstep %}

{% step %}
### Express Pass

Enable the Express Pass feature for roles to hop the queue if they miss their queue window. Allow players with a specific role to reclaim their queue position if they disconnect or leave within a time window.

<figure><img src="../../../../.gitbook/assets/image (279).png" alt=""><figcaption></figcaption></figure>

Select the role with this permission and then the reclaim windows (measured in minutes).

Example, a Moderator of the city can reclaim their position within 30 minutes.

<figure><img src="../../../../.gitbook/assets/image (280).png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
#### Save your work!

Configure Discord roles and their priority order for queue management. Drag roles to reorder them. Then click "**Save Configuration**" to save your work!

<figure><img src="../../../../.gitbook/assets/image (266).png" alt=""><figcaption></figcaption></figure>
{% endstep %}
{% endstepper %}
