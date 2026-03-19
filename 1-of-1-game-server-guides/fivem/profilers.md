---
icon: circle-info
---

# Profilers

### What Is Profiling in FiveM?

Profiling helps you **measure how much CPU time each resource uses**, so you can identify performance-heavy scripts that cause lag or drops in server performance.\
FiveM provides **built-in profiling tools** accessible via the console (F8 or server console).

### Types of Profilers

* Resource Time Profiler - Measures **CPU usage per resource** on the server.
* Client Profiler - Used to profile scripts on the **client side** (useful if a player experiences FPS drops).
* Network Profiler - Monitors **bandwidth usage** for each resource or player (useful for detecting excessive event/network spam).

### Prerequisites

* A **running FiveM server**.
* Access to the **server console(txAdmin console)** or **RCON**.
* For client-side profiling: developer console (F8) and permission to use `profiler` commands.

### Server-Side Profiling (CPU Usage)

{% stepper %}
{% step %}
#### Start the Profiler

In the **server console**, run:

```
profile start
```

You can also specify a resource:

```
profile start <resourceName>
```
{% endstep %}

{% step %}
#### Let It Run Then Stop

Let the server run for **30–60 seconds** while normal gameplay or test activity happens. Then run:

```
profile stop
```
{% endstep %}

{% step %}
#### View Results

The profiler will output results in your console or create a `.json` file (depending on version).\
To print results directly:

```
profile view
```

The output shows:

* **Resource Name**
* **Average time (ms)**
* **Total calls**
* **CPU % usage**

Look for **resources with high average or total times** — these are likely causing performance drops.
{% endstep %}
{% endstepper %}

### Client-Side Profiling (FPS / Performance)

{% stepper %}
{% step %}
#### Open the F8 Console and Start the Profiler

Press `F8` in-game (as a developer/admin).

`profiler record`
{% endstep %}

{% step %}
#### Perform Actions In-Game

Do things that normally cause lag or stutter.
{% endstep %}

{% step %}
#### Stop and View Results

```
profiler stop
```

Then:

```
profiler view
```

This shows which client-side scripts consume the most frame time.

#### Optional: Export the Report

```
profiler save <filename>
```

You can open the saved file with Chrome’s **Performance Viewer** (`chrome://tracing`) for a detailed breakdown
{% endstep %}
{% endstepper %}

### Network Profiling (Bandwidth Usage)

To track network events and packets:

```
netgraph 1
```

Shows per-client network usage overlay (similar to GTA:O dev netgraph).

Or for resource-level network debugging:

```
nettrace start
...
nettrace stop
```

Then analyze logs for excessive event spam or large data transmissions.

#### Example Use Case

Say you suspect your **inventory script** is lagging:

1. Run `profile start inventory`.
2. Have players open and use inventories for 1–2 minutes.
3. Run `profile stop` then `profile view`.
4. If the average tick time > 2ms, the script may need optimization.

### Tips for Better Results

* Run profiling during **normal gameplay load** (10–20 players).
* Avoid profiling during restarts or idle time.
* If one resource shows **>2–3ms average tick**, inspect its loops or timers.
* Combine this with `resmon 1` for a real-time in-game performance overlay.

### Helpful Commands

| Command                    | Description                          |
| -------------------------- | ------------------------------------ |
| `resmon 1`                 | Real-time resource monitor (in-game) |
| `profile start [resource]` | Start CPU profiling                  |
| `profile stop`             | Stop profiling                       |
| `profile view`             | View results                         |
| `profiler record`          | Start client-side profiler           |
| `profiler stop`            | Stop client-side profiler            |
| `profiler save <name>`     | Save profiling data                  |
| `nettrace start/stop`      | Start/stop network profiling         |
| `netgraph 1`               | Show network usage overlay           |

{% hint style="danger" %}
We do not offer any support other than what is found on this guide. Please do not ask us for any support or open tickets about this, they will be auto closed.&#x20;
{% endhint %}
