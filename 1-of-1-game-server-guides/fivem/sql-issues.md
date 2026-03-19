---
description: A quick rundown of a few issues you can encounter on SQL.
icon: circle-info
---

# SQL Issues

### SQL Error (2013)

{% hint style="danger" %}
Error:

SQL Error (2013): Lost connection to server during query Notice: You can disable the "Stop on errors in batch mode" option to ignore such errors"
{% endhint %}

{% hint style="success" %}
Solution:

Fix: Run this query in your HeidiSQL query-tab
{% endhint %}

```sql
SET GLOBAL max_allowed_packet=1073741824;
SET GLOBAL wait_timeout = 3500;
SET GLOBAL net_read_timeout = 3500;
SET GLOBAL connect_timeout = 3500;
```

{% hint style="info" %}
After you're done importing the file, run this other query to revert back to default.
{% endhint %}

```sql
SET GLOBAL max_allowed_packet=1073741824;
SET GLOBAL wait_timeout = 600;
SET GLOBAL net_read_timeout = 600;
SET GLOBAL connect_timeout = 600;
```

{% hint style="danger" %}
We do not offer any support other than what is found on this guide. Please do not ask us for any support.&#x20;
{% endhint %}
