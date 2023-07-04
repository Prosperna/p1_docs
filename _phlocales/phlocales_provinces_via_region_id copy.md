---
title: /business-profile/ph-locale/provinces/:regionId
position_number: 1.3
type: get
description: Get all Philippine provinces via region id
content_markdown: |-
  | ***Parameters***         | ***Data Type*** | ***Required*** | ***Description***                        |
  |--------------------|-----------|----------|------------------------------------|
  | regionId               | string    | Yes      | Region id            |

left_code_blocks:
  - code_block: |-
      var axios = require('axios');

      var config = {
      method: 'get',
      url: 'api.prosperna.com/v1/business-profile/ph-locale/provinces/60530f205d8baa22bcb55921'
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
          "message": "Successfully retrieve PH regions.",
          "data": {
              "regions": [
                  {
                      "_id": "60530f205d8baa22bcb55921",
                      "regionName": "BARMM",
                      "regionShortName": "BARMM",
                      "dateCreated": "2021-03-18T08:28:16.223Z",
                      "lastUpdated": "2021-03-18T08:28:16.223Z"
                  },
                  {
                      "_id": "60530f205d8baa22bcb55922",
                      "regionName": "CAR",
                      "regionShortName": "CAR",
                      "dateCreated": "2021-03-18T08:28:16.224Z",
                      "lastUpdated": "2021-03-18T08:28:16.224Z"
                  },
                  {
                      "_id": "60530f205d8baa22bcb55923",
                      "regionName": "NCR",
                      "regionShortName": "NCR",
                      "dateCreated": "2021-03-18T08:28:16.224Z",
                      "lastUpdated": "2021-03-18T08:28:16.224Z"
                  },
                  {
                      "_id": "60530f205d8baa22bcb55917",
                      "regionName": "REGION I",
                      "regionShortName": "01",
                      "dateCreated": "2021-03-18T08:28:16.223Z",
                      "lastUpdated": "2021-03-18T08:28:16.223Z"
                  },
                  {
                      "_id": "60530f205d8baa22bcb55918",
                      "regionName": "REGION II",
                      "regionShortName": "02",
                      "dateCreated": "2021-03-18T08:28:16.223Z",
                      "lastUpdated": "2021-03-18T08:28:16.223Z"
                  },
                  {
                      "_id": "60530f205d8baa22bcb55919",
                      "regionName": "REGION III",
                      "regionShortName": "03",
                      "dateCreated": "2021-03-18T08:28:16.223Z",
                      "lastUpdated": "2021-03-18T08:28:16.223Z"
                  },
                  {
                      "_id": "60530f205d8baa22bcb5591a",
                      "regionName": "REGION IV-A",
                      "regionShortName": "4A",
                      "dateCreated": "2021-03-18T08:28:16.223Z",
                      "lastUpdated": "2021-03-18T08:28:16.223Z"
                  },
                  {
                      "_id": "60530f205d8baa22bcb5591b",
                      "regionName": "REGION IV-B",
                      "regionShortName": "4B",
                      "dateCreated": "2021-03-18T08:28:16.223Z",
                      "lastUpdated": "2021-03-18T08:28:16.223Z"
                  },
                  {
                      "_id": "60530f205d8baa22bcb55920",
                      "regionName": "REGION IX",
                      "regionShortName": "09",
                      "dateCreated": "2021-03-18T08:28:16.223Z",
                      "lastUpdated": "2021-03-18T08:28:16.223Z"
                  },
                  {
                      "_id": "60530f205d8baa22bcb5591c",
                      "regionName": "REGION V",
                      "regionShortName": "05",
                      "dateCreated": "2021-03-18T08:28:16.223Z",
                      "lastUpdated": "2021-03-18T08:28:16.223Z"
                  },
                  {
                      "_id": "60530f205d8baa22bcb5591d",
                      "regionName": "REGION VI",
                      "regionShortName": "06",
                      "dateCreated": "2021-03-18T08:28:16.223Z",
                      "lastUpdated": "2021-03-18T08:28:16.223Z"
                  },
                  {
                      "_id": "60530f205d8baa22bcb5591e",
                      "regionName": "REGION VII",
                      "regionShortName": "07",
                      "dateCreated": "2021-03-18T08:28:16.223Z",
                      "lastUpdated": "2021-03-18T08:28:16.223Z"
                  },
                  {
                      "_id": "60530f205d8baa22bcb5591f",
                      "regionName": "REGION VIII",
                      "regionShortName": "08",
                      "dateCreated": "2021-03-18T08:28:16.223Z",
                      "lastUpdated": "2021-03-18T08:28:16.223Z"
                  },
                  {
                      "_id": "60530f205d8baa22bcb55913",
                      "regionName": "REGION X",
                      "regionShortName": "10",
                      "dateCreated": "2021-03-18T08:28:16.222Z",
                      "lastUpdated": "2021-03-18T08:28:16.222Z"
                  },
                  {
                      "_id": "60530f205d8baa22bcb55914",
                      "regionName": "REGION XI",
                      "regionShortName": "11",
                      "dateCreated": "2021-03-18T08:28:16.222Z",
                      "lastUpdated": "2021-03-18T08:28:16.222Z"
                  },
                  {
                      "_id": "60530f205d8baa22bcb55915",
                      "regionName": "REGION XII",
                      "regionShortName": "12",
                      "dateCreated": "2021-03-18T08:28:16.223Z",
                      "lastUpdated": "2021-03-18T08:28:16.223Z"
                  },
                  {
                      "_id": "60530f205d8baa22bcb55916",
                      "regionName": "REGION XIII",
                      "regionShortName": "13",
                      "dateCreated": "2021-03-18T08:28:16.223Z",
                      "lastUpdated": "2021-03-18T08:28:16.223Z"
                  }
              ]
          }
      }
    title: Response
    language: json
---
