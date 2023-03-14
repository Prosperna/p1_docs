---
title: /v1/orders
position_number: 1.1
type: post
description: Create Order
content_markdown: |-
  | Parameters         | Data Type | Required | Description                        |
  |--------------------|-----------|----------|------------------------------------|
  | store_id           | string    | Yes      | ID of the Store                    |
  | customer_id        | string    | Yes      | ID of the Consumer                 |
  | cart_id            | string    | Yes      | ID of the Cart of Consumer         |
  | urls               | object    | Yes      | Redirection URLs for Order API result. Possible values: { "success_redirect_url": "https://www.google.com/search?q=success", "failure_redirect_url": "https://www.google.com/search?q=failed", "cancel_redirect_url": "https://www.google.com/search?q=cancel" }          |
  | order_information  | object    | Yes      | Possible values: { "fname": "Juan", "lname": "Dela Cruz", "email_address": "email@email.com", "phone": "639685432321", "address_line": "Star Building", "state": "METRO-MANILA", "city": "BINONDO", "barangay": "BARANGAY 287", "zip_code": "1234", "note": "" }                     |
  | shipping_information | object  | Yes      | Possible values: { "type": (Possible types: "STANDARD_JNT", "OWN_BOOKING", "PICKUP", "SAMEDAY_SCHED_LALAMOVE") }|
  | dimensions           | object  | Yes      | Dimensions of the Ordered Product. Possible values: { "actual_weight": 12, "volumetric_weight": 8.0905 } |
  | payment_information | object  | Yes      | Possible values: { "type": (Possible types: "EWALLET", "OVER_THE_COUNTER", "COP", "COD", "CREDIT_CARD") }|
  | fees                | object  | Yes      | Possible values: { "convenience_fee": 0, "convenience_fee_customer": 0, "shipping_fee": 0, "additional_fee": 0 }|

