---
title: /business-profile/store/additional-fee
position_number: 1.1
type: get
description: Get all additional fees

left_code_blocks:
  - code_block: |-

      var config = {
        method: 'get',
        url: 'api.prosperna.com/v1/business-profile/store/additional-fee',
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
          "message": "",
          "data": {
              "additional_fees": [
                  {
                      "store_id": "639749a5cb1db88617891bf0",
                      "description": "Additional fee description",
                      "price": 12,
                      "is_set": false,
                      "createdAt": "2023-03-26T08:19:16.731Z",
                      "updatedAt": "2023-03-26T08:19:16.731Z",
                      "id": "642000041e840f2c62fcbe73"
                  }
              ]
          }
      }
    title: Response
    language: json
---
