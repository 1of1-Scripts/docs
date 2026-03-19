---
icon: pen-to-square
---

# Server Convars

## **API Key & API Port**

Initial server configuration.&#x20;

```cfg
set 1of1webqueue_api_key "ChangeMeASAPDoNotLeaveMeDefaultOrBadThingsWillHappen"
set 1of1webqueue_api_port "FiveM Port"
```

* `1of1webqueue_api_key`\
  Your secret API key. **Change this immediately** and do not leave it as the default.
* `1of1webqueue_api_port`\
  The port your FiveM server is running on.

***

## **Auth Timeout**

```cfg
set 1of1webqueue_auth_timeout 60
```

How long (in seconds) a player has to join the server after they are marked as “ready” in the web queue. If they don’t connect within this time, they are removed from the queue.\
Default: `60`

***

## **Reject Message**

```cfg
set 1of1webqueue_reject_message "Join our queue at https://waitqueue.com/"
```

Configure the rejection message players see when they try to join the server but aren’t whitelisted, aren’t in the queue, or their queue request was declined.

***

## **Debug Mode**

```cfg
set 1of1webqueue_debug true
```

Enables extra debug logs in the console for txAdmin and our side. Only turn this on if we specifically ask you to enable it for troubleshooting.
