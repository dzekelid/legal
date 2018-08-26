---
swagger: "2.0"
x-collection-name: Dezrez
x-complete: 1
info:
  title: Dezrez.Rezi.Client.Api
  version: 1.0.0
host: api.dezrez.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /api/accountingsystem:
    get:
      summary: Gets accounting system for a legal entity
      description: Gets accounting system for a legal entity.
      operationId: AccountingSystem_Get
      x-api-path-slug: apiaccountingsystem-get
      parameters:
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - S
      - Accounting
      - Systema
      - Legal
      - Entity
  /api/Peppermint:
    post:
      summary: Submits a referral to dezrez legal
      description: Submits a referral to dezrez legal.
      operationId: Peppermint_SubmitReferralByreferralDataContract
      x-api-path-slug: apipeppermint-post
      parameters:
      - in: body
        name: referralDataContract
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Submits
      - Referral
      - To
      - Dezrez
      - Legal
---