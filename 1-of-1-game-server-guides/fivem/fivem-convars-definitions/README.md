---
icon: gamepad-modern
---

# FiveM Convars Definitions

### sv\_showBusySpinnerOnLoadingScreen

{% hint style="info" %}
Hides loading spinner on the loading screen.
{% endhint %}

### sv\_protectServerEntities

{% hint style="info" %}
Block clients from deleting entities created by the server.
{% endhint %}

## set sv\_listingHostOverride https://play.myrpserver.com

{% hint style="info" %}
Replaces the backend end pints to a custom one.
{% endhint %}

## sv\_exposePlayerIdentifiersInHttpEndpoint

{% hint style="info" %}
Server owners who want to retain identifiers on their players.json for backward-compatibility will be able to use the sv\_exposePlayerIdentifiersInHttpEndpoint ConVar.
{% endhint %}

## set sv\_kick\_players\_cnl 0

{% hint style="info" %}
Fixed the error "Connection CNL timed out." on FiveM servers.
{% endhint %}

## sv\_httpHandlerConnectionTimeoutSeconds

{% hint style="info" %}
This configures the connection timeout when a http request handler is running. This is required to prevent the connection from getting closed when the request handler takes longer then the normal connection timeout. Default 5 minutes:
{% endhint %}

## sv\_tcpConnectionTimeoutSeconds

{% hint style="info" %}
This configures the connection timeout in general. This timeout starts each time the connection receives data or is getting data send to. Default 5 seconds (this matches the nodejs timeout).
{% endhint %}

## sv\_forceIndirectListing true

{% hint style="info" %}
The "sv\_forceIndirectListing true" setting in the FiveM server configuration file forces the server to list itself indirectly in the FiveM server browser.

By default, FiveM servers are listed directly in the server browser. This means that players can see the server's IP address and port directly in the browser and can connect to it directly. However, this can be a security risk as it allows attackers to easily discover and target your server.

When "sv\_forceIndirectListing" is set to "true", the server is listed indirectly in the server browser, which means that players cannot see the server's IP address and port directly. Instead, players connect to the server through a proxy server, which helps to protect the server from direct attacks.

Overall, setting "sv\_forceIndirectListing" to "true" can help improve the security of your FiveM server by making it more difficult for attackers to target it directly.
{% endhint %}

## sv\_listingIpOverride "1.2.3.4"

{% hint style="info" %}
The "sv\_listingIpOverride" setting in the FiveM server configuration file specifies the IP address that the server should use when listing itself in the FiveM server browser.

When the server lists itself in the server browser, it includes its IP address so that players can connect to it directly. However, in some cases, the server may have multiple IP addresses or may be behind a NAT firewall, which can make it difficult for players to connect to it.

The "sv\_listingIpOverride" setting allows you to specify a specific IP address that the server should use when listing itself in the server browser. In the example you provided, the setting is set to "1.2.3.4", which means that the server will use this IP address when listing itself in the server browser.

By specifying a specific IP address to use for listing, you can ensure that players can connect to the server even if it has multiple IP addresses or is behind a NAT firewall. This can help make the server more accessible to players and improve its visibility in the FiveM server browser.
{% endhint %}

## sv\_endpoints "1.2.3.4:30120"

{% hint style="info" %}
The endpoint is the address that clients use to connect to the server. When a client connects to the server, it uses the endpoint to establish a connection and exchange data with the server.

By default, the server will use the IP address and port that it is bound to for the endpoint. However, in some cases, you may want to specify a different endpoint for the server to use.\
\
The "sv\_endpoint" setting allows you to specify a different endpoint for the server to use. For example, if your server is behind a NAT firewall and has a different external IP address than its internal IP address, you can use the "sv\_endpoint" setting to specify the external IP address and port that clients should use to connect to the server.
{% endhint %}

## sv\_endpointurl

{% hint style="info" %}
The "sv\_endpointurl" setting is a variation of "sv\_endpoint" that allows you to specify a custom URL for the endpoint. This can be useful if you want to use a custom domain name or URL for your server's endpoint.
{% endhint %}

## sv\_requestParanoia <a href="#sv_requestparanoia-newvalue" id="sv_requestparanoia-newvalue"></a>

{% hint style="info" %}
This helps counter proxy-based HTTP floods. Levels:

