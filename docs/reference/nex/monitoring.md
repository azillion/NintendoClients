
# Module: <code>nintendo.nex.monitoring</code>

Provides a client and server for the `MonitoringProtocol`. This page was generated automatically from `monitoring.proto`.

<code>**class** [MonitoringClient](#monitoringclient)</code><br>
<span class="docs">The client for the `MonitoringProtocol`.</span>

<code>**class** [MonitoringServer](#monitoringserver)</code><br>
<span class="docs">The server for the `MonitoringProtocol`.</span>

## MonitoringClient
<code>**def _\_init__**(client: [RMCClient](rmc.md#rmcclient) / [HppClient](hpp.md#hppclient))</code><br>
<span class="docs">Creates a new [`MonitoringClient`](#monitoringclient).</span>

<code>**async def ping_daemon**() -> bool</code><br>
<span class="docs">Calls method `1` on the server.</span>

<code>**async def get_cluster_members**() -> list[str]</code><br>
<span class="docs">Calls method `2` on the server.</span>

## MonitoringServer
<code>**def _\_init__**()</code><br>
<span class="docs">Creates a new [`MonitoringServer`](#monitoringserver).</span>

<code>**async def logout**(client: [RMCClient](rmc.md#rmcclient)) -> None</code><br>
<span class="docs">Called whenever a client is disconnected. May be overridden by a subclass.</span>

<code>**async def ping_daemon**(client: [RMCClient](rmc.md#rmcclient)) -> bool</code><br>
<span class="docs">Handler for method `1`. This method should be overridden by a subclass.</span>

<code>**async def get_cluster_members**(client: [RMCClient](rmc.md#rmcclient)) -> list[str]</code><br>
<span class="docs">Handler for method `2`. This method should be overridden by a subclass.</span>

