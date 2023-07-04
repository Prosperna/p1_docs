---
title: /business-profile/shipping/settings/:store_id/guest-checkout-verification
position_number: 1.4
type: patch
description: Toggle on and off guest checkout verification

content_markdown: |-
  | ***Request parameters***         | ***Data Type*** | ***Required*** | ***Description*** |
  |--------------------|-----------|----------|------------------------------------|
  | store_id               | string    | Yes      | Store id  |

left_code_blocks:
  - code_block: |-
      var axios = require('axios');

      var config = {
        method: 'patch',
        url: 'api.prosperna.com/v1/business-profile/shipping/settings/63861440e2c90910a117e826/guest-checkout-verification',
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
          "message": "Successfully updated shipping settings."
      }
    title: Response
    language: json
---
