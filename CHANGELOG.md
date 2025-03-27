# Change Log for [Tango](https://tango.makegov.com/) and [Tango API](https://tango.makegov.com/api)

All notable changes to this project will be documented in this file.
This project adheres to [Semantic Versioning](http://semver.org/).

[![Production Badge](https://tango.makegov.com/badges/version.svg?label=production)](https://tango.makegov.com/)
[![Staging Badge](https://staging-tango.makegov.com/badges/version.svg?label=staging)](https://staging-tango.makegov.com/)

## 3.0.4 (2025-03-27)

**Changes**

- **Auth:** Adds support for API key authentication.
- **Auth:** Auto-generates default API key for new users.
- **Auth:** Accounts page updated with API key management.

## 3.0.0 (2025-03-25) 🎉🎉🎉

**Changes**

- **API:** Major improvements to awards data structure for performance and consistency.

## 2.6.21 (2025-03-18)

**Changes**

- **Entities:** Adds summary metrics to entity detail API.

## 2.6.20 (2025-03-15)

**Changes**

- **Metrics:** Adds endpoints for NAICS and PSC code metrics.

## 2.6.19 (2025-03-14)

**Changes**

- **Entities:** Adds API support for basic entity metrics.

## 2.6.17 (2025-03-07)

**Changes**

- **Entities:** Optimizes entity loading process.
- **Entities:** Adds index for `cage_code` to improve lookup performance.
- **Opportunities:** Improved performance on opportunity queries.

## 2.6.14 (2025-02-25)

**Changes**

- **Opportunities:** Faster opportunity queries and better indexing under the hood.

## 2.6.13 (2025-02-18)

**Changes**

- **API:** Adds support for `psc_code` filtering on `contracts` endpoint.

## 2.6.12 (2025-02-10)

**Changes**

- **Search:** Improves opportunity search vector matching.
- **Entities:** Additional entity metrics exposed.

## 2.6.11 (2025-02-03)

**Changes**

- **Awards:** New materialized view for aggregated award data powering faster API responses.

## 2.6.10 (2025-01-26)

**Changes**

- **Entities:** Adds new filters for entity searches.
- **Assistance:** Exposes more fields on `assistance_transactions` endpoint.

## 2.6.9 (2025-01-19)

**Changes**

- **Contracts:** Adds support for `pop_end_date` filtering.

## 2.6.7 (2025-01-08)

**Changes**

- **Entities:** Enhances organization-level aggregation performance.

## 2.6.6 (2025-01-03)

**Changes**

- **Opportunities:** Fixes issue with filtering by NAICS/PSC combo.

## 2.6.5 (2024-12-30)

**Changes**

- **Opportunities:** Improves disjunctive keyword filtering performance.

## 2.6.4 (2024-12-21)

**Changes**

- **Opportunities:** Bugfix for keyword highlighting in results.

## 2.6.3 (2024-12-15)

**Changes**

- **Search:** Improves search results relevance for `opportunities`.

## 2.6.2 (2024-12-08)

**Changes**

- **API:** Adds support for multi-keyword OR-search logic.

## 2.6.1 (2024-12-01)

**Changes**

- **API:** Fixes date filters returning incorrect opportunities.

## 2.6.0 (2024-11-28)

**Changes**

- **Entities:** Adds endpoint for `related_entities` data.
- **Opportunities:** Adds `base_notice_type_code` to API response.

## 2.5.0 (2024-11-25)

**Changes**

- **Entities:** Adds endpoint for entity summary data.

## 2.1.5 (2024-11-22)

**Changes**

- **Opportunities:** Redesigned `Opportunity` and `OpportunityNotice` models for streamlined data handling.
- **Opportunities:** Added support for empty opportunity titles and other edge cases.
- **Opportunities:** API improvements for opportunities management.

### Closed issues

- Resolves makegov/tango-public#3

## 2.0.0 (2024-11-11)

**Changes**

- **Opportunities:** Implemented a new schema for opportunities, optimizing data structure and usability.
- **Opportunities:** Improved `OpportunityNotice` integration and functionality.
- **Codebase:** Organized views and URLs into app-specific folders for better maintainability.


## 1.5.1 (2024-11-04)$$

**Changes**

- **API:** Adds ordering parameters to `contracts` and `idvs` endpoints
- **API:** Defaults ordering for `contracts` and `idvs` endpoints to `award_date`

### Closed issues

- Resolves makegov/tango-public#11

## 1.4.10 (2024-10-19)

**Changes**

- **API:** Cleans up responses for certain endpoints without values

## 1.4.7 (2024-10-11)

**Changes**

- **API:** Adds multiple keyword search with disjunctive logic for `opportunities`

### Closed issues

- Resolves makegov/tango-public#10

## 1.4.5 (2024-10-11)

**Changes**

- **API:** Adds `assistance_listings` endpoint; learn more about Assistance Listing (CFDA) data [here](https://fedspendingtransparency.github.io/whitepapers/cfdaprogramnumber-title/)
- **API:** Adds `version` endpoint
- **API:** Fixes `business_types` detail endpoint so it properly accepts business type codes
- **Awards:** Adds FPDS loader for both historical and contemporaneous data; currently, only newer data is being added by the FPDS loader
- **Misc:** Version badges so y'all can know where we're at!

### Breaking changes

- **API:** `last_updated_time` has been renamed `last_updated` on the `notices` and `opportunities` endpoints

### Closed issues

- Resolves makegov/tango-public#5

## 1.4.1 (2024-10-04)

**Changes**

- **Notices/Opportunities:** Fixes encoding for notices and opportunities

### Closed issues

- Resolves makegov/tango-public#1

## 1.4.0 (2024-09-27)

### Breaking changes

- **API:** Standardized all API endpoints to use `limit` instead of having some use `page_size` for choosing the number of results
- **API:** Changes parameter `naics_code` to `naics` for `notices` and `opportunities` endpoints

### Additional changes

- **API:** Removed alphabetical sorting of parameters (Endpoints: ALL)
- **API:** Added documentation and examples for parameters that accept disjunctive values: `naics`, `psc`, etc. (Endpoints: ALL)
- **API:** Added `psc` parameter (Endpoints: `notices`, `opportunities`)
- **API:** Added `place_of_performance` parameter (Endpoints: `notices`, `opportunities`)
- **API:** Added disjunctive search for both `agency`, `naics`, `office`, `psc` (Endpoints: ALL)

### Closed issues

- Resolves makegov/tango-public#4
