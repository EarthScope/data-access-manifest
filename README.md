# Data Access Manifest Concept

A manifest contains the location, data type, and details of user selection.
Manifest locations are envisioned to be used primarily for identifying
data in object-storage systems, either as direct object access or to data
containers (zarr, tiledb, iceberg, etc.) at object-store prefixes.

A web service returning a manifest allows the consumer to access the data
according to their use case:
  * directly from high performance storage,
  * in parallel,
  * in the order desired,
  * only a subset of the initially selected data

This pattern is particularly useful for large data volumes that are
impractical to return in a synchronous access request.  It is also very
useful for large scale parallel processing.

## Examples
  * `may2025_ccp_fdsnws_example.json` May 2025 dataselect-api WIP example
  * `tiledb_content_stub.json` tileDB stub
