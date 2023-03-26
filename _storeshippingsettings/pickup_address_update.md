---
title: /business-profile/shipping/:store_id/pickup-address/:pickup_address_id
position_number: 1.9
type: put
description: Add new pickup address

content_markdown: |-
  | ***Request parameters***         | ***Data Type*** | ***Required*** | ***Description*** |
  |--------------------|-----------|----------|------------------------------------|
  | store_id               | string    | Yes      | Store id  |
  | ***Request Body***         | ***Data Type*** | ***Required*** | ***Description*** |
  |--------------------|-----------|----------|------------------------------------|
  | barangay.id               | string    | Yes      | Barangay id |
  | barangay.name               | string    | Yes      | Barangay name |
  | province.id               | string    | Yes      | Province id |
  | province.name               | string    | Yes      | Province name |
  | city.id               | string    | Yes      | City id |
  | city.name               | string    | Yes      | City name |
  | contact_number               | string    | Yes      | Contact number |
  | contact_person               | string    | Yes      | Contact person |
  | business_address               | string    | Yes      | Business address |
  | save_address_name               | string    | Yes      | Save address name |
  | coordinates.lat               | number    | Yes, *if LALAMOVE will be used*      | Latitude coordinates |
  | coordinates.long               | number    | Yes, *if LALAMOVE will be used*      | Longitude coordinates |

left_code_blocks:
  - code_block: |-
      var axios = require('axios');
      var data = JSON.stringify({
        "barangay": {
          "id": "",
          "name": ""
        },
        "province": {
          "id": "",
          "name": ""
        },
        "city": {
          "id": "",
          "name": ""
        },
        "contact_number": "contact_number",
        "contact_person": "contact_person",
        "business_address": "business_address",
        "save_address_name": "save_address_name"
      });

      var config = {
        method: 'put',
        url: 'api.prosperna.com/v1/business-profile/shipping/63861440e2c90910a117e826/pickup-address/63908c8b5e8aa33cd37b9e77',
        data : data
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
          "message": "Successfully updated pickup address.",
          "data": {
              "address": {
                  "store_id": "63988d50710a9e5920f87b68",
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
                  "createdAt": "2023-03-26T13:24:26.597Z",
                  "updatedAt": "2023-03-26T13:24:26.597Z",
                  "id": "6420478a1e840f2c62fcbf08"
              }
          }
      }
    title: Response
    language: json
---
