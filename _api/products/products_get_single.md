---
title: /v1/products/:product_id
position_number: 1.1
type: get
description: Get single product
parameters:
  - name: product_id
    content: product id
left_code_blocks:
  - code_block: |-
      var axios = require('axios');
      var data = '';

      var config = {
        method: 'get',
        url: 'api.prosperna.com/v1/products/:product_id'
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
        "data": {
          "product_specification": {
            "name": "product_name",
            "slug": "product_slug",
            "brand": "product_brand",
            "short_description": "short description",
            "long_description": "<p>long description</p>",
            "images": [
              {
                "image": "image_uri",
                "original_name": "original_name",
                "type": "images/png",
                "name_with_path": "name_with_path",
                "id": "image_id"
              }
            ]
          },
          "product_state": {
            "is_product_has_variants": false,
            "is_hide_stock": true,
            "is_always_instock": true,
            "is_published": true
          },
          "product_measurements": {
            "product_size": {
              "height": 100,
              "length": 62,
              "width": 1235,
              "unit": "cm"
            },
            "product_weight": {
              "weight": 45,
              "unit": "l"
            }
          },
          "product_price": {
            "regular_price": 900,
            "sale_price": 12,
            "price_display": "",
            "unit_cost": 56,
            "margin": 0,
            "stock_quantity": 0
          },
          "product_seo": {
            "primary": {
              "title": "seo_title",
              "description": "seo description",
              "url": "url"
            }
          },
          "product_addons": {
            "addOn_limit": 1,
            "addOn_list": [
              {
                "name": "addon_name",
                "price": 55.55,
                "description": "Addon description",
                "createdAt": "2023-02-09T13:38:21.140Z",
                "updatedAt": "2023-02-09T13:38:21.140Z",
                "store_id": "639749a5cb1db88617891bf0",
                "id": "63e4f74dbf61b3a5047d9dbe"
              }
            ]
          },
          "product_categories": [
            {
              "name": "category_name",
              "id": "63e4f6c4bf61b3a5047d9daf"
            }
          ],
          "product_variant_types": [
            {
              "id": "63e5810a763ae9c5f788b2e5",
              "product_id": "63e4f4fabf61b3a5047d9da4",
              "name": "Color",
              "with_color_variant": true,
              "variant_type_options": [
                {
                  "name": "White",
                  "color": "#fff",
                  "id": "63e5810a763ae9c5f788b2e6"
                },
                {
                  "name": "Black",
                  "color": "#000",
                  "id": "63e5810a763ae9c5f788b2e7"
                }
              ],
              "createdAt": "2023-02-09T23:26:02.164Z",
              "updatedAt": "2023-02-09T23:26:02.164Z"
            },
            {
              "id": "63e5820f763ae9c5f788b2eb",
              "product_id": "63e4f4fabf61b3a5047d9da4",
              "name": "Flavor",
              "with_color_variant": false,
              "variant_type_options": [
                {
                  "name": "variant_type_option_name",
                  "color": "",
                  "id": "variant_type_option_id"
                }
              ],
              "createdAt": "2023-02-10T13:40:04.358Z",
              "updatedAt": "2023-02-10T13:40:04.358Z"
            }
          ],
          "createdAt": "2023-02-09T13:28:26.326Z",
          "updatedAt": "2023-02-18T06:11:04.116Z",
          "product_type": "PHYSICAL",
          "id": "63e4f4fabf61b3a5047d9da4",
          "store_id": "639749a5cb1db88617891bf0",
          "product_variants_combinations": [
            {
              "name": "variant_combination_name",
              "price": 12.3,
              "stock_quantity": 10,
              "sale_price": 0,
              "margin": 0,
              "sku": "",
              "createdAt": "2023-02-03T01:31:06.493Z",
              "updatedAt": "2023-02-03T01:31:06.493Z",
              "id": "63dc63dae6ea5a06a9801d8b",
              "product_id": null,
              "variant_combination_image": {
                "image": "image_uri",
                "original_name": "original_name",
                "type": "images/png",
                "name_with_path": "name_with_path"
              },
              "variant_combinations": [
                {
                  "selected_variant_option_id": "selected_variant_option_id",
                  "variant_type_id": "variant_type_id"
                },
                {
                  "selected_variant_option_id": "selected_variant_option_id",
                  "variant_type_id": "variant_type_id"
                }
              ]
            }
          ]
        },
        "message": "",
        "statusCode": 200
      }

    title: Response
    language: json
  - code_block: |-
      {
        "error": true,
        "message": "Invalid score"
      }
    title: Error
    language: json
---
