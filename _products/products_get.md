---
title: /v1/products/merchant-listing
position_number: 1.0
type: get
description: Get all Products
left_code_blocks:
  - code_block: |-
      var axios = require('axios');

      var config = {
        method: 'get',
        url: 'api.prosperna.com/v1/products/merchant-listing',
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
          "products": [
            {
              "product_specification": {
                "name": "product_name",
                "slug": "unique_product_slug",
                "brand": "product_brand",
                "short_description": "short_description",
                "long_description": "<p><strong>long_description</strong></p>",
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
              "product_seo": {
                "primary": {
                  "title": "seo_title",
                  "description": "seo description",
                  "url": "url"
                }
              },
              "product_measurements": {
                "product_size": {
                  "height": 44,
                  "length": 74,
                  "width": 45,
                  "unit": "cm"
                },
                "product_weight": {
                  "weight": 55,
                  "unit": "lb"
                }
              },
              "product_price": {
                "regular_price": 28,
                "sale_price": 0,
                "price_display": "",
                "unit_cost": 0,
                "margin": 0,
                "stock_quantity": 19
              },
              "product_categories": [
                {
                  "name": "category_name",
                  "id": "category_id"
                }
              ],
              "createdAt": "2023-02-12T14:29:12.173Z",
              "updatedAt": "2023-03-01T10:14:31.171Z",
              "product_type": "PHYSICAL",
              "id": "63e8f7b8c07f74725ccd2fb2",
              "store_id": "639749a5cb1db88617891bf0",
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
            }
          ],
          "pagination": {
            "totalDocs": 1,
            "limit": 999999,
            "page": 1,
            "totalPages": 1,
            "pagingCounter": 1,
            "hasPrevPage": false,
            "hasNextPage": false,
            "prevPage": null,
            "nextPage": null
          }
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
