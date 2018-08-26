---
swagger: "2.0"
x-collection-name: Storecove
x-complete: 1
info:
  title: Storecove
  description: storecove-api
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
    patch:
      summary: Update LegalEntity
      description: Update a specific LegalEntity.
      operationId: update_legal_entity
      x-api-path-slug: legal-entitiesid-patch
      parameters:
      - in: path
        name: id
        description: legal_entity id
      - in: body
        name: legal_entity
        description: LegalEntity updates
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Legal
      - Entities
  /legal_entities/{legal_entity_id}/peppol_identifiers:
    post:
      summary: Create a new PeppolIdentifier
      description: Create a new PeppolIdentifier.
      operationId: create_peppol_identifier
      x-api-path-slug: legal-entitieslegal-entity-idpeppol-identifiers-post
      parameters:
      - in: path
        name: legal_entity_id
      - in: body
        name: peppol_identifier
        description: PeppolIdentifier to create
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Legal
      - Entities
      - Legal
      - Entity
      - Peppolentifiers
  /legal_entities/{legal_entity_id}/peppol_identifiers/iso6523-actorid-upis/{scheme}/{identifier}:
    delete:
      summary: Delete PeppolIdentifier
      description: Delete a specific PeppolIdentifier.
      operationId: delete_peppol_identifier
      x-api-path-slug: legal-entitieslegal-entity-idpeppol-identifiersiso6523actoridupisschemeidentifier-delete
      parameters:
      - in: path
        name: identifier
        description: PEPPOL identifier
      - in: path
        name: legal_entity_id
        description: The id of the LegalEntity this PeppolIdentifier belongs to
      - in: path
        name: scheme
        description: PEPPOL identifier scheme id, e
      responses:
        200:
          description: OK
      tags:
      - Legal
      - Entities
      - Legal
      - Entity
      - Peppolentifiers
      - Iso6523
      - Actorid
      - Upis
      - Schemeentifier
    patch:
      summary: Update PeppolIdentifier
      description: Update a specific PeppolIdentifier.
      operationId: update_peppol_identifier
      x-api-path-slug: legal-entitieslegal-entity-idpeppol-identifiersiso6523actoridupisschemeidentifier-patch
      parameters:
      - in: path
        name: identifier
        description: PEPPOL identifier
      - in: path
        name: legal_entity_id
        description: The id of the LegalEntity this PeppolIdentifier belongs to
      - in: body
        name: peppol_identifier
        description: PeppolIdentifier updates
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: scheme
        description: PEPPOL identifier scheme id, e
      responses:
        200:
          description: OK
      tags:
      - Legal
      - Entities
      - Legal
      - Entity
      - Peppolentifiers
      - Iso6523
      - Actorid
      - Upis
      - Schemeentifier
---