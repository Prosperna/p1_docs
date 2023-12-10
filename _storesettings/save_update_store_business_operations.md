---
title: /business-profile/store/update/store-business-operations
position_number: 2.2
type: put
description: Save/update business operations settings

content_markdown: |-
  | ***Request Body***         | ***Data Type*** | ***Required*** | ***Description*** |
  |--------------------|-----------|----------|------------------------------------|
  | business_operation_type | string    | Yes      | Type of business operation (Possible values: rfq', 'add_to_cart', 'disabled') |
  | contact_form            | string    | Yes (for rfq)       | Contact form URL. |
  | btn_name                | string    | Yes (for rfq)       | Button name request for quotation. |

left_code_blocks:
  - code_block: |-
      var axios = require('axios');
      var data = JSON.stringify({
        "business_operation_type": "rfq",
        "contact_form": "https://contact-form.com",
        "btn_name": "Request for Quotation",
      });

      var config = {
        method: 'put',
        url: 'api.prosperna.com/v1/business-profile/store/update/store-business-operations',
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
          "success": true,
          "message": "Succesfully updated business operations settings.",
          "data": null
      }
    title: Response
    language: json
---
