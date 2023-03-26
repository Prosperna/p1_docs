---
title: /business-profile/industries
position_number: 1.6
type: get
description: Get industry list
left_code_blocks:
  - code_block: |-
      var axios = require('axios');

      var config = {
      method: 'get',
      url: 'api.prosperna.com/v1/business-profile/industries',

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
          "message": "Successfully retrieve industries.",
          "data": {
              "count": 30,
              "industries": [
                  {
                      "_id": "63b6eb7b7ed0a8312a834630",
                      "industryName": "Agency",
                      "industryLabel": "Agency"
                  },
                  {
                      "_id": "63b6eb7b7ed0a8312a834631",
                      "industryName": "Agriculture",
                      "industryLabel": "Agriculture"
                  },
                  {
                      "_id": "63b6eb7b7ed0a8312a834632",
                      "industryName": "Arts & Crafts",
                      "industryLabel": "Arts & Crafts"
                  },
                  {
                      "_id": "63b6eb7b7ed0a8312a834633",
                      "industryName": "Automotive",
                      "industryLabel": "Automotive"
                  },
                  {
                      "_id": "63b6eb7b7ed0a8312a834634",
                      "industryName": "Bakery",
                      "industryLabel": "Bakery"
                  },
                  {
                      "_id": "63b6eb7b7ed0a8312a834635",
                      "industryName": "Beer & Wine",
                      "industryLabel": "Beer & Wine"
                  },
                  {
                      "_id": "63b6eb7b7ed0a8312a834636",
                      "industryName": "Bike Shop",
                      "industryLabel": "Bike Shop"
                  },
                  {
                      "_id": "63b6eb7b7ed0a8312a834637",
                      "industryName": "Coffee Shop",
                      "industryLabel": "Coffee Shop"
                  },
                  {
                      "_id": "63b6eb7b7ed0a8312a834638",
                      "industryName": "Construction",
                      "industryLabel": "Construction"
                  },
                  {
                      "_id": "63b6eb7b7ed0a8312a834639",
                      "industryName": "Digital/Downloadable Products",
                      "industryLabel": "Digital/Downloadable Products"
                  },
                  {
                      "_id": "63b6eb7b7ed0a8312a83463a",
                      "industryName": "Education",
                      "industryLabel": "Education"
                  },
                  {
                      "_id": "63b6eb7b7ed0a8312a83463b",
                      "industryName": "Electronics",
                      "industryLabel": "Electronics"
                  },
                  {
                      "_id": "63b6eb7b7ed0a8312a83463c",
                      "industryName": "Fashion & Apparel",
                      "industryLabel": "Fashion & Apparel"
                  },
                  {
                      "_id": "63b6eb7b7ed0a8312a83463d",
                      "industryName": "Financial & Insurance Services",
                      "industryLabel": "Financial & Insurance Services"
                  },
                  {
                      "_id": "63b6eb7b7ed0a8312a83463e",
                      "industryName": "Footwear",
                      "industryLabel": "Footwear"
                  },
                  {
                      "_id": "63b6eb7b7ed0a8312a83463f",
                      "industryName": "Grocery",
                      "industryLabel": "Grocery"
                  },
                  {
                      "_id": "63b6eb7b7ed0a8312a834640",
                      "industryName": "Health & Beauty",
                      "industryLabel": "Health & Beauty"
                  },
                  {
                      "_id": "63b6eb7b7ed0a8312a834641",
                      "industryName": "Home Furnishings",
                      "industryLabel": "Home Furnishings"
                  },
                  {
                      "_id": "63b6eb7b7ed0a8312a834642",
                      "industryName": "Jewelry",
                      "industryLabel": "Jewelry"
                  },
                  {
                      "_id": "63b6eb7b7ed0a8312a834643",
                      "industryName": "Not for Profit",
                      "industryLabel": "Not for Profit"
                  },
                  {
                      "_id": "63b6eb7b7ed0a8312a834644",
                      "industryName": "Pet Care & Supply",
                      "industryLabel": "Pet Care & Supply"
                  },
                  {
                      "_id": "63b6eb7b7ed0a8312a834645",
                      "industryName": "Pharmacy",
                      "industryLabel": "Pharmacy"
                  },
                  {
                      "_id": "63b6eb7b7ed0a8312a834646",
                      "industryName": "Printing",
                      "industryLabel": "Printing"
                  },
                  {
                      "_id": "63b6eb7b7ed0a8312a834647",
                      "industryName": "Professional Services",
                      "industryLabel": "Professional Services"
                  },
                  {
                      "_id": "63b6eb7b7ed0a8312a834649",
                      "industryName": "Real Estate",
                      "industryLabel": "Real Estate"
                  },
                  {
                      "_id": "63b6eb7b7ed0a8312a834648",
                      "industryName": "Restaurant",
                      "industryLabel": "Restaurant"
                  },
                  {
                      "_id": "63b6eb7b7ed0a8312a83464a",
                      "industryName": "Sporting Goods",
                      "industryLabel": "Sporting Goods"
                  },
                  {
                      "_id": "63b6eb7b7ed0a8312a83464b",
                      "industryName": "Travel & Hospitality",
                      "industryLabel": "Travel & Hospitality"
                  },
                  {
                      "_id": "63b6eb7b7ed0a8312a83464c",
                      "industryName": "Venture Capital",
                      "industryLabel": "Venture Capital"
                  },
                  {
                      "_id": "63b6eb7b7ed0a8312a83464d",
                      "industryName": "Other",
                      "industryLabel": "Other"
                  }
              ]
          }
      }
    title: Response
    language: json
---
