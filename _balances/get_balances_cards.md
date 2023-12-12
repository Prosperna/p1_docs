---
title: 'payments/balances/merchants'
position_number: 1.3
type: get
description: 'Get balances breakdown'

left_code_blocks:
  - code_block: |-
      var axios = require('axios');

      var config = {
        method: 'get',
        url: 'api.prosperna.com/v1/payments/balances/merchants'
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
        "message": "",
        "data": {
          "available_balance": 5000,
          "pending_balance": 0,
          "lifetime_orders": 5000,
          "total_withdrawal_history: 0
        }          
      }
    title: Response
    language: json
---
