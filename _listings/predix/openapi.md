swagger: "2.0"
x-collection-name: Predix
x-complete: 1
info:
  title: VIEWS
  version: 1.0.0
host: thetaray-anomaly-service.run.aws-usw02-pr.ice.predix.io
basePath: /v1
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /v1/blocks:
    get:
      summary: Get Blocks
      description: Get current blockchain root info
      operationId: get-current-blockchain-root-info
      x-api-path-slug: v1blocks-get
      parameters:
      - in: header
        name: Authorization
        description: access token
      - in: header
        name: predix-zone-id
        description: tenantId
      responses:
        200:
          description: OK
      tags:
      - Blocks
  /v1/blocks/{blockNumber}:
    get:
      summary: Get Blocks Blocknumber
      description: Get a single blockchain info
      operationId: get-a-single-blockchain-info
      x-api-path-slug: v1blocksblocknumber-get
      parameters:
      - in: header
        name: Authorization
        description: access token
      - in: path
        name: blockNumber
        description: block node number
      - in: header
        name: predix-zone-id
        description: tenantId
      responses:
        200:
          description: OK
      tags:
      - Blocks
      - Blocknumber