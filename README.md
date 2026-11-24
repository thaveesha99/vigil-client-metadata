# Vigil SOC OAuth client metadata

Client ID Metadata Document (CIMD) used by the local Vigil SOC install to sign
in to the hosted MCP servers on Railway (Sophos Fusion, Microsoft Defender,
FortiAnalyzer Cloud).

The broker at each of those servers has no dynamic client registration: it takes
an HTTPS URL as the `client_id` and fetches this document to learn which grant
types and redirect URIs the client may use.

It contains no credentials. The callback URIs are loopback addresses, which the
broker always permits, and the host `thaveesha99.github.io` must be listed in
each service's `MCP_ALLOWED_REDIRECT_HOSTS` variable.

Served by GitHub Pages at:
<https://thaveesha99.github.io/vigil-client-metadata/client-metadata.json>
