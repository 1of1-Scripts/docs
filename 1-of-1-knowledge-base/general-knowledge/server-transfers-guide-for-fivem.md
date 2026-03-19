---
description: >-
  Here's how to prepare your previous server files for transfer to our hosting
  company.
icon: circle-info
---

# Server Transfers Guide for FiveM

{% hint style="danger" %}
<mark style="color:red;">**Please note this service is only offered to NEW customers with Dedicated Server purchases only.**</mark> \
<mark style="color:red;">**You can handle everything yourself and don't need to wait for us to transfer your server. This guide is only for those who want us to transfer their server on their behalf.**</mark>

\ <mark style="color:red;">**Do NOT**</mark> miss any steps or bullet point from this guide. Read it carefully and follow the instructions on here.
{% endhint %}

Thank you for choosing us as your hosting provider! This guide is only if you have existing files. If you're installing a fresh copy of a framework you don't need to follow this (along with the stipulations above).

If you choose to use our services to transfer your files over, below is a quick guide on how to get your server files ready to be moved over. This guide is assuming you're moving from a VPS or a dedicated server.\
\
**We do not provide any FiveM related support or issues. Should any errors arise post-transfer, it is NOT our duty to fix them. You'll be responsible for addressing any non-functional scripts or those that might malfunction/break during the transfer.**

{% hint style="info" %}
If you're transferring from a hosting company that you only have access via File Zilla or WinSCP. Please create a ticket through your client portal so we can assist you!

Provide us all of your FTP information.&#x20;

Along with sending us your FTP information in the ticket, send us the following manually:

* myLogo file (your server logo)
* server.cfg file
* Your database
{% endhint %}

### Gathering your server files

* Create a folder named resources and get all of your resources into that folder. <mark style="color:red;">**Do not add cache or server artifacts**</mark>**,** only resources.&#x20;
* Add server.cfg file to the resource folder.&#x20;
* Add myLogo file (your server logo) to the resource folder.
* Export your SQL and add it to the resource folder. You may do this later if your server is still live to reduce any data loss from your current players

{% hint style="success" %}
To export your SQL via Heidi:<br>

* Select your database you want to export.&#x20;
* Right click it and click on Export database as SQL
* Make sure Database and Table "Create" boxes are checked. **DO NOT CHECK "DROP".**&#x20;
* In Data drop down menu, select Insert.
* Create a filename and location choose the export location by clicking the folder button.
* Click Export on the bottom.
{% endhint %}

<figure><img src="../../.gitbook/assets/image (32).png" alt=""><figcaption><p>HeidiSQL Export Settings</p></figcaption></figure>

{% hint style="success" %}
To export your database from phpMyAdmin.<br>

* Go to the database you want to export
* Click on "Export" should be between "Query" & "Import".&#x20;
* Scroll all the down down and click on "Export"
* Add that file to your resource folder.
{% endhint %}

* Right click on your resource folder and zip it/rar it.
* Upload the rar/zip resource folder to Google Drive, Dropbox, One Drive or any other sharing services you use.&#x20;
* Open a ticket in your client portal and share your files with viewable/download access with the team with a link.

{% hint style="info" %}
Please note that if you permit us to proceed with this setup, our sole responsibility is to transfer or provide a fresh framework installation.\
\
We can assist with the transfer of your server files from your previous host or install the framework upon request. These services are extended as a courtesy, but note that any subsequent errors post-transfer will be your responsibility to address and fix.&#x20;



Owing to the way much of the data is stored, particularly in many game servers sourced from FTP, you're likely to face some errors. This is especially true for encrypted scripts or scripts that are dependent on js or html.
{% endhint %}

#### How To Make a FiveM Server with QBCore or QBox | 2025 | Beginner's Guide

{% embed url="https://www.youtube.com/watch?ab_channel=1of1Servers&v=6jdfc99IlXc" %}

