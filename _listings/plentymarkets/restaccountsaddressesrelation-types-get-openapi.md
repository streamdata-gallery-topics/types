---
swagger: "2.0"
x-collection-name: Plentymarkets
x-complete: 0
info:
  title: Plentymarkets List address relation types
  description: List address relation types.
  contact:
    name: plentymarkets
    url: https://forum.plentymarkets.com/c/rest-api
  version: 1.0.0
host: example.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /rest/accounts/addresses/option_types:
    get:
      summary: List address option types
      description: List address option types.
      operationId: getRestAccountsAddressesOptionTypes
      x-api-path-slug: restaccountsaddressesoption-types-get
      responses:
        200:
          description: OK
      tags:
      - List
      - Address
      - Option
      - Types
  /rest/accounts/addresses/relation_types:
    get:
      summary: List address relation types
      description: List address relation types.
      operationId: getRestAccountsAddressesRelationTypes
      x-api-path-slug: restaccountsaddressesrelation-types-get
      responses:
        200:
          description: OK
      tags:
      - List
      - Address
      - Relation
      - Types
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---