# USDA Agricultural Research Service (ARS)

The USDA Agricultural Research Service (ARS) is the principal in-house research agency of the US Department of Agriculture, conducting research to develop and implement solutions to agricultural problems. ARS provides public data access through FoodData Central (nutritional data) and the Ag Data Commons (agricultural research datasets).

**ARS Website:** https://www.ars.usda.gov  
**FoodData Central:** https://fdc.nal.usda.gov  
**Ag Data Commons:** https://agdatacommons.nal.usda.gov  
**APIs.yml:** https://raw.githubusercontent.com/api-evangelist/usda-agricultural-research-service-ars-/refs/heads/main/apis.yml

---

## Scope

- **Type:** Contract
- **Position:** Consuming
- **Access:** 3rd-Party

## Tags

Federal Government, Agriculture, Food Safety, Nutrition, Open Data, Research

## Timestamps

- **Created:** 2024-11-21
- **Modified:** 2026-05-03

---

## APIs

### USDA FoodData Central API
Integrated food and nutrition data system with extended nutritional composition data for thousands of foods.

- **Base URL:** `https://api.nal.usda.gov/fdc/v1`
- **Auth:** API key (query param `api_key`) — register free at [api.data.gov/signup](https://api.data.gov/signup/)
- **OpenAPI:** [openapi/usda-ars-fooddata-central-openapi.yml](openapi/usda-ars-fooddata-central-openapi.yml)
- **License:** CC0 1.0 Universal

Key endpoints:
- `GET /foods/search` — Search foods by keyword
- `GET /food/{fdcId}` — Get detailed nutritional data by FDC ID
- `GET/POST /foods` — Fetch multiple foods by FDC IDs
- `GET/POST /foods/list` — Browse foods in paginated list

Data types: Foundation Foods, SR Legacy, Survey (FNDDS), Branded Foods, Experimental Foods

### USDA Ag Data Commons CKAN API
Open agricultural research data repository with CKAN API for dataset metadata discovery.

- **Base URL:** `https://data.nal.usda.gov`
- **Auth:** None required for read access
- **OpenAPI:** [openapi/usda-ars-ag-data-commons-openapi.yml](openapi/usda-ars-ag-data-commons-openapi.yml)

Key endpoints:
- `GET /api/action/package_search` — Search datasets
- `GET /api/action/package_show` — Get dataset metadata
- `GET /api/action/datastore_search` — Query tabular dataset records

---

## Artifacts

| Type | Files |
|------|-------|
| OpenAPI Specs | [openapi/](openapi/) — 2 specs |
| Examples | [examples/](examples/) — 2 examples |
| Spectral Rules | [rules/](rules/) — 1 ruleset |
| Naftiko Capabilities | [capabilities/](capabilities/) — 1 workflow + 2 shared |
| JSON Schema | [json-schema/](json-schema/) — 1 schema |
| JSON Structure | [json-structure/](json-structure/) — 1 structure |
| JSON-LD | [json-ld/](json-ld/) — 1 context |
| Vocabulary | [vocabulary/](vocabulary/) — 1 vocabulary |

---

## Capabilities

### Shared Definitions
- [capabilities/shared/fooddata-central.yaml](capabilities/shared/fooddata-central.yaml) — FoodData Central API (3 operations)
- [capabilities/shared/ag-data-commons.yaml](capabilities/shared/ag-data-commons.yaml) — Ag Data Commons CKAN API (3 operations)

### Workflow Capabilities
- [capabilities/agricultural-research-data.yaml](capabilities/agricultural-research-data.yaml) — Agricultural research data access (6 MCP tools)
  - Food nutritional composition search
  - Detailed food data by FDC ID
  - Foundation Foods browsing
  - Research dataset discovery
  - Dataset metadata retrieval
  - Tabular dataset record queries

---

## GitHub Organizations

- [USDA-ARS](https://github.com/USDA-ARS) — Main ARS GitHub org
- [USDA-ARS-GBRU](https://github.com/usda-ars-gbru) — Genomics and Bioinformatics Research Unit
- [USDA-ARS-NWRC](https://github.com/usda-ars-nwrc) — Northwest Watershed Research Center
- [USDA-ARS-ACSL](https://github.com/USDA-ARS-ACSL) — Adaptive Cropping Systems Laboratory

---

## Use Cases

- **Nutrition Research** — Access food nutritional data for dietary analysis and research
- **Food Labeling** — Look up nutritional composition for food products
- **Agricultural Research Discovery** — Find ARS datasets on soil health, crop genetics, and more
- **Food Safety Assessment** — Access baseline food composition for contaminant research
- **Sustainable Agriculture Research** — Discover LTAR network and soil health datasets
- **Plant Genetics** — Explore germplasm resources and crop diversity datasets

---

## Maintainers

**FN:** Kin Lane  
**Email:** kin@apievangelist.com
