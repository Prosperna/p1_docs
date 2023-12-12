---
title: 'payments/balances/merchants/withdraw'
position_number: 1.2
type: post
description: 'Withdraw balances'

content_markdown: |-
  | **Request Body**          | ***Data Type*** | ***Required*** | ***Description***                                          |
  |---------------------------|---------------|--------------|----------------------------------------------------------|
  | amount             | number        | Yes          | Withdrawal amount, limits to Php250 minimum and Php50000 maximum per transaction.                                 |
  | otp_code             | number        | Yes          | Valid OTP code sent to merchant's mobile number.                                 |

left_code_blocks:
  - code_block: |-
      var axios = require('axios');

      var config = {
        method: 'post',
        url: 'api.prosperna.com/v1/payments/balances/merchants/withdraw',
        data: {
          "amount": 1000,
          "otp_code": 123456
        }
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
        "message": "Your available balance of PhP 1000.00 has been withdrawn. The funds may reflect in your account in "real-time" or within 3 business days, depending on the financial institution you have chosen for settlement.",
        "data": {
          "amount": 1000,
          "withdrawal_amount": 970,
          "admin_fee": 30,
          "expected_arrival:"2023-12-31T23:59:59.999Z"
        }          
      }
    title: Response
    language: json
---
