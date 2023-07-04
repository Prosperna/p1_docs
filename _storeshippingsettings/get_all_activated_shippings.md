---
title: /business-profile/shipping/settings/:store_id
position_number: 1.0
type: get
description: Get all activated shippings for a given store

left_code_blocks:
  - code_block: |-
      var axios = require('axios');

      var config = {
        method: 'get',
        url: 'api.prosperna.com/v1/business-profile/store/details',
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
          "message": "",
          "data": {
              "shippingDetails": [
                  {
                      "pickup_address": "63908c8b5e8aa33cd37b9e77",
                      "shipping_option": "PICKUP",
                      "shipping_option_type": "PICKUP",
                      "selected": true,
                      "payment_options": {
                          "BANK_TRANSFER": true,
                          "COD": true,
                          "COP": false,
                          "E_WALLET": false,
                          "CREDIT_CARD": false,
                          "OVER_THE_COUNTER": false
                      },
                      "createdAt": "2022-12-08T02:28:16.886Z",
                      "updatedAt": "2022-12-08T03:01:31.355Z",
                      "id": "63914bc0ae4193caaf9c179d",
                      "pickup_details": {
                          "_id": "63908c8b5e8aa33cd37b9e77",
                          "store_id": "63861440e2c90910a117e826",
                          "contact_person": "contact_person",
                          "contact_number": "contact_number",
                          "business_address": "business_address",
                          "save_address_name": "save address",
                          "province": {
                              "name": "province_name",
                              "id": "province_id"
                          },
                          "barangay": {
                              "name": "barangay_name",
                              "id": "barangay_id"
                          },
                          "city": {
                              "name": "city_name",
                              "id": "city_id"
                          },
                          "createdAt": "2022-12-07T12:52:27.162Z",
                          "updatedAt": "2022-12-07T12:53:38.519Z",
                          "__v": 0
                      }
                  },
                  {
                      "pickup_address": "63908c8b5e8aa33cd37b9e77",
                      "shipping_option": "OWN_BOOKING",
                      "shipping_option_type": "OWN_BOOKING",
                      "selected": true,
                      "payment_options": {
                          "BANK_TRANSFER": true,
                          "COD": true,
                          "COP": false,
                          "E_WALLET": false,
                          "CREDIT_CARD": false,
                          "OVER_THE_COUNTER": false
                      },
                      "createdAt": "2022-12-08T03:03:58.344Z",
                      "updatedAt": "2022-12-09T14:33:35.490Z",
                      "id": "6391541e1db2f7242fd1e4ba",
                      "pickup_details": {
                          "_id": "63908c8b5e8aa33cd37b9e77",
                          "store_id": "63861440e2c90910a117e826",
                          "contact_person": "contact_person",
                          "contact_number": "contact_number",
                          "business_address": "business_address",
                          "save_address_name": "save address",
                          "province": {
                              "name": "province_name",
                              "id": "province_id"
                          },
                          "barangay": {
                              "name": "barangay_name",
                              "id": "barangay_id"
                          },
                          "city": {
                              "name": "city_name",
                              "id": "city_id"
                          },
                          "createdAt": "2022-12-07T12:52:27.162Z",
                          "updatedAt": "2022-12-07T12:53:38.519Z",
                          "__v": 0
                      }
                  },
                  {
                      "pickup_address": "6395af15cb1db8861788ad22",
                      "shipping_option": "J&T",
                      "shipping_option_type": "STANDARD",
                      "selected": true,
                      "payment_options": {
                          "BANK_TRANSFER": true,
                          "COD": true,
                          "COP": false,
                          "E_WALLET": true,
                          "CREDIT_CARD": true,
                          "OVER_THE_COUNTER": true
                      },
                      "createdAt": "2022-12-09T13:49:46.701Z",
                      "updatedAt": "2022-12-11T10:21:23.770Z",
                      "id": "63933cfa669bf24320a29815",
                      "pickup_details": {
                          "_id": "63908c8b5e8aa33cd37b9e77",
                          "store_id": "63861440e2c90910a117e826",
                          "contact_person": "contact_person",
                          "contact_number": "contact_number",
                          "business_address": "business_address",
                          "save_address_name": "save address",
                          "province": {
                              "name": "province_name",
                              "id": "province_id"
                          },
                          "barangay": {
                              "name": "barangay_name",
                              "id": "barangay_id"
                          },
                          "city": {
                              "name": "city_name",
                              "id": "city_id"
                          },
                          "createdAt": "2022-12-07T12:52:27.162Z",
                          "updatedAt": "2022-12-07T12:53:38.519Z",
                          "__v": 0
                      }
                  },
                  {
                      "pickup_address": "63908c8b5e8aa33cd37b9e77",
                      "shipping_option": "LALAMOVE",
                      "shipping_option_type": "SAMEDAY_SCHED",
                      "selected": true,
                      "payment_options": {
                          "BANK_TRANSFER": true,
                          "COD": true,
                          "COP": false,
                          "E_WALLET": false,
                          "CREDIT_CARD": false,
                          "OVER_THE_COUNTER": false
                      },
                      "createdAt": "2022-12-09T14:12:12.165Z",
                      "updatedAt": "2022-12-09T14:12:12.165Z",
                      "id": "6393423cb49cfd9aad9eeb14",
                      "pickup_details": {
                          "_id": "63908c8b5e8aa33cd37b9e77",
                          "store_id": "63861440e2c90910a117e826",
                          "contact_person": "contact_person",
                          "contact_number": "contact_number",
                          "business_address": "business_address",
                          "save_address_name": "save address",
                          "province": {
                              "name": "province_name",
                              "id": "province_id"
                          },
                          "barangay": {
                              "name": "barangay_name",
                              "id": "barangay_id"
                          },
                          "city": {
                              "name": "city_name",
                              "id": "city_id"
                          },
                          "createdAt": "2022-12-07T12:52:27.162Z",
                          "updatedAt": "2022-12-07T12:53:38.519Z",
                          "__v": 0
                      }
                  }
              ]
          }
      }
    title: Response
    language: json
---
