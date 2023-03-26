---
title: /business-profile/store/digital-products/payment-settings
position_number: 1.0
type: put
description: Save and update digital product payment settings

content_markdown: |-
  | ***Request Body***         | ***Data Type*** | ***Required*** | ***Description*** |
  |--------------------|-----------|----------|------------------------------------|
  | BANK_TRANSFER               | boolean    | Yes      | Determines if bank transfer is accepted as payment option for digital products purchases. |
  | E_WALLET               | boolean    | Yes      | Determines if e-wallet is accepted as payment option for digital products purchases. |
  | CREDIT_CARD               | boolean    | Yes      | Determines if credit card is accepted as payment option for digital products purchases. |
  | OVER_THE_COUNTER               | boolean    | Yes      | Determines if over-the-counter is accepted as payment option for digital products purchases. |

left_code_blocks:
  - code_block: |-
      var axios = require('axios');
      var data = JSON.stringify({
        "BANK_TRANSFER": true,
        "E_WALLET": false,
        "CREDIT_CARD": true,
        "OVER_THE_COUNTER": true
      });

      var config = {
        method: 'put',
        url: 'api.prosperna.com/v1/business-profile/store/digital-products/payment-settings',
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
          "message": "Successfully updated digital product payment settings.",
          "data": {
              "digital_payment_options": {
                  "store_id": "63760ee5a3444c4d444c158c",
                  "createdAt": "2023-03-03T03:12:46.392Z",
                  "payment_options": {
                      "BANK_TRANSFER": true,
                      "E_WALLET": false,
                      "CREDIT_CARD": true,
                      "OVER_THE_COUNTER": true
                  },
                  "updatedAt": "2023-03-26T11:34:38.719Z",
                  "id": "640165ae27495b7b2574aeaa"
              }
          }
      }
    title: Response
    language: json
---
