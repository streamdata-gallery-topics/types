---
swagger: "2.0"
x-collection-name: YouTube
x-complete: 0
info:
  title: Youtube Get Reporttypes
  description: Lists report types.
  termsOfService: https://developers.google.com/terms/
  contact:
    name: Google
    url: https://google.com
  version: 1.0.0
host: www.googleapis.com
basePath: /youtube/v1
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /v1/reportTypes:
    get:
      summary: Get Reporttypes
      description: Lists report types.
      operationId: getV1Reporttypes
      x-api-path-slug: v1reporttypes-get
      parameters:
      - in: query
        name: includeSystemManaged
        description: If set to true, also system-managed report types will be returned;otherwise
          only the report types that can be used to create new reportingjobs will
          be returned
      - in: query
        name: onBehalfOfContentOwner
        description: The content owners external ID on which behalf the user is acting
          on
      - in: query
        name: pageSize
        description: Requested page size
      - in: query
        name: pageToken
        description: A token identifying a page of results the server should return
      responses:
        200:
          description: OK
      tags:
      - V1
      - Reporttypes
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