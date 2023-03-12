---
title: /v1/products/:product_id
position_number: 1.3
type: put
description: Save/Update Product
parameters:
  - name: product_id
    content: Product id
content_markdown: |-
  The books will automatically be added to your reading list
  {: .success}

  Adds a book to your collection.
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
          price: 900,
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
        "id": 3,
        "title": "The Book Thief",
        "score": 4.3,
        "dateAdded": "5/1/2015"
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
