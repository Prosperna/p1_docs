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


  Adds a products to your inventory.
left_code_blocks:
  - code_block: |-
      $.post("http://api.myapp.com/products/", {
        "token": "YOUR_APP_KEY",
        "title": "The Product Thief",
        "score": 4.3
      }, function(data) {
        alert(data);
      });
    title: jQuery
    language: javascript
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
