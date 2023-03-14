---
title: /order/:id
position_number: 1.3
type: delete
description: Deletes a Order
content_markdown: |-
  | Query Parameters         | Data Type | Required | Description                        |
  |--------------------|-----------|----------|------------------------------------|
  | sid           | string    | Yes      | ID of the Store                    |
  | cid           | string    | Yes      | ID of the Consumer                    |
  
  | Path Variables         | Data Type | Required | Description                        |
  |--------------------|-----------|----------|------------------------------------|
  | order_id           | string    | Yes      | ID of the Order                    |

  Deletes a order in your collection.
left_code_blocks:
  - code_block: |-
        var axios = require('axios');

        var config = {
        method: 'delete',
        maxBodyLength: Infinity,
        url: 'https://api.dev.prosperna.ph/v1/orders/6395690183b8967af19222f9?sid=6386ae5dba4bf984402d848e&cid=3945a7bb-b2d9-4b6c-8d41-2db4d56fc4ec'
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
  - code_block: |2-
      {
            "message": "Delete successful"
        }
    title: Response
    language: json
---
