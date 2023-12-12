---
title: 'payments/balances/merchants/order-breakdowns'
position_number: 1.4
type: get
description: 'Get payment order breakdowns'

content_markdown: |-
  | Query Parameters         | Data Type | Required | Description                        |
  |--------------------|-----------|----------|------------------------------------|
  | balance_type           | string    | Yes      | Type of balance to be queried, values must be either 'pending_order' or 'lifetime_orders'                 |
  | min_date           | Date    | No      | Minimum date filter.                    |
  | max_date           | Date    | No      | Maximum date filter.                    |
  | search           | string    | No      | Search filter for order id.                    |
  | page           | number    | No      | Page for pagination. |
  | limit           | number    | No      | Number of records per page. |

left_code_blocks:
  - code_block: |-
      var axios = require('axios');

      var config = {
        method: 'get',
        url: 'api.prosperna.comv1/payments/balances/merchants/order-breakdowns?balance_type=pending_orders&min_date=2023-06-17&max_date=2023-06-17&search=&page=1&limit=10',
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
        "statusCode": 200,
        "message": "",
        "data": {
          "order_breakdowns": [
            {
                "order_id": "65241f47500c18505c900333",
                "store_id": "639749a5cb1db88617891333",
                "customer_name": "Merchant name",
                "payment_type": "CREDIT_CARD",
                "shipping_type": "Same Day",
                "amount": 268.45,
                "order_payment_date": "2023-10-09T15:42:00.865Z"
            }
          ],
          "pagination": {
              "totalDocs": 2,
              "limit": 10,
              "page": 1,
              "totalPages": 1,
              "pagingCounter": 1,
              "hasPrevPage": false,
              "hasNextPage": false,
              "prevPage": null,
              "nextPage": null
          }
        }          
      }
    title: Response
    language: json
---
