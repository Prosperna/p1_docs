---
title: 'payments/balances/merchants/send-otp'
position_number: 1.1
type: put
description: 'Send OTP'

left_code_blocks:
  - code_block: |-
      var axios = require('axios');

      var config = {
        method: 'put',
        url: 'api.prosperna.com/v1/payments/balances/merchants/send-otp',
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
        "statusCode": 200,
        "message": "Successfully sent otp code.",
        "data": {
          "valid_until:"2023-12-31T23:59:59.999Z",
          "mobile_number": "+639658745878"
          "is_valid_otp": true,
          "remaining_otp_resends": 2
        }          
      }
    title: Response
    language: json
---
