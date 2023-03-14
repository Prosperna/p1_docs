---
title: /v1/products/:product_id
position_number: 1.4
type: delete
description: Delete single product
content_markdown: |-
  | Parameters         | Data Type | Required | Description                        |
  |--------------------|-----------|----------|------------------------------------|
  | product_id               | string    | Yes      | Product id                |

left_code_blocks:
  - code_block: |-
      var axios = require('axios');
      var data = '';

      var config = {
        method: 'delete',
        url: 'api.prosperna.com/v1/products/:product_id'
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
          "data": null,
          "message": "Successfully updated product.",
          "statusCode": 200
      }
    title: Response
    language: json
---
