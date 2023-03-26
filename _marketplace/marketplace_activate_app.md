---
title: /business-profile/marketplace/my-apps/:app_key/activate
position_number: 1.1
type: get
description: Activate/Install an app to your store

content_markdown: |-
  | ***Request Body***         | ***Data Type*** | ***Required*** | ***Description*** |
  |--------------------|-----------|----------|------------------------------------|
  | app_key               | string    | Yes      | The app key of marketplace app you want to activate/install. |

left_code_blocks:
  - code_block: |-
      var axios = require('axios');

      var config = {
        method: 'post',
        url: 'api.prosperna.com/v1/business-profile/marketplace/my-apps/jnt/activate',
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
          "message": "Successfully retrieve all installed marketplace apps.",
          "data": {
              "my_apps": {
                "activated_apps": {
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
                }
              }
          }
      }
    title: Response
    language: json
---
