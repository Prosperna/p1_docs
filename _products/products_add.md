---
title: /:product_id
position_number: 1.3
type: put
description: Save/Update Product

content_markdown: |-
  | ***Parameters***         | ***Data Type*** | ***Required*** | ***Description***                        |
  |--------------------|-----------|----------|------------------------------------|
  | product_id               | string    | Yes      | Product id            |

  | ***Request Body***         | ***Data Type*** | ***Required*** | ***Description***                        |
  |--------------------|-----------|----------|------------------------------------|
  | product_specification.name               | string    | Yes      | Product name            |
  | product_specification.slug               | string    | Yes      | Product slug (without url)            |
  | product_specification.short_description               | string    | Yes      | Product short description            |
  | product_specification.long_description               | string    | Yes      | Product long description            |
  | product_specification.brand               | string    | No      | Product brand            |
  | product_specification.images               | array   | Yes      | Product images/thumbnails.            |
  | product_state.is_always_instock               | boolean   | Yes      | **PAID FEATURE** Boolean value for is always instock feature.          |
  | product_state.is_hide_stock               | boolean   | Yes      | **PAID FEATURE** Boolean value for is always hiding stock.          |
  | product_state.is_product_has_variants               | boolean   | Yes      | Boolean value to set if product has variants.          |
  | product_categories               | array   | Yes      | Array of categories id for a given product.          |
  | product_variant_types               | array   | Yes, _if is_product_has_variants is set to **true** else_ No.      | Array of product variant types.          |
  | product_variants_combinations               | array   | Yes, _if is_product_has_variants is set to **true** else_ No.     | Array of variant combinations.          |
  | product_addons               | object   | No     | **PAID FEATURE** Product addons, object containing the addon limit and array of addons ids.          |
  | product_price.regular_price               | number   | Yes, _if is_product_has_variants is set to **false** else_ No.     |  Product regular price.         |
  | product_price.sale_price               | number   | No     |  Product regular price.         |
  | product_price.stock_quantity               | number   | Yes, _if is_product_has_variants is set to **false** else_ No.     |  Product stock quantity.         |
  | product_price.margin               | number   | No     |  Product sale price.         |
  | product_price.unit_cost               | number   | No     |  Product sale price.         |
  | product_measurements.product_size.height               | number   | Yes, _if is_product_has_variants is set to **false** else_ No.     |  Product height.         |
  | product_measurements.product_size.width               | number   | Yes, _if is_product_has_variants is set to **false** else_ No.     |  Product width.         |
  | product_measurements.product_size.length               | number   | Yes, _if is_product_has_variants is set to **false** else_ No.     |  Product length.         |
  | product_measurements.product_size.unit               | string   | Yes, _if is_product_has_variants is set to **false** else_ No.     |  Product size unit. ```['mm', 'cm', 'in', 'm']```        |
  | product_measurements.product_weight.weight               | number   | Yes, _if is_product_has_variants is set to **false** else_ No.     |  Product weight.         |
  | product_measurements.product_weight.unit               | string   | Yes, _if is_product_has_variants is set to **false** else_ No.     |  Product weight unit. ```['g', 'kg', 'lb', 'ml', 'l', 'Oz']```         |
  | product_seo.primary.title               | string   | No     | **PAID FEATURE** SEO title.          |
  | product_seo.primary.description               | string   | No     | **PAID FEATURE** SEO description.          |
  | product_seo.primary.url               | string   | No     | **PAID FEATURE** SEO url.          |

left_code_blocks:
  - code_block: |-
      var axios = require('axios');
      var data = JSON.stringify({
        product_specification: {
          name: 'product_name',
          slug: 'product_slug',
          long_description: 'long description',
          short_description: 'short description',
          brand: 'product_brand',
          images: [
            {
              image: 'base64 image',
              file_name: 'image file name',
              image_action: 'new', // "delete" | "new" | "ordering_update"
            },
          ],
        },
        product_state: {
          is_always_instock: true,
          is_hide_stock: true,
          is_product_has_variants: false,
        },
        product_price: {
          regular_price: 900,
          margin: 56,
          sale_price: 12,
          unit_cost: 56,
          stock_quantity: 56,
        },
        product_measurements: {
          product_size: {
            height: 100,
            width: 1235,
            length: 62,
            unit: 'cm',
          },
          product_weight: {
            weight: 45,
            unit: 'l',
          },
        },
        product_variants_combinations: ['63e58292ad7a318363625be4'],
        product_variant_types: [
          '63e5810a763ae9c5f788b2e5',
          '63e5820f763ae9c5f788b2eb',
        ],
        product_addons: {
          addOn_limit: 1,
          addOn_list: ['63e4f74dbf61b3a5047d9dbe'],
        },
        product_categories: ['63e4f6c4bf61b3a5047d9daf'],
        product_seo: {
          primary: {
            title: 'seo_title',
            description: 'seo description',
            url: 'http://localhost:3000',
          },
        },
      });

      var config = {
        method: 'put',
        url: 'api.prosperna.com/v1/products/640c8c4de596bf3e3684bb57',
        headers: {
          'Content-Type': 'application/json',
        },
        data: data,
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
          "data": null,
          "message": "Successfully updated product.",
          "statusCode": 200
      }
    title: Response
    language: json
---
