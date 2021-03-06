---
swagger: "2.0"
x-collection-name: AWS Internet of Things
x-complete: 0
info:
  title: AWS Internet of Things API List Thing Types
  version: 1.0.0
  description: Lists the existing thing types.
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?Action=ListThingTypes:
    get:
      summary: List Thing Types
      description: Lists the existing thing types.
      operationId: listThingTypes
      x-api-path-slug: actionlistthingtypes-get
      parameters:
      - in: query
        name: maxResults
        description: The maximum number of results to return in this operation
        type: string
      - in: query
        name: nextToken
        description: The token for the next set of results, or null if there are no
          additional results
        type: string
      - in: query
        name: thingTypeName
        description: The name of the thing type
        type: string
      responses:
        200:
          description: OK
      tags:
      - Thing Types
  /?Action=CreateThingType:
    get:
      summary: Create Thing Type
      description: Creates a new thing type.
      operationId: createThingType
      x-api-path-slug: actioncreatethingtype-get
      parameters:
      - in: query
        name: thingTypeName
        description: The name of the thing type
        type: string
      - in: query
        name: thingTypeProperties
        description: The ThingTypeProperties for the thing type to create
        type: string
      responses:
        200:
          description: OK
      tags:
      - Thing Types
  /?Action=DeleteThingType:
    get:
      summary: Delete Thing Type
      description: Deletes the specified thing type.
      operationId: deleteThingType
      x-api-path-slug: actiondeletethingtype-get
      parameters:
      - in: query
        name: thingTypeName
        description: The name of the thing type
        type: string
      responses:
        200:
          description: OK
      tags:
      - Thing Types
  /?Action=DeprecateThingType:
    get:
      summary: Deprecate Thing Type
      description: Deprecates a thing type.
      operationId: deprecateThingType
      x-api-path-slug: actiondeprecatethingtype-get
      parameters:
      - in: query
        name: thingTypeName
        description: The name of the thing type to deprecate
        type: string
      - in: query
        name: undoDeprecate
        description: Whether to undeprecate a deprecated thing type
        type: string
      responses:
        200:
          description: OK
      tags:
      - Thing Types
  /?Action=DescribeThingType:
    get:
      summary: Describe Thing Type
      description: Gets information about the specified thing type.
      operationId: describeThingType
      x-api-path-slug: actiondescribethingtype-get
      parameters:
      - in: query
        name: thingTypeName
        description: The name of the thing type
        type: string
      responses:
        200:
          description: OK
      tags:
      - Thing Types
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