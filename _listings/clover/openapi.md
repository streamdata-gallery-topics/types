swagger: "2.0"
x-collection-name: Clover
x-complete: 1
info:
  title: ""
  version: 1.0.0
host: /merchants
basePath: https://api.clover.com
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /v3/merchants/{mId}/order_types:
    get:
      summary: Get all order types for a merchant
      description: Merchants have the ability to create custom order types via the
        Setup App (https://www.clover.com/setupapp). These custom order types can
        be associated with a System Order Type (see /v3/merchants/{mId}/system_order_types).
        Custom Order Types can support items in all categories (filterCategories=false)
        or a subset of the merchant's categories (filterCategories=true and categories
        property contains the list of supported categories). Note that when expanding
        the categories for an order type, they will only be returned if this orderType
        only supports a subset of the categories (filterCategories=true). If the orderType
        supports all categories (filterCategories=false) then you should make a GET
        request to /v3/merchants/{mId}/categories.
      operationId: GetOrderTypes
      x-api-path-slug: v3merchantsmidorder-types-get
      parameters:
      - in: query
        name: expand
        description: 'Expandable fields: [hours, attributes, categories]'
      - in: query
        name: filter
        description: 'Filter fields: [id, deletedTime]'
      - in: path
        name: mId
        description: Merchant Id
      responses:
        200:
          description: OK
      tags:
      - Merchants
      - Order
      - Types
    post:
      summary: Create Order Type For Merchant
      description: Create order type for merchant.
      operationId: CreateOrderType
      x-api-path-slug: v3merchantsmidorder-types-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: expand
        description: 'Expandable fields: [hours, attributes, categories]'
      - in: path
        name: mId
        description: Merchant Id
      responses:
        200:
          description: OK
      tags:
      - Merchants
      - Order
      - Types
  /v3/merchants/{mId}/order_types/{orderTypeId}:
    get:
      summary: Get a single order type
      description: Get a single order type.
      operationId: GetOrderType
      x-api-path-slug: v3merchantsmidorder-typesordertypeid-get
      parameters:
      - in: query
        name: expand
        description: 'Expandable fields: [hours, attributes, categories]'
      - in: path
        name: mId
        description: Merchant Id
      - in: path
        name: orderTypeId
        description: Order Type Id
      responses:
        200:
          description: OK
      tags:
      - Merchants
      - Order
      - Types
      - OrderTypeId
    post:
      summary: Update a single order type
      description: Update a single order type.
      operationId: UpdateOrderType
      x-api-path-slug: v3merchantsmidorder-typesordertypeid-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: expand
        description: 'Expandable fields: [hours, attributes, categories]'
      - in: path
        name: mId
        description: Merchant Id
      - in: path
        name: orderTypeId
        description: Order Type Id
      responses:
        200:
          description: OK
      tags:
      - Merchants
      - Order
      - Types
      - OrderTypeId
    delete:
      summary: Delete an order type
      description: Delete an order type.
      operationId: DeleteOrderType
      x-api-path-slug: v3merchantsmidorder-typesordertypeid-delete
      parameters:
      - in: path
        name: mId
        description: Merchant Id
      - in: path
        name: orderTypeId
        description: Order Type Id
      responses:
        200:
          description: OK
      tags:
      - Merchants
      - Order
      - Types
      - OrderTypeId
  /v3/merchants/{mId}/system_order_types:
    get:
      summary: Return a list of system order types
      description: Merchants can create custom Order Types via "/v3/merchants/{mId}/order_types".
        It is useful to associate these custom order types with particular system
        order types in order to group things functionally. For example, a merchant
        may have a "Lunch Take-Out" order type and a "Dinner Take-Out" order type.
        These two order types can be associated with the "TAKE-OUT-TYPE" system order
        type so that applications can understand that they are both take-out order
        types.
      operationId: GetSystemOrderTypes
      x-api-path-slug: v3merchantsmidsystem-order-types-get
      parameters:
      - in: path
        name: mId
        description: Merchant Id
      responses:
        200:
          description: OK
      tags:
      - Merchants
      - System
      - Order
      - Types
  /v3/merchants/{mId}/order_type_categories:
    post:
      summary: Create or delete a order type category
      description: Create or delete a order type category.
      operationId: CreateOrDeleteOrderTypeCategories
      x-api-path-slug: v3merchantsmidorder-type-categories-post
      parameters:
      - in: path
        name: mId
        description: Merchant Id
      responses:
        200:
          description: OK
      tags:
      - Merchants
      - Order
      - Type
      - Categories