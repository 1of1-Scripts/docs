---
description: Backups dashboard.
---

# Backups

{% hint style="success" %}
We strongly recommend creating backups of your server. Save your precious data, or else you will start from scratch!
{% endhint %}

## Backups

### Backups Creation

Backups are copies of the server's primary disk. Any additional storage that may be attached, will not be included in the backup.&#x20;

You have **2 slots** available to store your backups.

{% hint style="warning" %}
We recommend that you **power down your server** before creating a backup to ensure data consistency on the disk.\
\
**The Budget VPS lineup does not have the Backup feature available**.
{% endhint %}

* To create a backup manually, simply click "**Create Backup Now**", it will automatically create a backup file and store it in one of your two slots available.

<figure><img src="../../.gitbook/assets/Backups info.png" alt=""><figcaption><p>Backups Tab Information &#x26; Creation Options</p></figcaption></figure>

You can also create a Backup Schedule, this way you never forget!&#x20;

* Click "**Schedule**" and proceed to select the frequency of when backups are created (None, Daily, Weekly), then click "**Update**".

<figure><img src="../../.gitbook/assets/Backup Schedule.png" alt="" width="476"><figcaption><p>Backup Schedule</p></figcaption></figure>

{% hint style="info" %}
Please remember that you are responsible for keeping these files somewhere safe (Github, Google Drive, etc)
{% endhint %}

* When a backup is created, a new section will appear that displays the backup's date & time, size, status, and the **Restore** or **Delete** options.&#x20;
  * As backups are created, the current backup files in the slots will be replaced as you go.

<figure><img src="../../.gitbook/assets/Backup created.png" alt=""><figcaption><p>Backup Creeated Section</p></figcaption></figure>

{% hint style="danger" %}
## <mark style="color:red;">KEEP YOUR FILES BACKED UP!!!</mark>

#### <mark style="color:red;">**You are solely responsible for backing up your data at all times, including database files such as Heidi or SQL.**</mark>&#x20;

We have a guide for backing up your database [here](https://app.gitbook.com/o/pbvcYYj6vn0K4v1rZG23/s/gKTFt9mGD7H32xa7OmD1/).

#### <mark style="color:red;">**Use GitHub, Google Drive or any other backup service. Your data is NOT currently protected. Do not rely on our VPS backups, things fail and we do not want you to lose your data.**</mark>&#x20;
{% endhint %}
