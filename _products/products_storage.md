---
title: /v1/products/storage
position_number: 1.5
type: get
description: Storage breakdown for product usage
left_code_blocks:
  - code_block: |-
      var axios = require('axios');

      var config = {
        method: 'get',
        url: 'api.prosperna.com/v1/products/storage',
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
          "data": {
              "total_consumed": {
                  "gb": 0,
                  "mb": 0.94
              },
              "store_allocation": {
                  "gb": 25,
                  "mb": 25600
              },
              "remaining_space": {
                  "gb": 25,
                  "mb": 25599.06
              }
          },
          "message": "",
          "statusCode": 200
      }
    title: Response
    language: json
---
