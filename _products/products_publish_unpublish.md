---
title: /v1/products/status
position_number: 1.7
type: post
description: Publish or unpublish products, accepts array of product id

content_markdown: |-
  | ***Request body***         | ***Data Type*** | ***Required*** | ***Description***                        |
  |--------------------|-----------|----------|------------------------------------|
  |                | array    | Yes      | Array of product ids. |

  ```
    Example request body.

    ["63e4f4fabf61b3a5047d9da4", "63e64f99ca104a61440fd50b"]
  ``` 

  | ***Query Parameters***         | ***Data Type*** | ***Required*** | ***Description***                        |
  |--------------------|-----------|----------|------------------------------------|
  |  action               | string    | Yes      | publish or unpublish           |

left_code_blocks:
  - code_block: |-
      var axios = require('axios');
      var data = JSON.stringify([
        "639584fdde9e74b0a80d1606"
      ]);

      var config = {
        method: 'post',
        url: 'api.prosperna.com/v1/products/status?action=publish',
        data: data
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
              "publishedProducts": 10,
              "storePlan": "PLUS",
              "eligibleProductsToPublish": "40"
          },
          "message": "published",
          "statusCode": 200
      }
    title: Response
    language: json
---
