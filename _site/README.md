# Prosperna

API documentation for Prosperna. Browse through a [API documenation](https://docs.prosperna.com/).
Start documenting your API with this configurable theme.

Public Postman

[![Run in Postman](https://run.pstmn.io/button.svg)](https://god.gw.postman.com/run-collection/22726848-d4428d72-2968-4fef-8ccb-4ce88e7177c9?action=collection%2Ffork&collection-url=entityId%3D22726848-d4428d72-2968-4fef-8ccb-4ce88e7177c9%26entityType%3Dcollection%26workspaceId%3Df139785f-cdb6-4a6d-b3c1-77d3e522e4a2)

![screenshot](images/_screenshot.png)

## Setup

1. Add your site and author details in `_config.yml`.
2. Get a workflow going to see your site's output (with [CloudCannon](https://app.cloudcannon.com/) or Jekyll locally).

```bash
$ bundle install
```

Run `jekyll` commands through Bundler to ensure you're using the right versions:

```bash
$ bundle exec jekyll serve
```

### Usage

- Each section is a different collection, this helps organise your content.
- Set the order of the collections with the position_number field in collection configuration in `_config.yml`.
- Set the order of the documents inside a collection by setting the position_number in front matter.

### Steps to create collections

1. Create directory name '\_collection_name' eg: \_orders
2. Create file name of the endpoints eg: \_orders_list.md
3. Add the default yml code

```yml
---
title:
position_number:
parameters:
  - name:
    content:
content_markdown:
left_code_blocks:
  - code_block:
    title:
    language:
right_code_blocks:
  - code_block:
    title:
    language:
---
```

4. Specify the title: of the endpoint, which should briefly describe its purpose or functionality.
5. Set the position_number: to indicate the order in which the endpoint appears within the collection, with lower numbers indicating higher priority.
6. Define any parameters that are required or optional for the endpoint, including their name and a brief description of their purpose. For example:

```yml
arameters:
  - name: id
    content: The ID of the order to retrieve
    required: true
  - name: status
    content: The status of the orders to retrieve
    required: false
```

7. Add the content_markdown: section, which should provide a detailed explanation of the endpoint's functionality, including any relevant examples or use cases. This section should use Markdown formatting to make the text easy to read and understand.
8. If necessary, add any left_code_blocks or right_code_blocks sections to include additional code snippets or examples to illustrate the endpoint or collection's usage. For each code block, specify a title and the language in which the code is written. For example:

```yml
left_code_blocks:
  - code_block:
      title: Example Request
      language: bash
      content: |
        curl https://example.com/api/users/123
  - code_block:
      title: Example Response
      language: json
      content: |
        {
          "id": 123,
          "name": "John Doe",
          "email": "john.doe@example.com"
        }
```

9. Repeat the above steps for each endpoint in the collection, with each endpoint having its own separate file within the collection directory.

10. Create a new right_code_blocks field under the main YAML object.
11. Add one or more code_block objects under the right_code_blocks field to provide additional code snippets or examples to illustrate the endpoint's usage. For each code_block object, specify a title and the language in which the code is written, as well as the actual code content. For example:

```yml
right_code_blocks:
  - code_block:
      title: Example Response
      language: json
      content: |
        {
          "success": true,
          "message": "User created successfully",
          "user_id": 1234
        }
```

12. You can add multiple code_block objects under the right_code_blocks field to provide different examples or variations of the same code. For example, you might include a code block that demonstrates how to handle errors or exceptions that might occur during the execution of the endpoint.

```yml
right_code_blocks:
  - code_block:
      title: Example Response
      language: json
      content: |
        {
          "success": true,
          "message": "User created successfully",
          "user_id": 1234
        }
  - code_block:
      title: Error Response
      language: json
      content: |
        {
          "success": false,
          "message": "User creation failed",
          "error_code": 1001
        }
```

13. Once you have added the right_code_blocks field and any necessary code_block objects, save the updated YAML code to the appropriate file within your collection or endpoint directory.
