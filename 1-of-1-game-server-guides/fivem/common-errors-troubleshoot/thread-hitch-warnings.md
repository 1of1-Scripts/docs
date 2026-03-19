---
description: Seeing multiple thread hitch warnings in your FiveM console.
---

# Thread Hitch Warnings

### What Is a Thread Hitch in FiveM?

A **thread hitch** occurs when a specific part of the FiveM server (called a “thread”) **takes too long to process its tasks**. These threads are responsible for different aspects of the server — like game logic, entity syncing, networking, etc.

### What Does a Thread Hitch Mean?

FiveM’s server runs on a **tick-based system**, where every thread is expected to complete its work within a small window of time (typically \~16ms for smooth performance, matching 60 FPS logic). If a thread **exceeds this expected time**, a **hitch warning** appears in the console.

#### **What a Hitch Means (In Practical Terms)**

> "This part of the server is taking too long to finish its job, and it's slowing everything else down."

It’s similar to a lag spike in a game — but instead of a player’s FPS dropping, the **server’s brain stalls**, affecting everyone connected.

### Common Symptoms of a Thread Hitch:

* It creates **lag** or **delayed server response**.
* May cause **rubberbanding** for players.
* Leads to **poor synchronization** of vehicles, peds, or events.
* If frequent or severe, can even crash the server.

### Hitch Types You'll See in Logs

* `sync thread hitch` – delay in syncing game entities (vehicles, peds, players)
* `network thread hitch` – delay in sending/receiving network data
* `server thread hitch` – delay in core server logic (scripts, events, DB, etc.)
* Generic: `Hitch warning: frame time of Xms` – overall stall affecting multiple threads

Lets dive into more detail in the table below:

### 3 Kinds of Thread Hitch Warnings

{% tabs %}
{% tab title="Server" %}
**What is a Sync Thread Hitch?**

This is the **core logic loop** of the FiveM server.\
**Console msg:**

```
"Thread hitch warning: server main thread took Xms"
```

**Common Causes:**

* Badly optimized server-side scripts.
* Heavy MySQL sync calls inside player events.
* Resource loading issues

**Fix Tips:**

* Switch to `MySQL.Async`.
* Audit `server.cfg` for bloated or broken scripts.
* Profile performance (`sv_profile 1`, `resmon`).
{% endtab %}

{% tab title="Network" %}
**What is a Network Thread Hitch?**

This thread deals with **sending/receiving data packets** between the server and clients.

**Console msg:**

```
"Thread hitch warning: network thread took Xms"
```

**Common Causes:**

* Laggy or unstable network connections (usually client-side).
* Server under DDoS or packet flood.
* Too much real-time data being sent (e.g. custom voice/data streaming).
* Server NIC misconfiguration (rare).

Fix Tips:

* Reduce real-time network-intensive scripts.
* Check server host firewall or router.
* Monitor for abuse (anticheat tools like txAdmin’s player monitoring help).
{% endtab %}

{% tab title="Sync" %}
**What is a Sync Thread Hitch?**

If your **FiveM console log** shows **many "sync thread hitch warnings"**, that means parts of the server (especially the main game thread or resource threads) are **lagging or stalling** — usually due to heavy or poorly optimized server-side scripts.

FiveM's **sync thread** is an **internal logic thread** that:

* Handles **game entity synchronization**: peds, vehicles, player states, objects.
* Hitches here usually mean that **scripts or in-game conditions** are choking the logic loop.
* Syncs player/entity data
* Runs server-side game logic
* Manages resources/scripts

If this thread takes too long to complete a "tick," you get a **hitch warning** — which means **your scripts, resources, or in-game activity are stalling the server loop**, **not** that the server hardware is failing.

**Console msg:**

```
"Thread hitch warning: sync thread took Xms"
```

**Common Causes:**

* Too many entities (especially unoptimized AI, props, or cars).
* Server-side scripts doing heavy processing.
* Overuse of server events with lots of players.
* Loops that don’t yield enough (`Wait(0)` abuse).

**Fix Tips:**

* Clean up unused entities.
* Optimize loops with longer waits.
* Move expensive logic to client where safe.
* Use `resmon` and `sv_profile` to find culprits.
{% endtab %}
{% endtabs %}

### Common Causes & Fixes

#### Heavy or Unoptimized Scripts

<details>

<summary>Bad loops, too many server events, or frequent database queries.</summary>

Use profiling to find heavy scripts:

* Run `resmon 1` in console to show resource CPU usage.
* Use `sv_profile 1` and check logs for usage spikes.
* Avoid tight loops or unnecessary server triggers.
* Offload frequent operations to **client-side** if possible.

</details>

<details>

<summary>Scripts using <code>Citizen.Wait(0)</code> too often in <code>server.lua</code>.</summary>

Optimize scripts:

* Replace `Citizen.Wait(0)` with longer waits (`100–1000ms`) unless it needs real-time speed.
* Avoid tight loops or unnecessary server triggers.
* Offload frequent operations to **client-side** if possible

</details>

#### Too Many Entities to Sync

<details>

<summary>Massive number of <strong>peds</strong>, <strong>vehicles</strong>, or <strong>objects</strong> being streamed/synced at once.</summary>

Common in servers with custom mapping, AI traffic, or jobs that spawn lots of props/NPCs.

* Limit unnecessary vehicle/ped spawning.
* Use `SetEntityNoCollisionEntity`, `SetEntityAsNoLongerNeeded`, or `SetEntityInvisible` for unneeded entities.
* Remove unused props/objects using `DeleteEntity` when no longer needed.

</details>

#### Database Bottlenecks (MySQL Async)

<details>

<summary>Scripts using <strong>MySQL queries</strong> inside real-time loops or server events.</summary>

Server waits on slow DB response = sync hitch.

* Use **MySQL-Async** properly:
  * Avoid queries in tick events or loops.
  * Use `MySQL.Async.fetchAll(...)` and cache data if needed.
* Optimize your SQL database (indexes, cleanup).

</details>

#### Long Tick Handlers

<details>

<summary>Server-side <code>Citizen.CreateThread</code> blocks main thread for too long.</summary>

Review any server-side `threads` and space out workloads:

**Instead** of:

```
while true do
    -- heavy logic
    Citizen.Wait(0)
end
```

**Do**:

```
while true do
    -- lighter logic
    Citizen.Wait(500)
end
```

</details>

#### Resource Loading Delays

<details>

<summary>Slow or bloated resources taking long to load during join or restart.</summary>

* Compress textures and map files.
* Move static data client-side when possible.
* Use `ensure` order in `server.cfg` to load key resources first.

</details>

#### Too Many Unused Resources Running

<details>

<summary>You're running 50+ scripts, many of which might be unused but still consume CPU</summary>

* Disable or remove unused or test scripts.
* Group utility scripts together (e.g., use one "utils" or "core" script instead of many separate).

</details>

#### Bonus Recommended Debug Tips!

* **Use `resmon 1` or `sv_profile 1`** while players are active to see heavy resources.
* **Restart the server** and gradually re-add resources to see which causes the hitch.
*   Enable `onesync` correctly in your `server.cfg`:

    ```cfg
    onesync on
    ```

    (Or use `onesync legacy` or `onesync infinite` depending on your setup.)
