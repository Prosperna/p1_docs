---
title: /order_id?sid=""&cid=""
position_number: 1.3
type: post
description: Update Order
content_markdown: |-
  | Query Parameters         | Data Type | Required | Description                        |
  |--------------------|-----------|----------|------------------------------------|
  | sid           | string    | Yes      | ID of the Store                    |
  | cid           | string    | Yes      | ID of the Consumer                    |
  
  | Path Variables         | Data Type | Required | Description                        |
  |--------------------|-----------|----------|------------------------------------|
  | order_id           | string    | Yes      | ID of the Order                    |

  | Parameters         | Data Type | Required | Description                        |
  |--------------------|-----------|----------|------------------------------------|
  | store_id           | string    | No      | ID of the Store                    |
  | customer_id        | string    | No      | ID of the Consumer                 |
  | cart_id            | string    | No      | ID of the Cart of Consumer         |
  | urls               | object    | No      | Redirection URLs for Order API result. Possible values: { "success_redirect_url": "https://www.google.com/search?q=success", "failure_redirect_url": "https://www.google.com/search?q=failed", "cancel_redirect_url": "https://www.google.com/search?q=cancel" }          |
  | order_information  | object    | No      | Possible values: { "fname": "Juan", "lname": "Dela Cruz", "email_address": "email@email.com", "phone": "639685432321", "address_line": "Star Building", "state": "METRO-MANILA", "city": "BINONDO", "barangay": "BARANGAY 287", "zip_code": "1234", "note": "" }                     |
  | shipping_information | object  | No      | Possible values: { "type": (Possible types: "STANDARD_JNT", "OWN_BOOKING", "PICKUP", "SAMEDAY_SCHED_LALAMOVE") }|
  | dimensions           | object  | No      | Dimensions of the Ordered Product. Possible values: { "actual_weight": 12, "volumetric_weight": 8.0905 } |
  | payment_information | object  | No      | Possible values: { "type": (Possible types: "EWALLET", "OVER_THE_COUNTER", "COP", "COD", "CREDIT_CARD") }|
  | fees                | object  | No      | Possible values: { "convenience_fee": 0, "convenience_fee_customer": 0, "shipping_fee": 0, "additional_fee": 0 }|

left_code_blocks:
  - code_block: |-
        var axios = require('axios');
        var data = JSON.stringify({
        "delivery_information": {
            "vehicle_type": "N/A",
            "status": "N/A",
            "reference_number": "167180805411"
        }
        });

        var config = {
        method: 'patch',
        maxBodyLength: Infinity,
        url: 'https://api.prosperna.com/v1/orders/640fc92a2742e57a81038b09?sid=637de5eab94b30555121f36c&cid=453c955e-ae65-4975-8bf1-c8dd98892c60',
        headers: { 
            'Content-Type': 'application/json'
        },
        data : data
        };

        axios(config)
        .then(function (response) {
        console.log(JSON.stringify(response.data));
        })
        .catch(function (error) {
        console.log(error);
        });

        title: Request
        language: json
    title: NodeJs
    language: javascript

right_code_blocks:
  - code_block: |-
      {
            "data": {
                "order_information": {
                    "fname": "TEST",
                    "lname": "ORDER",
                    "email_address": "ian+637de5eab94b30555121f36c@prosperna.com",
                    "phone": "639685432321",
                    "address_line": "sdasdasd",
                    "state": "METRO-MANILA",
                    "city": "BINONDO",
                    "barangay": "BARANGAY 287",
                    "zip_code": "sdasdasd",
                    "note": "PRO1-DISABLE-JNT-56770644-c14b-11ed-afa1-0242ac120002",
                    "status": "Accepted",
                    "landmark": "N/A"
                },
                "payment_information": {
                    "type": "COD",
                    "status": "Awaiting Payment",
                    "gateway": "N/A",
                    "reference_id": "N/A"
                },
                "shipping_information": {
                    "type": "Standard Delivery",
                    "shipped_by": "JNT"
                },
                "delivery_information": {
                    "vehicle_type": "N/A",
                    "status": "N/A",
                    "reference_number": "167180805411"
                },
                "fees": {
                    "convenience_fee": 0,
                    "convenience_fee_customer": 0,
                    "shipping_fee": 0,
                    "payment_gateway_fee": 0,
                    "additional_fee": 0
                },
                "dimensions": {
                    "actual_weight": 12,
                    "volumetric_weight": 8.0905
                },
                "order_id": "640fc92a2742e57a81038b08",
                "store_id": "637de5eab94b30555121f36c",
                "customer_id": "453c955e-ae65-4975-8bf1-c8dd98892c60",
                "cart_ids": [
                    "640fc91d2742e57a81038b05"
                ],
                "ordered_item_ids": [],
                "is_trashed": false,
                "order_total_amount": 1000,
                "order_subtotal_amount": 1000,
                "order_total_qty": 1,
                "has_been_disbursed_to_merchant": false,
                "requested_for_disbursement": false,
                "disbursement_status": "ACCEPTED",
                "disbursement_updated_by": [],
                "createdAt": "2023-03-14T01:08:58.387Z",
                "updatedAt": "2023-03-14T01:22:33.305Z",
                "id": "640fc92a2742e57a81038b09"
            },
            "message": "Order updated successfully"
        }
    title: Response
    language: json
  - code_block: |-
      {
            "name": "Error",
            "message": "Failed to update order."
        }
    title: Error
    language: json
---
