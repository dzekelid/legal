---
swagger: "2.0"
x-collection-name: Storecove
x-complete: 0
info:
  title: Storecove Get LegalEntity
  description: Get a specific LegalEntity.
  version: 2.0.1
host: api.storecove.com
basePath: /api/v2
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /legal_entities:
    post:
      summary: Create a new LegalEntity
      description: Create a new LegalEntity.
      operationId: create_legal_entity
      x-api-path-slug: legal-entities-post
      parameters:
      - in: body
        name: legal_entity
        description: LegalEntity to create
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Legal
      - Entities
  /legal_entities/{id}:
    delete:
      summary: Delete LegalEntity
      description: Delete a specific LegalEntity.
      operationId: delete_legal_entity
      x-api-path-slug: legal-entitiesid-delete
      parameters:
      - in: path
        name: id
        description: legal_entity id
      responses:
        200:
          description: OK
      tags:
      - Legal
      - Entities
    get:
      summary: Get LegalEntity
      description: Get a specific LegalEntity.
      operationId: get_legal_entity
      x-api-path-slug: legal-entitiesid-get
      parameters:
      - in: path
        name: id
        description: legal_entity id
      responses:
        200:
          description: OK
      tags:
      - Legal
      - Entities
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