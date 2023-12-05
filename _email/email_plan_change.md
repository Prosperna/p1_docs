---
title: '/email/billing/plan-change'
position_number: 1.1
type: post
description: 'Send plan change billing emails'

content_markdown: |-
  | **Request Body**          | ***Data Type*** | ***Required*** | ***Description***                                          |
  |---------------------------|---------------|--------------|----------------------------------------------------------|
  | merchant_name             | string        | Yes          | The name of the merchant.                                 |
  | merchant_email            | string        | Yes          | The email of the merchant.                                |
  | subject                   | string        | Yes          | The subject of the email.                                 |
  | plan_expiration_date      | string        | Yes          | The expiration date of the subscription plan.             |
  | plan_action               | string        | Yes          | The action to be taken regarding the subscription plan. Possible values: `plan_upgrade`, `plan_renew`, `plan_change` |
  | billing_url               | string        | Yes          | The URL link to the billing or invoice page.              |
  | current_plan              | string        | Yes          | The current subscription plan. Possible values: `FREE`, `PLUS`, `PRO`, `PREMIUM`, `PREMIUM TRIAL` |
  | previous_plan             | string        | Yes          | The previous subscription plan. Possible values: `FREE`, `PLUS`, `PRO`, `PREMIUM`, `PREMIUM TRIAL` |
  | billing_type              | string        | Yes          | The type of billing. Possible values: `MONTHLY`, `QUARTERLY`, `ANNUAL` |

left_code_blocks:
  - code_block: |-
      var axios = require('axios');

      var config = {
        method: 'post',
        url: 'api.prosperna.com/v1/email/billing/plan-change',
        data: {
         merchant_name: 'merchant_name',
         merchant_email: 'merchant@example.com',
         subject: 'Your Email Subject',
         plan_expiration_date: '2023-12-31',
         plan_action: 'plan_upgrade',
         billing_url: 'https://p1.prosperna.com/home/billing?tab=invoices',
         current_plan: 'PRO',
         previous_plan: 'FREE',
         billing_type: 'MONTHLY'
       }
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
        "message": "Ok",
        "data": null          
      }
    title: Response
    language: json
---
