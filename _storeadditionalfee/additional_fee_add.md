---
title: /business-profile/store/additional-fee
position_number: 1.0
type: post
description: Add new additional fee

content_markdown: |-
  | ***Request Body***         | ***Data Type*** | ***Required*** | ***Description*** |
  |--------------------|-----------|----------|------------------------------------|
  | description               | string    | Yes      | Description of the additional fee |
  | price               | number    | Yes      | Additional fee amount |
  | is_set               | boolean    | No      | Flag used to set as active or not this new additinal fee. |

left_code_blocks:
  - code_block: |-
      var axios = require('axios');
      var data = JSON.stringify({
        "description": "Additional fee description",
        "price": 12,
        "is_set": false
      });

      var config = {
        method: 'post',
        url: 'api.prosperna.com/v1/business-profile/store/additional-fee',
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
          "message": "Successfully created additional fee.",
          "data": {
              "id": "642000041e840f2c62fcbe73",
              "description": "Additional fee description",
              "price": 12,
              "is_set": false
          }
      }
    title: Response
    language: json
---