* 0: Off. Default behavior.
* 1: Block any IPs sending requests containing a 'Via' header.
* 2: Block any IPs sending requests containing a 'Upgrade-Insecure-Requests' header. This includes all browser-based attempts at requesting .json endpoints, so use with care.
* 3: Also close the socket the requests have been submitted on.

If set to level 2 greater, all requests made to [info.json](https://github.com/citizenfx/fivem/blob/65bf224097b1107c10f84f5dfc25ee8e4bddc95d/code/components/citizen-server-impl/src/InfoHttpHandler.cpp#L276), [dynamic.json](https://github.com/citizenfx/fivem/blob/65bf224097b1107c10f84f5dfc25ee8e4bddc95d/code/components/citizen-server-impl/src/InfoHttpHandler.cpp#L317) and [players.json](https://github.com/citizenfx/fivem/blob/65bf224097b1107c10f84f5dfc25ee8e4bddc95d/code/components/citizen-server-impl/src/InfoHttpHandler.cpp#L331) related endpoints will return "Nope."

\
We recommend setting to 3 to prevent DDoS floods!
{% endhint %}

## sv\_pureLevel <a href="#sv_purelevel-level" id="sv_purelevel-level"></a>

{% hint style="info" %}
&#x20;Console variable used to prevent users from using modified client files. There currently are two pure mode levels (1 and 2), an explanation for these levels can be found below:

* 1: Will block all modified client files except audio files and known graphics mods.
* 2: Will block all modified client files.

If modified files are installed in the FiveM folder, they will be ignored - if users however modified base game files, they will receive an error message telling them what file is modified.
{% endhint %}

## txAdmin

{% hint style="info" %}
The txAdmin menu has a variety convars that can alter the default behavior of the menu.\
Convars configured in the settings page should not be set manually.

#### Settings page only



**txAdmin-menuEnabled**

* Description: Whether the menu is enabled or not. Changing it requires server restart.
* Default: `true`

**txAdmin-menuAlignRight**

* Description: Whether to align the menu to the right of the screen instead of the left.
* Default: `false`

**txAdmin-menuPageKey**

* Description: Will change the key used for changing pages in the menu. This value must be the exact browser key code for your preferred key. You can use [this](https://keycode.info/) website and the `event.code` section to find it.
* Default: `Tab`

**txAdmin-hideDefaultAnnouncement**

* Description: Suppresses the display of announcements, allowing you to implement your own announcement via the event `txAdmin:events:announcement`.
* Default: `false`

**txAdmin-hideDefaultDirectMessage**

* Description: Suppresses the display of direct messages, allowing you to implement your own direct message notification via the event `txAdmin:events:playerDirectMessage`.
* Default: `false`

**txAdmin-hideDefaultWarning**

* Description: Suppresses the display of warnings, allowing you to implement your own warning via the event `txAdmin:events:playerWarned`.
* Default: `false`

**txAdmin-hideDefaultScheduledRestartWarning**

* Description: Suppresses the display of scheduled restart warnings, allowing you to implement your own warning via the event `txAdmin:events:scheduledRestart`.
* Default: `false`

#### Convar only (not in settings page)



**txAdmin-debugMode**

* Description: Will toggle debug printing on the server and client.
* Default: `false`
* Usage: `+setr txAdmin-debugMode true`

**txAdmin-menuPlayerIdDistance**

* Description: The distance in which Player IDs become visible, if toggled on. Note that the game engine limits to show tags that are only closer than \~300m, so increasing the number above that might be useless.
* Default: 150
* Usage: `+setr txAdmin-menuPlayerIdDistance 100`

**txAdmin-menuDrunkDuration**

* Description: How many seconds the drunk effect (troll action) should last.
* Default: 30
* Usage: `+setr txAdmin-menuDrunkDuration 120`

**txAdmin-menuPtfxDisable**

* Description: Determine whether to not play particles effects whenever an admin's player mode is changed.
* Default: `false`
* Usage: `+set txAdmin-menuPtfxDisable true`

**txAdmin-menuAnnounceNotiPos**

* Description: Determines the location of the txAdmin announcement notification. This **must** use one of the following valid positions, `top-center`, `top-left`, `top-right`, `bottom-center`, `bottom-left`, `bottom-right`.
* Default: `top-center`
* Usage: `+set txAdmin-menuAnnounceNotiPos top-right`
{% endhint %}
