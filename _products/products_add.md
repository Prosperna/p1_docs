---
title: /products
position_number: 1.1
type: post
description: Create Product
content_markdown: |-
  | Parameters         | Data Type | Required | Description                        |
  |--------------------|-----------|----------|------------------------------------|
  | name               | string    | Yes      | Name of the Product                |
  | slug               | string    | Yes      | Path of the Product                |
  | description        | text      | No       | Product long description           |
  | short_description  | text      | No       | Product short description          |
  | brand              | string    | No       | Product brand                      |
  | product_measurements | array   | No       | available values: `['cm', 'mm', 'in', 'm' ]`                   |


  Adds a products to your inventory.
left_code_blocks:
  - code_block: |-
      const request = require('request');
      const username = 'your_username';
      const password = 'your_password';
      const auth = 'Basic ' + Buffer.from(username + ':' + password).toString('base64');

      const options = {
        method: 'POST',
        url: 'http://localhost:4000/v1/products',
        headers: {
          Authorization: auth,
          'Content-Type': 'application/json',
        },
        body: {
          product_specification: {
            name: 'another name here',
            slug: 'davide_unique_slugl3',
            description: 'product_description',
            short_description: 'short description',
            brand: 'product_brand',
            images: [
              {
                file_name: 'newccc.jpeg',
                image: 'data:image/jpeg;base64',
              },
            ],
          },
          product_state: {
            is_always_instock: true,
            is_hide_stock: true,
          },
          product_measurements: {
            product_size: {
              height: 45,
              width: 45,
              length: 62,
              unit: 'cm',
            },
            product_weight: {
              weight: 45,
              unit: 'l',
            },
          },
          product_variants_combinations: [
            {
              combination_name: 'Large Chocolate',
              stock_quantity: 10,
              price: 12.3,
              variant_combinations: [
                {
                  selected_variant_option_id: '6389ec5665561a16ca6c096a',
                  variant_type_id: '6389ec5665561a16ca6c0969',
                },
                {
                  selected_variant_option_id: '638997c9f3c4c4080d6d4c15',
                  variant_type_id: '638997c9f3c4c4080d6d4c14',
                },
              ],
            },
            {
              combination_name: 'Large Cheese',
              stock_quantity: 10,
              price: 10,
              variant_combinations: [
                {
                  selected_variant_option_id: '6389ec5665561a16ca6c096b',
                  variant_type_id: '6389ec5665561a16ca6c0969',
                },
                {
                  selected_variant_option_id: '638997c9f3c4c4080d6d4c15',
                  variant_type_id: '638997c9f3c4c4080d6d4c14',
                },
              ],
            },
          ],
          product_addons: {
            addOn_limit: 1,
            addOn_list: ['6386a7d04d734f58b587f131'],
          },
          product_price: {
            regular_price: 1522,
            sale_price: 0,
            price_display: 'Buy one take one',
            margin: 45,
            unit_cost: 1,
          },
          store_locations: [
            {
              stock_quantity: 3,
              store_location_id: '636bab233ea4455a9486ad5b',
            },
          ],
          product_categories: ['6386a2b04d734f58b587f0f8'],
          product_seo: {
            primary: {
              title: 'seo_title',
              description: 'seo description',
              url: 'http://localhost:3000',
            },
          },
        },
        json: true,
      };

      rp(options)
        .then((response) => {
          console.log(response);
        })
        .catch((err) => {
          console.error(err);
        });
    title: NodeJs
    language: javascript
  - code_block: |-
      import base64
      import json
      import requests

      username = 'your_username'
      password = 'your_password'
      url = 'https://your_api_endpoint.com/v1/products'

      # Encode the username and password in base64
      auth_string = f"{username}:{password}"
      encoded_auth_string = base64.b64encode(auth_string.encode()).decode()

      # Set the Authorization and Content-Type headers
      headers = {
          'Authorization': f'Basic {encoded_auth_string}',
          'Content-Type': 'application/json'
      }

      # Define the payload
      payload = {
          "product_specification": {
              "name": "another name here",
              "slug": "davide_unique_slugl3",
              "description": "product_description",
              "short_description": "short description",
              "brand": "product_brand",
              "images": [
                  {
                      "file_name": "newccc.jpeg",
                      "image": "data:image/jpeg;base64"
                  }
              ]
          },
          "product_state": {
              "is_always_instock": True,
              "is_hide_stock": True
          },
          "product_measurements": {
              "product_size": {
                  "height": 45,
                  "width": 45,
                  "length": 62,
                  "unit": "cm"
              },
              "product_weight": {
                  "weight": 45,
                  "unit": "l"
              }
          },
          "product_variants_combinations": [
              {
                  "combination_name": "Large Chocolate",
                  "stock_quantity": 10,
                  "price": 12.3,
                  "variant_combinations": [
                      {
                          "selected_variant_option_id": "6389ec5665561a16ca6c096a",
                          "variant_type_id": "6389ec5665561a16ca6c0969"
                      },
                      {
                          "selected_variant_option_id": "638997c9f3c4c4080d6d4c15",
                          "variant_type_id": "638997c9f3c4c4080d6d4c14"
                      }
                  ]
              },
              {
                  "combination_name": "Large Cheese",
                  "stock_quantity": 10,
                  "price": 10,
                  "variant_combinations": [
                      {
                          "selected_variant_option_id": "6389ec5665561a16ca6c096b",
                          "variant_type_id": "6389ec5665561a16ca6c0969"
                      },
                      {
                          "selected_variant_option_id": "638997c9f3c4c4080d6d4c15",
                          "variant_type_id": "638997c9f3c4c4080d6d4c14"
                      }
                  ]
              }
          ],
          "product_addons": {
              "addOn_limit": 1,
              "addOn_list": [
                  "6386a7d04d734f58b587f131"
              ]
          },
          "product_price": {
              "regular_price": 1522,
              "sale_price": 0,
              "price_display": "Buy one take one",
              "margin": 45,
              "unit_cost": 1
          },
          "store_locations": [
              {
                  "stock_quantity": 3,
                  "store_location_id": "636bab233ea4455a9486ad5b"
              }
          ],
          "product_categories": [
              "6386a2b04d734f58b587f0f8"
          ],
          "product_seo": {
              "primary": {
                  "title": "seo_title",
                  "description": "seo description",
                  "url": "http://localhost:3000"
              }
          }
      }

      # Convert the payload to a JSON string
      json_payload = json.dumps(payload)

      # Make a POST request with the headers and JSON payload
      response = requests.post(url, headers=headers, data=json_payload)

      # Print the response
      print(response.text)
    title: Python
    language: python
right_code_blocks:
  - code_block: |-
      {
        "id": 3,
        "title": "The Product Thief",
        "score": 4.3,
        "dateAdded": "5/1/2015"
      }
    title: Request
    language: json
  - code_block: |-
      {
        "error": true,
        "message": "Invalid score"
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
