---
title: /business-profile/banks
position_number: 1.7
type: get
description: Get all supported banks
left_code_blocks:
  - code_block: |-
      var axios = require('axios');

      var config = {
      method: 'get',
      url: 'api.prosperna.com/v1/business-profile/banks',

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
          "message": "Successfully retrieve banks.",
          "data": {
              "banks": [
                  {
                      "_id": "605433499138600528eb767b",
                      "bankName": "UNIONBANK",
                      "xenditBankChannelCode": "PH_UBP",
                      "country": "PH"
                  },
                  {
                      "_id": "605433319138600528eb7679",
                      "bankName": "BDO",
                      "xenditBankChannelCode": "PH_BDO",
                      "country": "PH"
                  },
                  {
                      "_id": "605433439138600528eb767a",
                      "bankName": "BPI",
                      "xenditBankChannelCode": "PH_BPI",
                      "country": "PH"
                  },
                  {
                      "_id": "61483124264faf4dae5f5147",
                      "bankName": "GCASH",
                      "xenditBankChannelCode": "PH_GCASH",
                      "country": "PH"
                  }
              ]
          }
      }
    title: Response
    language: json
---
