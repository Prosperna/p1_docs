---
title: /business-profile/store/additional-fee/:additional_fee_id
position_number: 1.2
type: put
description: Update additional fee

content_markdown: |-
  | ***Request Body***         | ***Data Type*** | ***Required*** | ***Description*** |
  |--------------------|-----------|----------|------------------------------------|
  | additional_fee_id               | string    | Yes      | Id of the additional fee to be updated |

left_code_blocks:
  - code_block: |-
      var axios = require('axios');
      var data = JSON.stringify({
        "description": "Updated additional fee description",
        "price": 23,
        "is_set": false
      });

      var config = {
        method: 'put',
        url: 'api.prosperna.com/v1/business-profile/store/additional-fee/641a7ff47f8d70fb9f757509',
        
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
          "message": "Successfully updated additional fee."
      }
    title: Response
    language: json
---
