# FiveM Setup

### Installation Guide

Follow the steps below to properly install and configure the script on your FiveM server.

#### 1. Download & Install

* Download the script.
* Upload it to your server’s `resources` folder (or your preferred custom folder).
* Ensure the resource is started in your `server.cfg`

```cfg
ensure 1of1-prometheus
```

{% hint style="info" %}
Do NOT rename this script or metrics will not be sent. DO NOT ensure this script live. Follow the instructions above.&#x20;
{% endhint %}

#### 2. Configure `server.cfg`

Open your `server.cfg` file and add the following configuration values.

{% hint style="info" %}
⚠️ **Important:** Replace the IP, port, and txAdmin path with your actual server details. Read more below.&#x20;
{% endhint %}

{% hint style="danger" %}
config.lua is encrypted, you don't need anything on there.&#x20;
{% endhint %}

```cfg
# 1of1 Scripts Metrics
set 1of1-ServerIPAndPort "YOUR_SERVER_IP:30120"

# Optional – defaults to "default" if not set
# set txdata_profile "default"

# Set this to your txAdmin default profile folder path
set txdata_path "C:\Path\To\Your\txAdmin\default\Folder"
```

***

### txAdmin Metrics

#### server.cfg

`config.lua` is encrypted, you don't need to change anything there.

#### Create the txData Link

FiveM blocks file access outside the resource folder (due to recent issue on GitHub). You need to create a directory junction once.

**Windows** (run in Command Prompt):

```cmd
mklink /J "<resource_path>\txdata_link" "<txdata_path>\data"
```

**Linux:**

```bash
ln -s <txdata_path>/data <resource_path>/txdata_link
```

**Example:**

```cmd
mklink /J "C:\txData\QBCore_ABC123.base\resources\[qb]\1of1-prometheus\txdata_link" "C:\txData\default\data"
```

To find your resource path, run in the server console:

```
path 1of1-prometheus
```

#### Restart

```
ensure 1of1-prometheus
```

Console should show:

```
[1of1 Prometheus] txAdmin data linked successfully via txdata_link/
```

The junction only needs to be created once. If you move your server or txData folder, re-create it.

***

#### 3. Restart Your Server

After saving your changes, restart your FiveM server to apply the configuration.

***

If everything is configured correctly, the metrics script should now be fully operational.
