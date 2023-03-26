---
title: /business-profile/ph-locale/municipalities/:provinceId
position_number: 1.4
type: get
description: Get all Philippine municipalities via province id
content_markdown: |-
  | ***Parameters***         | ***Data Type*** | ***Required*** | ***Description***                        |
  |--------------------|-----------|----------|------------------------------------|
  | provinceId               | string    | Yes      | Province id            |

left_code_blocks:
  - code_block: |-
      var axios = require('axios');

      var config = {
      method: 'get',
      url: 'api.prosperna.com/v1/business-profile/ph-locale/municipalities/60530f205d8baa22bcb5596f',
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
          "message": "Successfully retrieve PH municipalities by province ID.",
          "data": {
              "municipalities": [
                  {
                      "_id": "60530f215d8baa22bcb55f7e",
                      "municipalityName": "Bangued",
                      "municipalityNameUppercased": "BANGUED",
                      "province": "60530f205d8baa22bcb5596f",
                      "region": "60530f205d8baa22bcb55922",
                      "dateCreated": "2021-03-18T08:28:17.145Z",
                      "lastUpdated": "2021-03-18T08:28:17.145Z"
                  },
                  {
                      "_id": "60530f215d8baa22bcb55f7f",
                      "municipalityName": "Boliney",
                      "municipalityNameUppercased": "BOLINEY",
                      "province": "60530f205d8baa22bcb5596f",
                      "region": "60530f205d8baa22bcb55922",
                      "dateCreated": "2021-03-18T08:28:17.145Z",
                      "lastUpdated": "2021-03-18T08:28:17.145Z"
                  },
                  {
                      "_id": "60530f215d8baa22bcb55f80",
                      "municipalityName": "Bucay",
                      "municipalityNameUppercased": "BUCAY",
                      "province": "60530f205d8baa22bcb5596f",
                      "region": "60530f205d8baa22bcb55922",
                      "dateCreated": "2021-03-18T08:28:17.145Z",
                      "lastUpdated": "2021-03-18T08:28:17.145Z"
                  },
                  {
                      "_id": "60530f215d8baa22bcb55f81",
                      "municipalityName": "Bucloc",
                      "municipalityNameUppercased": "BUCLOC",
                      "province": "60530f205d8baa22bcb5596f",
                      "region": "60530f205d8baa22bcb55922",
                      "dateCreated": "2021-03-18T08:28:17.145Z",
                      "lastUpdated": "2021-03-18T08:28:17.145Z"
                  },
                  {
                      "_id": "60530f215d8baa22bcb55f82",
                      "municipalityName": "Daguioman",
                      "municipalityNameUppercased": "DAGUIOMAN",
                      "province": "60530f205d8baa22bcb5596f",
                      "region": "60530f205d8baa22bcb55922",
                      "dateCreated": "2021-03-18T08:28:17.145Z",
                      "lastUpdated": "2021-03-18T08:28:17.145Z"
                  },
                  {
                      "_id": "60530f215d8baa22bcb55f83",
                      "municipalityName": "Danglas",
                      "municipalityNameUppercased": "DANGLAS",
                      "province": "60530f205d8baa22bcb5596f",
                      "region": "60530f205d8baa22bcb55922",
                      "dateCreated": "2021-03-18T08:28:17.145Z",
                      "lastUpdated": "2021-03-18T08:28:17.145Z"
                  },
                  {
                      "_id": "60530f215d8baa22bcb55f84",
                      "municipalityName": "Dolores",
                      "municipalityNameUppercased": "DOLORES",
                      "province": "60530f205d8baa22bcb5596f",
                      "region": "60530f205d8baa22bcb55922",
                      "dateCreated": "2021-03-18T08:28:17.145Z",
                      "lastUpdated": "2021-03-18T08:28:17.145Z"
                  },
                  {
                      "_id": "60530f215d8baa22bcb55f85",
                      "municipalityName": "La Paz",
                      "municipalityNameUppercased": "LA PAZ",
                      "province": "60530f205d8baa22bcb5596f",
                      "region": "60530f205d8baa22bcb55922",
                      "dateCreated": "2021-03-18T08:28:17.145Z",
                      "lastUpdated": "2021-03-18T08:28:17.145Z"
                  },
                  {
                      "_id": "60530f215d8baa22bcb55f86",
                      "municipalityName": "Lacub",
                      "municipalityNameUppercased": "LACUB",
                      "province": "60530f205d8baa22bcb5596f",
                      "region": "60530f205d8baa22bcb55922",
                      "dateCreated": "2021-03-18T08:28:17.145Z",
                      "lastUpdated": "2021-03-18T08:28:17.145Z"
                  },
                  {
                      "_id": "60530f215d8baa22bcb55f87",
                      "municipalityName": "Lagangilang",
                      "municipalityNameUppercased": "LAGANGILANG",
                      "province": "60530f205d8baa22bcb5596f",
                      "region": "60530f205d8baa22bcb55922",
                      "dateCreated": "2021-03-18T08:28:17.145Z",
                      "lastUpdated": "2021-03-18T08:28:17.145Z"
                  },
                  {
                      "_id": "60530f215d8baa22bcb55f88",
                      "municipalityName": "Lagayan",
                      "municipalityNameUppercased": "LAGAYAN",
                      "province": "60530f205d8baa22bcb5596f",
                      "region": "60530f205d8baa22bcb55922",
                      "dateCreated": "2021-03-18T08:28:17.145Z",
                      "lastUpdated": "2021-03-18T08:28:17.145Z"
                  },
                  {
                      "_id": "60530f215d8baa22bcb55f89",
                      "municipalityName": "Langiden",
                      "municipalityNameUppercased": "LANGIDEN",
                      "province": "60530f205d8baa22bcb5596f",
                      "region": "60530f205d8baa22bcb55922",
                      "dateCreated": "2021-03-18T08:28:17.145Z",
                      "lastUpdated": "2021-03-18T08:28:17.145Z"
                  },
                  {
                      "_id": "60530f215d8baa22bcb55f8a",
                      "municipalityName": "Licuan-Baay (Licuan)",
                      "municipalityNameUppercased": "LICUAN-BAAY (LICUAN)",
                      "province": "60530f205d8baa22bcb5596f",
                      "region": "60530f205d8baa22bcb55922",
                      "dateCreated": "2021-03-18T08:28:17.146Z",
                      "lastUpdated": "2021-03-18T08:28:17.146Z"
                  },
                  {
                      "_id": "60530f215d8baa22bcb55f8b",
                      "municipalityName": "Luba",
                      "municipalityNameUppercased": "LUBA",
                      "province": "60530f205d8baa22bcb5596f",
                      "region": "60530f205d8baa22bcb55922",
                      "dateCreated": "2021-03-18T08:28:17.146Z",
                      "lastUpdated": "2021-03-18T08:28:17.146Z"
                  },
                  {
                      "_id": "60530f215d8baa22bcb55f8c",
                      "municipalityName": "Malibcong",
                      "municipalityNameUppercased": "MALIBCONG",
                      "province": "60530f205d8baa22bcb5596f",
                      "region": "60530f205d8baa22bcb55922",
                      "dateCreated": "2021-03-18T08:28:17.146Z",
                      "lastUpdated": "2021-03-18T08:28:17.146Z"
                  },
                  {
                      "_id": "60530f215d8baa22bcb55f8d",
                      "municipalityName": "Manabo",
                      "municipalityNameUppercased": "MANABO",
                      "province": "60530f205d8baa22bcb5596f",
                      "region": "60530f205d8baa22bcb55922",
                      "dateCreated": "2021-03-18T08:28:17.146Z",
                      "lastUpdated": "2021-03-18T08:28:17.146Z"
                  },
                  {
                      "_id": "60530f215d8baa22bcb55f8e",
                      "municipalityName": "PeÑArrubia",
                      "municipalityNameUppercased": "PEÑARRUBIA",
                      "province": "60530f205d8baa22bcb5596f",
                      "region": "60530f205d8baa22bcb55922",
                      "dateCreated": "2021-03-18T08:28:17.146Z",
                      "lastUpdated": "2021-03-18T08:28:17.146Z"
                  },
                  {
                      "_id": "60530f215d8baa22bcb55f8f",
                      "municipalityName": "Pidigan",
                      "municipalityNameUppercased": "PIDIGAN",
                      "province": "60530f205d8baa22bcb5596f",
                      "region": "60530f205d8baa22bcb55922",
                      "dateCreated": "2021-03-18T08:28:17.146Z",
                      "lastUpdated": "2021-03-18T08:28:17.146Z"
                  },
                  {
                      "_id": "60530f215d8baa22bcb55f90",
                      "municipalityName": "Pilar",
                      "municipalityNameUppercased": "PILAR",
                      "province": "60530f205d8baa22bcb5596f",
                      "region": "60530f205d8baa22bcb55922",
                      "dateCreated": "2021-03-18T08:28:17.146Z",
                      "lastUpdated": "2021-03-18T08:28:17.146Z"
                  },
                  {
                      "_id": "60530f215d8baa22bcb55f91",
                      "municipalityName": "Sallapadan",
                      "municipalityNameUppercased": "SALLAPADAN",
                      "province": "60530f205d8baa22bcb5596f",
                      "region": "60530f205d8baa22bcb55922",
                      "dateCreated": "2021-03-18T08:28:17.146Z",
                      "lastUpdated": "2021-03-18T08:28:17.146Z"
                  },
                  {
                      "_id": "60530f215d8baa22bcb55f92",
                      "municipalityName": "San Isidro",
                      "municipalityNameUppercased": "SAN ISIDRO",
                      "province": "60530f205d8baa22bcb5596f",
                      "region": "60530f205d8baa22bcb55922",
                      "dateCreated": "2021-03-18T08:28:17.146Z",
                      "lastUpdated": "2021-03-18T08:28:17.146Z"
                  },
                  {
                      "_id": "60530f215d8baa22bcb55f93",
                      "municipalityName": "San Juan",
                      "municipalityNameUppercased": "SAN JUAN",
                      "province": "60530f205d8baa22bcb5596f",
                      "region": "60530f205d8baa22bcb55922",
                      "dateCreated": "2021-03-18T08:28:17.146Z",
                      "lastUpdated": "2021-03-18T08:28:17.146Z"
                  },
                  {
                      "_id": "60530f215d8baa22bcb55f94",
                      "municipalityName": "San Quintin",
                      "municipalityNameUppercased": "SAN QUINTIN",
                      "province": "60530f205d8baa22bcb5596f",
                      "region": "60530f205d8baa22bcb55922",
                      "dateCreated": "2021-03-18T08:28:17.146Z",
                      "lastUpdated": "2021-03-18T08:28:17.146Z"
                  },
                  {
                      "_id": "60530f215d8baa22bcb55f95",
                      "municipalityName": "Tayum",
                      "municipalityNameUppercased": "TAYUM",
                      "province": "60530f205d8baa22bcb5596f",
                      "region": "60530f205d8baa22bcb55922",
                      "dateCreated": "2021-03-18T08:28:17.146Z",
                      "lastUpdated": "2021-03-18T08:28:17.146Z"
                  },
                  {
                      "_id": "60530f215d8baa22bcb55f96",
                      "municipalityName": "Tineg",
                      "municipalityNameUppercased": "TINEG",
                      "province": "60530f205d8baa22bcb5596f",
                      "region": "60530f205d8baa22bcb55922",
                      "dateCreated": "2021-03-18T08:28:17.146Z",
                      "lastUpdated": "2021-03-18T08:28:17.146Z"
                  },
                  {
                      "_id": "60530f215d8baa22bcb55f97",
                      "municipalityName": "Tubo",
                      "municipalityNameUppercased": "TUBO",
                      "province": "60530f205d8baa22bcb5596f",
                      "region": "60530f205d8baa22bcb55922",
                      "dateCreated": "2021-03-18T08:28:17.146Z",
                      "lastUpdated": "2021-03-18T08:28:17.146Z"
                  },
                  {
                      "_id": "60530f215d8baa22bcb55f98",
                      "municipalityName": "Villaviciosa",
                      "municipalityNameUppercased": "VILLAVICIOSA",
                      "province": "60530f205d8baa22bcb5596f",
                      "region": "60530f205d8baa22bcb55922",
                      "dateCreated": "2021-03-18T08:28:17.146Z",
                      "lastUpdated": "2021-03-18T08:28:17.146Z"
                  }
              ]
          }
      }
    title: Response
    language: json
---
