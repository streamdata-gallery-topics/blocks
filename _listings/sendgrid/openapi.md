swagger: "2.0"
x-collection-name: SendGrid
x-complete: 1
info:
  title: SendGrid
  version: 1.0.0
host: api.sendgrid.com
basePath: /v3
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /suppression/blocks:
    delete:
      summary: Delete Suppression Blocks
      description: "**This endpoint allows you to delete all email addresses on your
        blocks list.**\n\nThere are two options for deleting blocked emails: \n\n1.
        You can delete all blocked emails by setting `delete_all` to true in the request
        body. \n2. You can delete some blocked emails by specifying the email addresses
        in an array in the request body.\n\n[Blocks](https://sendgrid.com/docs/Glossary/blocks.html)
        happen when your message was rejected for a reason related to the message,
        not the recipient address. This can happen when your mail server IP address
        has been added to a blacklist or blocked by an ISP, or if the message content
        is flagged by a filter on the receiving server.\n\nFor more information, please
        see our [User Guide](https://sendgrid.com/docs/User_Guide/Suppressions/blocks.html)."
      operationId: suppression.blocks.delete
      x-api-path-slug: suppressionblocks-delete
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Email
      - Suppression
      - Blocks
    get:
      summary: Get Suppression Blocks
      description: |-
        **This endpoint allows you to retrieve a list of all email addresses that are currently on your blocks list.**

        There are several causes for [blocked](https://sendgrid.com/docs/Glossary/blocks.html) emails: for example, your mail server IP address is on an ISP blacklist, or blocked by an ISP, or if the receiving server flags the message content.

        For more information, please see our [User Guide](https://sendgrid.com/docs/User_Guide/Suppressions/blocks.html).
      operationId: suppression.blocks.get
      x-api-path-slug: suppressionblocks-get
      parameters:
      - in: query
        name: end_time
        description: Refers end of the time range in unix timestamp when a blocked
          email was created (inclusive)
      - in: query
        name: limit
        description: Limit the number of results to be displayed per page
      - in: query
        name: No Name
      - in: query
        name: offset
        description: The point in the list to begin displaying results
      - in: query
        name: start_time
        description: Refers start of the time range in unix timestamp when a blocked
          email was created (inclusive)
      responses:
        200:
          description: OK
      tags:
      - Email
      - Suppression
      - Blocks
  /suppression/blocks/{email}:
    delete:
      summary: Delete Suppression Blocks Email
      description: |-
        **This endpoint allows you to delete a specific email address from your blocks list.**

        [Blocks](https://sendgrid.com/docs/Glossary/blocks.html) happen when your message was rejected for a reason related to the message, not the recipient address. This can happen when your mail server IP address has been added to a blacklist or blocked by an ISP, or if the message content is flagged by a filter on the receiving server.

        For more information, please see our [User Guide](https://sendgrid.com/docs/User_Guide/Suppressions/blocks.html).
      operationId: suppression.blocks.email.delete
      x-api-path-slug: suppressionblocksemail-delete
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Email
      - Suppression
      - Blocks
      - Email
    get:
      summary: Get Suppression Blocks Email
      description: |-
        **This endpoint allows you to retrieve a specific email address from your blocks list.**

        [Blocks](https://sendgrid.com/docs/Glossary/blocks.html) happen when your message was rejected for a reason related to the message, not the recipient address. This can happen when your mail server IP address has been added to a blacklist or blocked by an ISP, or if the message content is flagged by a filter on the receiving server.

        For more information, please see our [User Guide](https://sendgrid.com/docs/User_Guide/Suppressions/blocks.html).
      operationId: suppression.blocks.email.get
      x-api-path-slug: suppressionblocksemail-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Email
      - Suppression
      - Blocks
      - Email