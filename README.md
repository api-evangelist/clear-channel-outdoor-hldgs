# clear-channel-outdoor-hldgs

Profile for **Clear Channel Outdoor Holdings** (Fortune 1000 #1000) in the API Evangelist network.

Clear Channel Outdoor is one of the world's largest out-of-home (OOH) media companies, operating billboards, street furniture, transit, airport, and digital out-of-home (DOOH) inventory. This profile covers three layers of CCO's API and pDOOH ecosystem:

1. The **CCO.IO Automated Direct API** at `direct.cco.io` (developer portal at `developer.cco.io`) — programmatic-direct buying of CCO inventory.
2. The **pDOOH RTB supply chain** — 21+ DSP partners that transact CCO inventory using OpenRTB 2.6 with the DOOH object extension.
3. **RADAR**, CCO's first-party audience and attribution data suite.

## Artifacts

| Artifact | Path |
|---|---|
| `apis.yml` | [`apis.yml`](apis.yml) |
| OpenAPI (Automated Direct) | [`openapi/clear-channel-outdoor-direct-openapi.yml`](openapi/clear-channel-outdoor-direct-openapi.yml) |
| JSON Schema — DSP Integration | [`json-schema/clear-channel-outdoor-hldgs-dsp-integration-schema.json`](json-schema/clear-channel-outdoor-hldgs-dsp-integration-schema.json) |
| JSON Schema — DOOH Display | [`json-schema/clear-channel-outdoor-hldgs-display-schema.json`](json-schema/clear-channel-outdoor-hldgs-display-schema.json) |
| JSON Schema — OOH Order (OpenDirect) | [`json-schema/clear-channel-outdoor-hldgs-order-schema.json`](json-schema/clear-channel-outdoor-hldgs-order-schema.json) |
| JSON Schema — OpenRTB DOOH | [`json-schema/clear-channel-outdoor-hldgs-openrtb-dooh-schema.json`](json-schema/clear-channel-outdoor-hldgs-openrtb-dooh-schema.json) |
| JSON Structure — pDOOH supply chain | [`json-structure/clear-channel-outdoor-hldgs-pdooh-supply-chain-structure.json`](json-structure/clear-channel-outdoor-hldgs-pdooh-supply-chain-structure.json) |
| JSON-LD context | [`json-ld/clear-channel-outdoor-hldgs-context.jsonld`](json-ld/clear-channel-outdoor-hldgs-context.jsonld) |
| Examples | [`examples/`](examples/) |
| Spectral rules | [`rules/clear-channel-outdoor-direct-rules.yml`](rules/clear-channel-outdoor-direct-rules.yml) |
| Naftiko shared capability | [`capabilities/shared/clear-channel-outdoor-direct.yaml`](capabilities/shared/clear-channel-outdoor-direct.yaml) |
| Naftiko capability — programmatic-direct buying | [`capabilities/programmatic-direct-ooh-buying.yaml`](capabilities/programmatic-direct-ooh-buying.yaml) |
| Naftiko capability — pDOOH RTB supply | [`capabilities/pdooh-rtb-supply.yaml`](capabilities/pdooh-rtb-supply.yaml) |
| Vocabulary | [`vocabulary/clear-channel-outdoor-hldgs-vocabulary.yml`](vocabulary/clear-channel-outdoor-hldgs-vocabulary.yml) |

## CCO.IO Automated Direct API

REST API for buying CCO inventory programmatically. Authentication is OAuth 2.0 client credentials at `https://direct.cco.io/v2/token`. Path families surfaced in the OpenAPI:

`/v1/displays`, `/v1/networks`, `/v1/networks/{id}/displays`, `/v1/markets`, `/v1/products`, `/v1/orders`, `/v1/bookings`, `/v1/campaigns`, `/v1/creatives`, `/v2/creatives`, `/v1/photos`, `/v1/customers`, `/v1/accounts`, `/v1/contracts`, `/v1/quotes`, `/v1/quotes/current`, `/v1/relationships`, `/v1/restrictions`, `/v1/codes`, `/v1/taxa`, `/v2/taxa`, `/v3/taxa`.

These were derived from the open-source Go SDK [`ClearChannelOutdoor/io-sdk-golang`](https://github.com/ClearChannelOutdoor/io-sdk-golang) and the developer portal at [developer.cco.io](https://developer.cco.io).

## pDOOH DSP Partners

CCO supports programmatic DOOH buying through 21 DSP partners using OpenRTB 2.6 with the DOOH object: Adelphic, Adform, Adomni, AdQuick, Campsite, Displayce, Google DV360, Hivestack, Nexxen, OneView, OutMoove, Pulsepoint, Quotient, Simplifi, Sito, StackAdapt, The Trade Desk, Vistar Media, Xandr, Yahoo, and Zeta.

## Standards

- [OpenRTB 2.6 (with DOOH extension)](https://github.com/InteractiveAdvertisingBureau/openrtb2.x)
- [OpenDirect-OOH](https://github.com/Outsmart-OOH/ooh_open_direct) (CCO maintains a fork at [ClearChannelOutdoor/ooh_open_direct](https://github.com/ClearChannelOutdoor/ooh_open_direct))
- OpenOOH Venue Taxonomy (`venuetypetax=1`)
