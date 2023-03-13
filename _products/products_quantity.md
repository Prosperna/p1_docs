---
title: /v1/products/stock-quantity?store_id=
position_number: 1.6
type: post
description: Decrease the product quantity and product variant combination quantity

content_markdown: |-
  | ***Request body***         | ***Data Type*** | ***Required*** | ***Description***                        |
  |--------------------|-----------|----------|------------------------------------|
  |                | array    | Yes      | Array of objects with the product id/variant combinationation id and the quantity that will be deducted. |

  ```
    Example request body.

    [
        {
          "product_id": "63e4f4fabf61b3a5047d9da4",
          "purchased_quantity": 9
        },
        {
          "purchased_quantity": 5,
          "product_variant_combination_id": "63e64f99ca104a61440fd50b"
        }
    ]
  ``` 

  | ***Query Parameters***         | ***Data Type*** | ***Required*** | ***Description***                        |
  |--------------------|-----------|----------|------------------------------------|
  | store_id               | string    | Yes      | Merchant store id            |

left_code_blocks:
  - code_block: |-
      var axios = require('axios');
      var data = JSON.stringify([
        {
          "product_id": "63e4f4fabf61b3a5047d9da4",
          "purchased_quantity": 9
        },
        {
          "purchased_quantity": 5,
          "product_variant_combination_id": "63e64f99ca104a61440fd50b"
        }
      ]);

      var config = {
        method: 'post',
        url: 'api.prosperna.com/v1/products/stock-quantity?store_id=639749a5cb1db88617891bf0',
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
          "data": null,
          "message": "Inventory successfully updated.",
          "statusCode": 200
      }
    title: Response
    language: json
---
