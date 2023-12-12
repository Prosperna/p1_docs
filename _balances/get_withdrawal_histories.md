---
title: 'payments/balances/merchants/withdrawal-history'
position_number: 1.5
type: get
description: 'Get merchant withdrawal histories'

content_markdown: |-
  | Query Parameters         | Data Type | Required | Description                        |
  |--------------------|-----------|----------|------------------------------------|
  | min_date           | Date    | No      | Minimum date filter.                    |
  | max_date           | Date    | No      | Maximum date filter.                    |
  | search           | string    | No      | Search filter for amount, bank name, transaction id, reference id and status.                   |
  | bank           | string    | No      | Filter by bank. Valid bank names are 'UNIONBANK', 'BDO', 'BPI', and 'GCASH'.   |
  | status           | string    | No      | Filter by status. Valid status are 'Completed', 'Pending', 'Cancelled', 'Failed', 'Disputed'. |
  | page           | number    | No      | Page for pagination. |
  | limit           | number    | No      | Number of records per page. |

left_code_blocks:
  - code_block: |-
      var axios = require('axios');

      var config = {
        method: 'get',
        url: 'api.prosperna.com/v1/payments/balances/merchants/withdrawal-history?page=2&limit=56&search=&min_date=2023-04-23&max_date=2023-04-26&status=Completed&bank=BPI',
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
          "withdrawal_history": [
            {
                "transaction_counter": 30,
                "transaction_id": "disb-5e718a53-3f02-4d7c-80f8-33333333333",
                "reference_id": "P1-DISBURSE-602c3afd-7929-4885-a22f-33333333333",
                "withdrawal_date": "2023-09-01T05:09:10.437Z",
                "expected_arrival": "2023-09-04T05:09:10.437Z",
                "withdrawal_amount": 1000,
                "bank_name": "UNIONBANK",
                "account_number": "6**************2",
                "status": "Completed",
                "id": "64f171f63ce0beff8705b333",
                "store_id": "639749a5cb1db88617891333"
            },
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
