---
title: /products/categories
position_number: 2.0
type: post
description: Create Categories
parameters:
  - name: title
    content: The title for the book
  - name: score
    content: The book's score between 0 and 5
content_markdown: |-
  The books will automatically be added to your reading list
  {: .success}

  Adds a book to your collection.
left_code_blocks:
  - code_block: |-
      $.post("http://api.myapp.com/products/", {
        "token": "YOUR_APP_KEY",
        "title": "The Book Thief",
        "score": 4.3
      }, function(data) {
        alert(data);
      });
    title: jQuery
    language: javascript
  - code_block: |-
      var request = require('request');
      var options = {
        'method': 'POST',
        'url': 'http://api.myapp.com/products',
        'headers': {
          'Content-Type': 'application/json'
        },
        body: JSON.stringify({
          "token": "YOUR_APP_KEY",
          "title": "The Book Thief",
          "score": 4.3
        })
      };
      request(options, function (error, response) {
        if (error) throw new Error(error);
        console.log(response.body);
      });
    title: NodeJS
    language: javascript
  - code_block: |-
      $client = new Client();
      $headers = [
        'Content-Type' => 'application/json'
      ];
      $body = '{
        "token": "YOUR_APP_KEY",
        "title": "The Book Thief",
        "score": 4.3
      }';
      $request = new Request('POST', 'http://api.myapp.com/products', $headers, $body);
      $res = $client->sendAsync($request)->wait();
      echo $res->getBody();
    title: PHP - Guzzle
    language: php
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
