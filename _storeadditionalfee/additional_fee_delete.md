---
title: /business-profile/store/additional-fee/:additional_fee_id
position_number: 1.3
type: delete
description: Delete additional fee

content_markdown: |-
  | ***Request Body***         | ***Data Type*** | ***Required*** | ***Description*** |
  |--------------------|-----------|----------|------------------------------------|
  | additional_fee_id               | string    | Yes      | Id of the additional fee to be deleted |

left_code_blocks:
  - code_block: |-
      var axios = require('axios');

      var config = {
        method: 'delete',
        url: 'api.prosperna.com/v1/business-profile/store/additional-fee/641a7ff47f8d70fb9f757509',
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
          "message": "Successfully deleted additional fee."
      }
    title: Response
    language: json
---
