---
swagger: "2.0"
x-collection-name: Akamai
x-complete: 0
info:
  title: Akamai API List Metric Types
  description: List Metric Types
  version: 1.0.0
host: developer.akamai.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /prolexic-analytics/v1/metric-types:
    get:
      summary: List Metric Types
      description: List Metric Types
      operationId: prolexicanalyticsv1metrictypes
      x-api-path-slug: prolexicanalyticsv1metrictypes-get
      responses:
        200:
          description: OK
      tags:
      - Prolexic
      - Analytics
      - Metric
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