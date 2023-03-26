---
title: /business-profile/shipping/:store_id
position_number: 1.7
type: get
description: Get all pickup address per store

content_markdown: |-
  | ***Request parameters***         | ***Data Type*** | ***Required*** | ***Description*** |
  |--------------------|-----------|----------|------------------------------------|
  | store_id               | string    | Yes      | Store id  |

left_code_blocks:
  - code_block: |-
      var axios = require('axios');

      var config = {
        method: 'get',
        url: 'api.prosperna.com/v1/business-profile/shipping/639749a5cb1db88617891bc2',
      };

      axios(config)
      .then(function (response) {
        console.log(JSON.stringify(response.data));
      })
      .catch(function (error) {
        console.log(error);
      });

    title: NodeJS
    language: javascript

right_code_blocks:
  - code_block: |-
      {
          "success": true,
          "message": "ok",
          "data": {
              "address": [
                  {
                      "store_id": "639749a5cb1db88617891bc2",
                      "contact_person": "contact_person",
                      "contact_number": "contact_number",
                      "business_address": "business_address",
                      "save_address_name": "save_address_name",
                      "province": {
                          "name": "",
                          "id": ""
                      },
                      "barangay": {
                          "name": "",
                          "id": ""
                      },
                      "city": {
                          "name": "",
                          "id": ""
                      },
                      "coordinates": {
                          "long": 121.1250825,
                          "lat": 14.1876712
                      },
                      "createdAt": "2023-01-26T11:55:00.754Z",
                      "updatedAt": "2023-01-26T11:55:00.754Z",
                      "id": "63d26a14a254f44dbf2fce3a"
                  },
              ]
          }
      }
    title: Response
    language: json
---
