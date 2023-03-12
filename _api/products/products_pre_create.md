---
title: /v1/products/pre-create
position_number: 1.2
type: post
description: Pre create product
parameters:
  - name: product_type
    content: Type of product either 'physical' or 'digital'.
left_code_blocks:
  - code_block: |-
      var axios = require('axios');
      var data = '';

      var config = {
        method: 'post',
        url: 'api.prosperna.com/v1/products/pre-create?product_type=physical',
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
          "data": {
              "id": "640da6e972daff1949be2a16",
              "product_type": "physical"
          },
          "message": "Product pre created.",
          "statusCode": 201
      }
    title: Response
    language: json
---