left_code_blocks:
  - code_block: |-
      var axios = require('axios');
        var data = JSON.stringify({
        "store_id": "637de5eab94b30555121f36c",
        "customer_id": "453c955e-ae65-4975-8bf1-c8dd98892c60",
        "cart_id": "640ebf13dc76cdcd5c0c0e03",
        "urls": {
            "success_redirect_url": "https://starcomputers.prodev.prosperna.ph/checkout/thank-you",
            "failure_redirect_url": "https://starcomputers.prodev.prosperna.ph/products",
            "cancel_redirect_url": "https://starcomputers.prodev.prosperna.ph/products"
        },
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
            "quotation": {}
        },
        "shipping_information": {
            "type": "STANDARD_JNT"
        },
        "dimensions": {
            "actual_weight": 12,
            "volumetric_weight": 8.0905
        },
        "payment_information": {
            "type": "COD"
        },
        "fees": {
            "convenience_fee": 0,
            "convenience_fee_customer": 0,
            "shipping_fee": 0,
            "additional_fee": 0
        }
        });

        var config = {
        method: 'post',
        maxBodyLength: Infinity,
        url: 'https://api.prosperna.com/v1/orders/',
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

    title: NodeJs
    language: javascript
  
right_code_blocks:
  - code_block: |-
      {
        "store_id": "637de5eab94b30555121f36c",
        "customer_id": "453c955e-ae65-4975-8bf1-c8dd98892c60",
        "cart_id": "640ebf13dc76cdcd5c0c0e03",
        "urls": {
            "success_redirect_url": "https://starcomputers.prodev.prosperna.ph/checkout/thank-you",
            "failure_redirect_url": "https://starcomputers.prodev.prosperna.ph/products",
            "cancel_redirect_url": "https://starcomputers.prodev.prosperna.ph/products"
        },
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
            "quotation": {}
        },
        "shipping_information": {
            "type": "STANDARD_JNT"
        },
        "dimensions": {
            "actual_weight": 12,
            "volumetric_weight": 8.0905
        },
        "payment_information": {
            "type": "COD"
        },
        "fees": {
            "convenience_fee": 0,
            "convenience_fee_customer": 0,
            "shipping_fee": 0,
            "additional_fee": 0
        }
       }
    title: Request
    language: json
  - code_block: |-
      {
            "data": {
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
                    "reference_number": "N/A"
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
                "has_been_disbursed_to_merchant": false,
                "requested_for_disbursement": false,
                "disbursement_status": "ACCEPTED",
                "disbursement_updated_by": [],
                "createdAt": "2023-03-14T01:08:58.387Z",
                "updatedAt": "2023-03-14T01:08:58.387Z",
                "id": "640fc92a2742e57a81038b09",
                "total_order_amount": 1000,
                "cart_list": [
                    {
                        "store_id": "637de5eab94b30555121f36c",
                        "product_slug": null,
                        "product_id": "640576472a33e0ca3c940d0c",
                        "customer_id": "453c955e-ae65-4975-8bf1-c8dd98892c60",
                        "is_guest": true,
                        "cart_quantity": 1,
                        "item_sub_total": 1000,
                        "addon_ids": [],
                        "product_variant_combination_id": "",
                        "createdAt": "2023-03-14T01:08:45.604Z",
                        "updatedAt": "2023-03-14T01:08:45.604Z",
                        "id": "640fc91d2742e57a81038b05",
                        "dev_ref_id": "640fc91d2742e57a81038b05",
                        "published": true,
                        "selected_variant_combination_data": null,
                        "product_data": {
                            "product_seo": {
                                "primary": {
                                    "title": "",
                                    "description": "",
                                    "url": "https://starcomputers.prodev.prosperna.ph/product/gaming-package-1"
                                }
                            },
                            "product_specification": {
                                "name": "Gaming Package 1",
                                "slug": "gaming-package-1",
                                "brand": "",
                                "short_description": "Entry Level Gaming Rig",
                                "long_description": "<p>Entry Level Gaming Rig</p>",
                                "images": [
                                    {
                                        "image": "https://p1-mediaserver.s3.ap-southeast-1.amazonaws.com/business/store/starcomputers/1678079639624-shopping.png",
                                        "original_name": "shopping.png",
                                        "type": "images/png",
                                        "name_with_path": "business/store/starcomputers/1678079639624-shopping.png",
                                        "position": 0,
                                        "id": "640576972a33e0ca3c940d27"
                                    }
                                ]
                            },
                            "product_state": {
                                "is_product_has_variants": false,
                                "is_hide_stock": false,
                                "is_always_instock": false,
                                "is_published": true
                            },
                            "product_measurements": {
                                "product_size": {
                                    "height": 12,
                                    "length": 12,
                                    "width": 12,
                                    "unit": "in"
                                },
                                "product_weight": {
                                    "weight": 12,
                                    "unit": "kg"
                                }
                            },
                            "product_price": {
                                "regular_price": 1000,
                                "sale_price": 0,
                                "price_display": "",
                                "unit_cost": 0,
                                "margin": 0,
                                "stock_quantity": 981
                            },
                            "product_addons": {
                                "addOn_limit": 0,
                                "addOn_list": []
                            },
                            "product_categories": [
                                {
                                    "name": "Gaming PC",
                                    "id": "63f4221681bfa92d923d45f1"
                                }
                            ],
                            "product_variant_types": [],
                            "product_type": "PHYSICAL",
                            "createdAt": "2023-03-06T05:12:39.534Z",
                            "updatedAt": "2023-03-13T06:47:16.677Z",
                            "id": "640576472a33e0ca3c940d0c",
                            "store_id": "637de5eab94b30555121f36c",
                            "product_variants_combinations": []
                        },
                        "selected_addon_data": []
                    }
                ],
                "ordered_items_list": [
                    {
                        "order_id": "640fc92a2742e57a81038b08",
                        "store_id": "637de5eab94b30555121f36c",
                        "product_slug": null,
                        "product_id": "640576472a33e0ca3c940d0c",
                        "dev_ref_id": "640fc92a2742e57a81038b0b",
                        "customer_id": "453c955e-ae65-4975-8bf1-c8dd98892c60",
                        "is_guest": true,
                        "cart_quantity": 1,
                        "item_sub_total": 1000,
                        "addon_ids": [],
                        "product_variant_combination_id": "",
                        "selected_variant_combination_data": null,
                        "product_data": {
                            "product_seo": {
                                "primary": {
                                    "title": "",
                                    "description": "",
                                    "url": "https://starcomputers.prodev.prosperna.ph/product/gaming-package-1"
                                }
                            },
                            "product_specification": {
                                "name": "Gaming Package 1",
                                "slug": "gaming-package-1",
                                "brand": "",
                                "short_description": "Entry Level Gaming Rig",
                                "long_description": "<p>Entry Level Gaming Rig</p>",
                                "images": [
                                    {
                                        "image": "https://p1-mediaserver.s3.ap-southeast-1.amazonaws.com/business/store/starcomputers/1678079639624-shopping.png",
                                        "original_name": "shopping.png",
                                        "type": "images/png",
                                        "name_with_path": "business/store/starcomputers/1678079639624-shopping.png",
                                        "position": 0,
                                        "id": "640576972a33e0ca3c940d27"
                                    }
                                ]
                            },
                            "product_state": {
                                "is_product_has_variants": false,
                                "is_hide_stock": false,
                                "is_always_instock": false,
                                "is_published": true
                            },
                            "product_measurements": {
                                "product_size": {
                                    "height": 12,
                                    "length": 12,
                                    "width": 12,
                                    "unit": "in"
                                },
                                "product_weight": {
                                    "weight": 12,
                                    "unit": "kg"
                                }
                            },
                            "product_price": {
                                "regular_price": 1000,
                                "sale_price": 0,
                                "price_display": "",
                                "unit_cost": 0,
                                "margin": 0,
                                "stock_quantity": 981
                            },
                            "product_addons": {
                                "addOn_limit": 0,
                                "addOn_list": []
                            },
                            "product_categories": [
                                {
                                    "name": "Gaming PC",
                                    "id": "63f4221681bfa92d923d45f1"
                                }
                            ],
                            "product_variant_types": [],
                            "product_type": "PHYSICAL",
                            "createdAt": "2023-03-06T05:12:39.534Z",
                            "updatedAt": "2023-03-13T06:47:16.677Z",
                            "id": "640576472a33e0ca3c940d0c",
                            "store_id": "637de5eab94b30555121f36c",
                            "product_variants_combinations": []
                        },
                        "selected_addon_data": [],
                        "createdAt": "2023-03-14T01:08:45.604Z",
                        "updatedAt": "2023-03-14T01:08:45.604Z",
                        "id": "640fc92a2742e57a81038b0b"
                    }
                ]
            },
            "message": "Order created successfully"
        }
    title: Response
    language: json
  - code_block: |-
      {
            "name": "Error",
            "message": "Cart data invalid."
        }
    title: Error
    language: json
---
