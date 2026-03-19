# Server & Player Core



| Metric                                | Description                        |
| ------------------------------------- | ---------------------------------- |
| `scripts_1of1_player_count`           | Currently connected players        |
| `scripts_1of1_player_connections`     | Total connections since restart    |
| `scripts_1of1_player_disconnections`  | Total disconnections since restart |
| `scripts_1of1_average_player_latency` | Average ping (ms)                  |
| `scripts_1of1_min_player_ping`        | Lowest ping (ms)                   |
| `scripts_1of1_max_player_ping`        | Highest ping (ms)                  |
| `scripts_1of1_players_latency`        | Histogram of player latencies      |
| `scripts_1of1_server_uptime`          | Seconds since resource start       |
| `scripts_1of1_object_count`           | Objects in world                   |
| `scripts_1of1_ped_count`              | NPCs in world                      |
| `scripts_1of1_vehicle_count`          | Vehicles in world                  |
| `scripts_1of1_events_server`          | Total server events triggered      |
| `scripts_1of1_events_client`          | Total client events triggered      |

<figure><img src="../../../../.gitbook/assets/image (9).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../../.gitbook/assets/image (4).png" alt=""><figcaption></figcaption></figure>

### Player Sessions

| Metric                            | Description                  |
| --------------------------------- | ---------------------------- |
| `scripts_1of1_avg_session_time`   | Average session time (s)     |
| `scripts_1of1_max_session_time`   | Longest active session (s)   |
| `scripts_1of1_total_session_time` | Sum of all session times (s) |

### Player Data

| Metric                               | Description                          |
| ------------------------------------ | ------------------------------------ |
| `scripts_1of1_player_routing_bucket` | Players per routing bucket (labeled) |
| `scripts_1of1_player_avg_last_msg`   | Avg ms since last network message    |
| `scripts_1of1_player_max_last_msg`   | Worst ms since last network message  |
| `scripts_1of1_unique_player_ips`     | Unique IP count                      |
| `scripts_1of1_players_in_vehicles`   | Players currently in a vehicle       |
| `scripts_1of1_server_capacity_pct`   | Server capacity %                    |
| `scripts_1of1_lua_memory_kb`         | Lua runtime memory (KB)              |

<figure><img src="../../../../.gitbook/assets/image (8).png" alt=""><figcaption></figcaption></figure>

### Server Tick Performance

| Metric                        | Description                       |
| ----------------------------- | --------------------------------- |
| `scripts_1of1_tick_rate`      | Effective tick rate (ticks/sec)   |
| `scripts_1of1_tick_count`     | Ticks in last collection interval |
| `scripts_1of1_frame_time_avg` | Average server frame time (ms)    |
| `scripts_1of1_frame_time_min` | Minimum server frame time (ms)    |
| `scripts_1of1_frame_time_max` | Maximum server frame time (ms)    |
| `scripts_1of1_frame_time`     | Histogram of server frame times   |

<figure><img src="../../../../.gitbook/assets/image (7).png" alt=""><figcaption></figcaption></figure>
