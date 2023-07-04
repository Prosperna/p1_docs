---
title: /business-profile/ph-locale/barangays/:municipalityId
position_number: 1.5
type: get
description: Get all Philippine barangay via municipality id
content_markdown: |-
  | ***Parameters***         | ***Data Type*** | ***Required*** | ***Description***                        |
  |--------------------|-----------|----------|------------------------------------|
  | municipalityId               | string    | Yes      | Municipality id            |

left_code_blocks:
  - code_block: |-
      var axios = require('axios');

      var config = {
      method: 'get',
      url: 'api.prosperna.com/v1/business-profile/ph-locale/barangays/:municipalityId',
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
          "message": "Successfully retrieve PH barangays by municipality ID.",
          "data": {
              "barangays": [
                  {
                      "_id": "60530f265d8baa22bcb5f314",
                      "barangayName": "Ableg",
                      "barangayNameUppercased": "ABLEG",
                      "municipality": "60530f215d8baa22bcb55f82",
                      "province": "60530f205d8baa22bcb5596f",
                      "region": "60530f205d8baa22bcb55922",
                      "dateCreated": "2021-03-18T08:28:22.397Z",
                      "lastUpdated": "2021-03-18T08:28:22.397Z"
                  },
                  {
                      "_id": "60530f265d8baa22bcb5f315",
                      "barangayName": "Cabaruyan",
                      "barangayNameUppercased": "CABARUYAN",
                      "municipality": "60530f215d8baa22bcb55f82",
                      "province": "60530f205d8baa22bcb5596f",
                      "region": "60530f205d8baa22bcb55922",
                      "dateCreated": "2021-03-18T08:28:22.397Z",
                      "lastUpdated": "2021-03-18T08:28:22.397Z"
                  },
                  {
                      "_id": "60530f265d8baa22bcb5f316",
                      "barangayName": "Pikek",
                      "barangayNameUppercased": "PIKEK",
                      "municipality": "60530f215d8baa22bcb55f82",
                      "province": "60530f205d8baa22bcb5596f",
                      "region": "60530f205d8baa22bcb55922",
                      "dateCreated": "2021-03-18T08:28:22.397Z",
                      "lastUpdated": "2021-03-18T08:28:22.397Z"
                  },
                  {
                      "_id": "60530f265d8baa22bcb5f317",
                      "barangayName": "Tui (Pob.)",
                      "barangayNameUppercased": "TUI (POB.)",
                      "municipality": "60530f215d8baa22bcb55f82",
                      "province": "60530f205d8baa22bcb5596f",
                      "region": "60530f205d8baa22bcb55922",
                      "dateCreated": "2021-03-18T08:28:22.397Z",
                      "lastUpdated": "2021-03-18T08:28:22.397Z"
                  }
              ]
          }
      }
    title: Response
    language: json
---
