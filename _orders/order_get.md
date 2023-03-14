---
title: /store?sid={store_id}
position_number: 1.2
type: get
description: Get Store Orders
parameters:
  - name:
    content:
content_markdown: |-
  | Parameters         | Data Type | Required | Description                        |
  |--------------------|-----------|----------|------------------------------------|
  | store_id           | string    | Yes      | ID of the Store                    |

  Returns all orders from your store
left_code_blocks:
  - code_block: |-
      var axios = require('axios');

      var config = {
        method: 'get',
      maxBodyLength: Infinity,
        url: 'https://api.prosperna.com/v1/orders/store?sid=63dc812b809e8c308d735e72'
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
          "sid": "63dc812b809e8c308d735e72",
          "data": [
              {
                  "order_information": {
                      "fname": "JOHN ERIC",
                      "lname": "SIGUENZA",
                      "email_address": "jsiguenza+63dc812b809e8c308d735e72@prosperna.com",
                      "phone": "639461503583",
                      "address_line": "Z3",
                      "state": "BOHOL",
                      "city": "BOHOL-ALICIA",
                      "barangay": "LA HACIENDA",
                      "zip_code": "4405",
                      "landmark": "",
                      "note": "",
                      "status": "Completed",
                      "quotation": {
                          "country_region": ""
                      }
                  },
                  "payment_information": {
                      "type": "EWALLET",
                      "gateway": "PH_GCASH",
                      "status": "Paid",
                      "reference_id": "ewc_e4778b73-7096-40c7-a9ea-3bcc06174d58"
                  },
                  "shipping_information": {
                      "type": "Standard Delivery",
                      "shipped_by": "J&T"
                  },
                  "delivery_information": {
                      "vehicle_type": "N/A",
                      "status": "Processing",
                      "reference_number": "980002480311",
                      "meta_data": {
                          "success": "true",
                          "reason": "",
                          "txlogisticid": "pros1-63dc8397072db349e8b63bc9",
                          "mailno": "980002480311",
                          "sortingcode": "380-631091",
                          "sortingNo": "126"
                      }
                  },
                  "fees": {
                      "convenience_fee": 10.069700000000001,
                      "convenience_fee_customer": 5.0348500000000005,
                      "shipping_fee": 9.97,
                      "payment_gateway_fee": 25.17425,
                      "additional_fee": 0
                  },
                  "dimensions": {
                      "actual_weight": 0,
                      "volumetric_weight": 0.0003
                  },
                  "order_id": "63dc8397072db349e8b63bc9",
                  "store_id": "63dc812b809e8c308d735e72",
                  "customer_id": "63dc83508c85c650353ae450",
                  "cart_ids": [
                      "63dc8368072db349e8b63bc5"
                  ],
                  "ordered_item_ids": [],
                  "is_trashed": false,
                  "order_total_amount": 1012.5,
                  "order_subtotal_amount": 997,
                  "order_total_qty": 1,
                  "has_been_disbursed_to_merchant": true,
                  "requested_for_disbursement": false,
                  "disbursement_status": "SUCCEEDED",
                  "disbursement_updated_by": [],
                  "createdAt": "2023-02-03T03:46:31.669Z",
                  "updatedAt": "2023-02-03T04:01:21.589Z",
                  "disbursement_reference_id": "P1-DISBURSE-3dac01bd-31c3-4d8c-bef9-363f95a1cd91",
                  "id": "63dc8397072db349e8b63bca",
                  "cart_items_list": [],
                  "ordered_items_list": [
                      {
                          "order_id": "63dc8397072db349e8b63bc9",
                          "store_id": "63dc812b809e8c308d735e72",
                          "product_slug": "product1",
                          "dev_ref_id": "63dc8399072db349e8b63bcc",
                          "customer_id": "63dc83508c85c650353ae450",
                          "is_guest": true,
                          "cart_quantity": 1,
                          "item_sub_total": 997,
                          "addon_ids": [],
                          "product_variant_combination_id": "",
                          "selected_variant_combination_data": null,
                          "product_data": {
                              "created_by": "63dc812b809e8c308d735e72",
                              "store_id": "63dc812b809e8c308d735e72",
                              "product_seo": {
                                  "primary": {
                                      "title": "",
                                      "description": "",
                                      "url": "https://maric100.prodev.prosperna.ph/product/product1"
                                  }
                              },
                              "product_specification": {
                                  "name": "Product1",
                                  "slug": "product1",
                                  "brand": "",
                                  "description": "",
                                  "images": [
                                      {
                                          "image": "https://p1-mediaserver.s3.ap-southeast-1.amazonaws.com/business/store/maric100/1675395507356-concrete-plaster-stone-brick-orange-3d-wall-mural_2.jpg",
                                          "original_name": "concrete-plaster-stone-brick-orange-3d-wall-mural_2.jpg",
                                          "type": "images/jpeg",
                                          "name_with_path": "business/store/maric100/1675395507356-concrete-plaster-stone-brick-orange-3d-wall-mural_2.jpg",
                                          "id": "63dc81b38ea1885610cb94f3"
                                      }
                                  ],
                                  "short_description": "",
                                  "source": "P1"
                              },
                              "product_state": {
                                  "is_product_has_variants": false,
                                  "is_hide_stock": false,
                                  "is_always_instock": false,
                                  "is_published": true,
                                  "is_imported": false,
                                  "is_trashed": false,
                                  "is_sold": false
                              },
                              "store_locations": [
                                  {
                                      "store_location_id": "63dc8178809e8c308d735ea0",
                                      "stock_quantity": 999
                                  }
                              ],
                              "product_measurements": {
                                  "product_size": {
                                      "height": 1,
                                      "length": 1,
                                      "width": 1,
                                      "unit": "cm"
                                  },
                                  "product_weight": {
                                      "weight": 0,
                                      "unit": "kg"
                                  }
                              },
                              "product_price": {
                                  "regular_price": 997,
                                  "sale_price": null,
                                  "price_display": "",
                                  "unit_cost": null,
                                  "margin": null
                              },
                              "product_addons": {
                                  "addOn_list": [],
                                  "addOn_limit": 0
                              },
                              "promo_codes": [],
                              "product_reviews": [],
                              "product_variants": [],
                              "createdAt": "2023-02-03T03:38:27.480Z",
                              "updatedAt": "2023-02-03T03:43:20.871Z",
                              "id": "63dc81b38ea1885610cb94f0",
                              "product_categories": [
                                  {
                                      "category_type": "main",
                                      "title": "main",
                                      "image": "https://p1-mediaserver.s3.ap-southeast-1.amazonaws.com/business/store/merchant/categories/concrete-plaster-stone-brick-orange-3d-wall-mural_2.jpg",
                                      "sub_categories": [],
                                      "createdAt": "2023-02-03T03:38:05.221Z",
                                      "updatedAt": "2023-02-03T03:38:05.221Z",
                                      "id": "63dc819d8ea1885610cb94ec"
                                  }
                              ],
                              "product_variant_combinations": [],
                              "product_variant_type_ids": []
                          },
                          "selected_addon_data": [],
                          "createdAt": "2023-02-03T03:45:44.370Z",
                          "updatedAt": "2023-02-03T03:45:44.370Z",
                          "id": "63dc8399072db349e8b63bcc"
                      }
                  ],
                  "order_coupons": []
              }
          ]
      }
    title: Response
    language: json
  - code_block: |2-
      
    title: Error
    language: json
---
