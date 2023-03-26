---
title: /business-profile/shipping/settings/:store_id/toggle?shipping_type_option=
position_number: 1.3
type: patch
description: Toggle on and off shipping setting

content_markdown: |-
  | ***Request parameters***         | ***Data Type*** | ***Required*** | ***Description*** |
  |--------------------|-----------|----------|------------------------------------|
  | store_id               | string    | Yes      | Store id  |
  | ***Query Parameters***         | ***Data Type*** | ***Required*** | ***Description*** |
  |--------------------|-----------|----------|------------------------------------|
  | shipping_type_option               | string    | Yes      | Shipping type option. Values are **OWN_BOOKING**, **SAMEDAY_SCHED**, **STANDARD**, **PICKUP**  |

left_code_blocks:
  - code_block: |-
      var axios = require('axios');

      var config = {
        method: 'patch',
        url: 'api.prosperna.com/v1/business-profile/shipping/settings/63861440e2c90910a117e826/toggle?shipping_type_option=SAMEDAY_SCHED',
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
