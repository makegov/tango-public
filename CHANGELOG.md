# Change Log for [Tango](https://tango.makegov.com/) and [Tango API](https://tango.makegov.com/api)

All notable changes to this project will be documented in this file.
This project adheres to [Semantic Versioning](http://semver.org/).

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
