---
title: /business-profile/marketplace/apps
position_number: 1.0
type: get
description: Get all marketplace apps on P1 platform

left_code_blocks:
  - code_block: |-
      var axios = require('axios');

      var config = {
        method: 'get',
        url: 'api.prosperna.com/v1/business-profile/marketplace/apps',
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
          "success": true,
          "message": "Successfully retrieve all marketplace apps.",
          "data": {
              "apps": [
                  {
                      "is_activated": true,
                      "app_key": "jnt",
                      "title": "app name",
                      "subtitle": "app subtitle",
                      "description": "app description",
                      "icon": "app_icon_url",
                      "contents": [
                          {
                              "title": "Overview",
                              "key": "overview",
                              "carousel": [
                                  "image_1.png",
                                  "image_2.png"
                              ],
                              "description": "description",
                              "createdAt": "2023-01-05T08:53:49.092Z",
                              "updatedAt": "2023-01-05T08:53:49.092Z",
                              "id": "63b6901d491f6be12b409215"
                          },
                      ],
                      "createdAt": "2023-01-05T08:53:49.092Z",
                      "updatedAt": "2023-01-05T08:53:49.092Z",
                      "id": "63b6901d491f6be12b409214"
                  }
              ]
          }
      }
    title: Response
    language: json
---
