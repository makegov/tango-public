# Change Log for [Tango](https://tango.makegov.com/) and [Tango API](https://tango.makegov.com/api)

All notable changes to this project will be documented in this file.
This project adheres to [Semantic Versioning](http://semver.org/).

[![Production Badge](https://tango.makegov.com/badges/version.svg?label=production)](https://tango.makegov.com/)
[![Staging Badge](https://staging-tango.makegov.com/badges/version.svg?label=staging)](https://staging-tango.makegov.com/)

## 1.5.1 (2024-11-04)

### Changes

- **API:** Adds ordering parameters to `contracts` and `idvs` endpoints
- **API:** Defaults ordering for `contracts` and `idvs` endpoints to `award_date`

### Closed issues

- Resolves makegov/tango-public#11

## 1.4.10 (2024-10-19)

### Changes

- **API:** Cleans up responses for certain endpoints without values

## 1.4.7 (2024-10-11)

### Changes

- **API:** Adds multiple keyword search with disjunctive logic for `opportunities`

### Closed issues

- Resolves makegov/tango-public#10

## 1.4.5 (2024-10-11)

### Changes

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

### Changes

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
