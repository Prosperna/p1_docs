---
title: /business-profile/shipping/settings/:store_id
position_number: 1.2
type: put
description: Save/update shipping setting of a given store

content_markdown: |-
  | ***Request parameters***         | ***Data Type*** | ***Required*** | ***Description*** |
  |--------------------|-----------|----------|------------------------------------|
  | store_id               | string    | Yes      | Store id  |
  | ***Request Body***         | ***Data Type*** | ***Required*** | ***Description*** |
  |--------------------|-----------|----------|------------------------------------|
  | shipping_option               | string    | Yes      | Shipping provider. Values are **OWN_BOOKING**, **LALAMOVE**, **LBC**, **PICKUP**, **J&T**  |
  | payment_options.BANK_TRANSFER               | boolean    | Yes      | Determines if bank transfer is enabled for a given shipping option.  |
  | payment_options.COD               | boolean    | Yes      | Determines if cash-on-delivery is enabled for a given shipping option.  |
  | payment_options.E_WALLET               | boolean    | Yes      | Determines if e-wallet payment is enabled for a given shipping option.  |
  | payment_options.CREDIT_CARD               | boolean    | Yes      | Determines if credit card payment is enabled for a given shipping option.  |
  | payment_options.OVER_THE_COUNTER               | boolean    | Yes      | Determines if over-the-counter payment is enabled for a given shipping option.  |
  | pickup_address               | string    | Yes      | Pickup address id.  |

left_code_blocks:
  - code_block: |-
      var axios = require('axios');
      var data = JSON.stringify({
      "shipping_option": "LBC",
      "payment_options": {
          "BANK_TRANSFER": true,
          "COD": true,
          "COP": false,
          "E_WALLET": false,
          "CREDIT_CARD": false,
          "OVER_THE_COUNTER": false
      },
      "pickup_address": "63989075f681e6a270814754"
      });

      var config = {
      method: 'put',
      url: 'api.prosperna.com/v1/business-profile/shipping/settings/6386ae5dba4bf984402d848e',
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
          "message": "Successfully updated shipping settings."
      }
    title: Response
    language: json
---
