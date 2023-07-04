---
title: /business-profile/shipping/:store_id/pickup-address/:pickup_address_id
position_number: 1.6
type: delete
description: Delete pickup address

content_markdown: |-
  | ***Request parameters***         | ***Data Type*** | ***Required*** | ***Description*** |
  |--------------------|-----------|----------|------------------------------------|
  | store_id               | string    | Yes      | Store id  |
  | pickup_address_id               | string    | Yes      | Pickup address id  |

left_code_blocks:
  - code_block: |-
      var axios = require('axios');

      var config = {
        method: 'delete',
        url: 'api.prosperna.com/v1/business-profile/shipping/639749a5cb1db88617891bf1/pickup-address/63d26a14a254f44dbf2fce3c',
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
          "message": "Successfully deleted pickup address.",
      }
    title: Response
    language: json
---
