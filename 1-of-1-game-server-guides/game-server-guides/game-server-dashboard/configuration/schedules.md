---
description: Manage all of this server's schedules in one place
---

# Schedules

The schedules tab allows for commands and power options to be automated, so you are able to enjoy your server in a more hands-free environment!

Schedules and their tasks are directly fed into the console to be executed.

{% hint style="info" %}
This example will use a Minecraft Server. However, the features, functions, and instructions remain the same for other games.
{% endhint %}

The tab displays:

* The schedule's name;
* The number of tasks the schedule contains;
* The schedule's last run/deployment;
* The time-frame for it's next run;
* Buttons to: Manage, Create, or Delete a schedule.

<figure><img src="../../../../.gitbook/assets/image (204).png" alt="" width="563"><figcaption><p>Schedules Tab Overview</p></figcaption></figure>

### Creating a Schedule & Tasks

Let's create a schedule to restart your server every 12 hours.

This can help reduce lag by deleting all particles/dropped items, save the current world and it's contents, and run the diagnostic properties of a boot cycle to repair any underlying issues.

#### To create a schedule:

* Click the "**Create**" button, this will trigger a pop-up window for you to:
  * Name your schedule (example, Squeaky Clean)
  * Set the time-frame parameters (example, every 12 hours every day)
  * Make sure your schedule is enabled by turning on the "**Enable**" toggle button.
    * This makes sure the schedule actually runs, you can disable schedules at any time by editing it and turning this button to the off position.
  * Once every field is filled into your desired parameters, click "**Submit**" to start this schedule.

<figure><img src="../../../../.gitbook/assets/image (205).png" alt="" width="485"><figcaption><p>Create Schedule, example restart every 12 hours</p></figcaption></figure>

Your newly created schedule will appear, you must now add the "**Task(s)**" that will run on this schedule. Our example is to restart the server every 12 hours, the "**Task**" is the restart command.

#### To create a task:

* Click "**Create Task**", this will trigger another pop-up window for you to select the tasks:
  * Action&#x20;
    * Send Power Action/Send Command
  * Time Offset&#x20;
    * The time (in seconds) it may take for the task to execute and run to completion, a restart may take up to 2 minutes, depending on the server size and it's contents.
  * Payload&#x20;
    * The specific action that is to be executed, example: Restart the server.
* Once all the fields are filled, be sure to click "**Submit**" to create your task!

<figure><img src="../../../../.gitbook/assets/image (206).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../../.gitbook/assets/image (207).png" alt="" width="491"><figcaption><p>Power Action Option (ex, Send power action)</p></figcaption></figure>

<figure><img src="../../../../.gitbook/assets/image (208).png" alt="" width="491"><figcaption><p>Payload Option (ex, Restart the server) &#x26; Time Offset at 120 seconds</p></figcaption></figure>

<figure><img src="../../../../.gitbook/assets/image (209).png" alt="" width="487"><figcaption><p>Submit Button</p></figcaption></figure>

There are 2 options for the Tasks Action, Send power action and Send command. We have covered an example for "**Send power action**", but what about "**Send command**"?&#x20;

The "**Send command**" option is a great tool for executing commands on a regular basis like \[/weather clear] or \[/time set day] in Minecraft. Or even for scheduling announcements!

This example will show how to schedule an announcement to be published in the global chat every 30 minutes.

The schedule was created and named "Announcement" with a time of "\*/30\*.

To create the task:

* Click "**Create Task**", this will trigger another pop-up window for you to select the tasks:
  * Action&#x20;
    * This example will use "**Send Command**"
  * Time Offset&#x20;
    * The time (in seconds) it may take for the task to execute and run to completion, an announcement should take 0 seconds.
  * Payload&#x20;
    * The specific action that is to be executed&#x20;
    * Example: /say The best server in the world! Powered by 1of1 Servers.
* Once all the fields are filled, be sure to click "**Submit**" to create your task!

<figure><img src="../../../../.gitbook/assets/image (210).png" alt=""><figcaption><p>Announcement Task Example: Minecraft Server</p></figcaption></figure>

<figure><img src="../../../../.gitbook/assets/image (211).png" alt=""><figcaption><p>Announcement in-game preview</p></figcaption></figure>
