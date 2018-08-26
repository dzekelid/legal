{
  "info": {
    "name": "Dezrez Gets accounting system for a legal entity",
    "_postman_id": "a51bb447-0068-4696-b2a4-e2e31ad1b95f",
    "description": "Gets accounting system for a legal entity.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "System",
      "item": [
        {
          "id": "c6b18d8b-9217-45db-a98a-09aaf25e4003",
          "name": "Account_GetSystemAccount",
          "request": {
            "url": "http://api.dezrez.com/api/account/systemaccount",
            "method": "GET",
            "header": [
              {
                "key": "Rezi-Api-Version",
                "value": "{}",
                "description": "Specifies which version of the API to call",
                "disabled": false
              },
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Get system account for the accounting system."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "052d6d9f-0838-4f04-82e6-a9f2071fb615"
            }
          ]
        }
      ]
    },
    {
      "name": "S",
      "item": [
        {
          "id": "6c539474-cc66-4f00-8829-218bb1c52dae",
          "name": "AccountingSystem_Get",
          "request": {
            "url": "http://api.dezrez.com/api/accountingsystem",
            "method": "GET",
            "header": [
              {
                "key": "Rezi-Api-Version",
                "value": "{}",
                "description": "Specifies which version of the API to call",
                "disabled": false
              },
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Gets accounting system for a legal entity."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "d9d91f39-5476-46c4-9f72-2c78557ca314"
            }
          ]
        }
      ]
    }
  ]
}