
# Module: <code>nintendo.nex.utility</code>

Provides a client and server for the `UtilityProtocol`. This page was generated automatically from `utility.proto`.

<code>**class** [UtilityClient](#utilityclient)</code><br>
<span class="docs">The client for the `UtilityProtocol`.</span>

<code>**class** [UtilityServer](#utilityserver)</code><br>
<span class="docs">The server for the `UtilityProtocol`.</span>

<code>**class** [UniqueIdInfo](#uniqueidinfo)([Structure](common.md))</code><br>

## UtilityClient
<code>**def _\_init__**(client: [RMCClient](rmc.md#rmcclient) / [HppClient](hpp.md#hppclient))</code><br>
<span class="docs">Creates a new [`UtilityClient`](#utilityclient).</span>

<code>**async def acquire_nex_unique_id**() -> int</code><br>
<span class="docs">Calls method `1` on the server.</span>

<code>**async def acquire_nex_unique_id_with_password**() -> [UniqueIdInfo](#uniqueidinfo)</code><br>
<span class="docs">Calls method `2` on the server.</span>

<code>**async def associate_nex_unique_id_with_my_principal_id**(info: [UniqueIdInfo](#uniqueidinfo)) -> None</code><br>
<span class="docs">Calls method `3` on the server.</span>

<code>**async def associate_nex_unique_ids_with_my_principal_id**(infos: list[[UniqueIdInfo](#uniqueidinfo)]) -> None</code><br>
<span class="docs">Calls method `4` on the server.</span>

<code>**async def get_associated_nex_unique_id_with_my_principal_id**() -> [UniqueIdInfo](#uniqueidinfo)</code><br>
<span class="docs">Calls method `5` on the server.</span>

<code>**async def get_associated_nex_unique_ids_with_my_principal_id**() -> list[[UniqueIdInfo](#uniqueidinfo)]</code><br>
<span class="docs">Calls method `6` on the server.</span>

<code>**async def get_integer_settings**(index: int) -> dict[int, int]</code><br>
<span class="docs">Calls method `7` on the server.</span>

<code>**async def get_string_settings**(index: int) -> dict[int, str]</code><br>
<span class="docs">Calls method `8` on the server.</span>

## UtilityServer
<code>**def _\_init__**()</code><br>
<span class="docs">Creates a new [`UtilityServer`](#utilityserver).</span>

<code>**async def logout**(client: [RMCClient](rmc.md#rmcclient)) -> None</code><br>
<span class="docs">Called whenever a client is disconnected. May be overridden by a subclass.</span>

<code>**async def acquire_nex_unique_id**(client: [RMCClient](rmc.md#rmcclient)) -> int</code><br>
<span class="docs">Handler for method `1`. This method should be overridden by a subclass.</span>

<code>**async def acquire_nex_unique_id_with_password**(client: [RMCClient](rmc.md#rmcclient)) -> [UniqueIdInfo](#uniqueidinfo)</code><br>
<span class="docs">Handler for method `2`. This method should be overridden by a subclass.</span>

<code>**async def associate_nex_unique_id_with_my_principal_id**(client: [RMCClient](rmc.md#rmcclient), info: [UniqueIdInfo](#uniqueidinfo)) -> None</code><br>
<span class="docs">Handler for method `3`. This method should be overridden by a subclass.</span>

<code>**async def associate_nex_unique_ids_with_my_principal_id**(client: [RMCClient](rmc.md#rmcclient), infos: list[[UniqueIdInfo](#uniqueidinfo)]) -> None</code><br>
<span class="docs">Handler for method `4`. This method should be overridden by a subclass.</span>

<code>**async def get_associated_nex_unique_id_with_my_principal_id**(client: [RMCClient](rmc.md#rmcclient)) -> [UniqueIdInfo](#uniqueidinfo)</code><br>
<span class="docs">Handler for method `5`. This method should be overridden by a subclass.</span>

<code>**async def get_associated_nex_unique_ids_with_my_principal_id**(client: [RMCClient](rmc.md#rmcclient)) -> list[[UniqueIdInfo](#uniqueidinfo)]</code><br>
<span class="docs">Handler for method `6`. This method should be overridden by a subclass.</span>

<code>**async def get_integer_settings**(client: [RMCClient](rmc.md#rmcclient), index: int) -> dict[int, int]</code><br>
<span class="docs">Handler for method `7`. This method should be overridden by a subclass.</span>

<code>**async def get_string_settings**(client: [RMCClient](rmc.md#rmcclient), index: int) -> dict[int, str]</code><br>
<span class="docs">Handler for method `8`. This method should be overridden by a subclass.</span>

## UniqueIdInfo
<code>**def _\_init__**()</code><br>
<span class="docs">Creates a new `UniqueIdInfo` instance. Required fields must be filled in manually.</span>

The following fields are defined in this class:<br>
<span class="docs">
<code>unique_id: int = 0</code><br>
<code>password: int = 0</code><br>
</span><br>

