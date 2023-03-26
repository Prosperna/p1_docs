---
title: /business-profile/ph-locale/provinces
position_number: 1.2
type: get
description: Get all Philippine provinces
left_code_blocks:
  - code_block: |-
      var axios = require('axios');

      var config = {
        method: 'get',
        url: 'api.prosperna.com/v1/business-profile/ph-locale/provinces',
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
          "message": "Successfully retrieve PH provinces.",
          "data": {
              "provinces": [
                  {
                      "_id": "60530f205d8baa22bcb5596f",
                      "provinceName": "Abra",
                      "provinceNameUppercased": "ABRA",
                      "region": "60530f205d8baa22bcb55922",
                      "dateCreated": "2021-03-18T08:28:16.403Z",
                      "lastUpdated": "2021-03-18T08:28:16.403Z"
                  },
                  {
                      "_id": "60530f205d8baa22bcb55932",
                      "provinceName": "Agusan Del Norte",
                      "provinceNameUppercased": "AGUSAN DEL NORTE",
                      "region": "60530f205d8baa22bcb55916",
                      "dateCreated": "2021-03-18T08:28:16.390Z",
                      "lastUpdated": "2021-03-18T08:28:16.390Z"
                  },
                  {
                      "_id": "60530f205d8baa22bcb55933",
                      "provinceName": "Agusan Del Sur",
                      "provinceNameUppercased": "AGUSAN DEL SUR",
                      "region": "60530f205d8baa22bcb55916",
                      "dateCreated": "2021-03-18T08:28:16.390Z",
                      "lastUpdated": "2021-03-18T08:28:16.390Z"
                  },
                  {
                      "_id": "60530f205d8baa22bcb55957",
                      "provinceName": "Aklan",
                      "provinceNameUppercased": "AKLAN",
                      "region": "60530f205d8baa22bcb5591d",
                      "dateCreated": "2021-03-18T08:28:16.394Z",
                      "lastUpdated": "2021-03-18T08:28:16.395Z"
                  },
                  {
                      "_id": "60530f205d8baa22bcb55951",
                      "provinceName": "Albay",
                      "provinceNameUppercased": "ALBAY",
                      "region": "60530f205d8baa22bcb5591c",
                      "dateCreated": "2021-03-18T08:28:16.393Z",
                      "lastUpdated": "2021-03-18T08:28:16.393Z"
                  },
                  {
                      "_id": "60530f205d8baa22bcb55958",
                      "provinceName": "Antique",
                      "provinceNameUppercased": "ANTIQUE",
                      "region": "60530f205d8baa22bcb5591d",
                      "dateCreated": "2021-03-18T08:28:16.395Z",
                      "lastUpdated": "2021-03-18T08:28:16.395Z"
                  },
                  {
                      "_id": "60530f205d8baa22bcb55970",
                      "provinceName": "Apayao",
                      "provinceNameUppercased": "APAYAO",
                      "region": "60530f205d8baa22bcb55922",
                      "dateCreated": "2021-03-18T08:28:16.403Z",
                      "lastUpdated": "2021-03-18T08:28:16.403Z"
                  },
                  {
                      "_id": "60530f205d8baa22bcb55940",
                      "provinceName": "Aurora",
                      "provinceNameUppercased": "AURORA",
                      "region": "60530f205d8baa22bcb55919",
                      "dateCreated": "2021-03-18T08:28:16.392Z",
                      "lastUpdated": "2021-03-18T08:28:16.392Z"
                  },
                  {
                      "_id": "60530f205d8baa22bcb5596a",
                      "provinceName": "Basilan",
                      "provinceNameUppercased": "BASILAN",
                      "region": "60530f205d8baa22bcb55921",
                      "dateCreated": "2021-03-18T08:28:16.403Z",
                      "lastUpdated": "2021-03-18T08:28:16.403Z"
                  },
                  {
                      "_id": "60530f205d8baa22bcb55941",
                      "provinceName": "Bataan",
                      "provinceNameUppercased": "BATAAN",
                      "region": "60530f205d8baa22bcb55919",
                      "dateCreated": "2021-03-18T08:28:16.392Z",
                      "lastUpdated": "2021-03-18T08:28:16.392Z"
                  },
                  {
                      "_id": "60530f205d8baa22bcb5593b",
                      "provinceName": "Batanes",
                      "provinceNameUppercased": "BATANES",
                      "region": "60530f205d8baa22bcb55918",
                      "dateCreated": "2021-03-18T08:28:16.391Z",
                      "lastUpdated": "2021-03-18T08:28:16.391Z"
                  },
                  {
                      "_id": "60530f205d8baa22bcb55947",
                      "provinceName": "Batangas",
                      "provinceNameUppercased": "BATANGAS",
                      "region": "60530f205d8baa22bcb5591a",
                      "dateCreated": "2021-03-18T08:28:16.392Z",
                      "lastUpdated": "2021-03-18T08:28:16.392Z"
                  },
                  {
                      "_id": "60530f205d8baa22bcb55971",
                      "provinceName": "Benguet",
                      "provinceNameUppercased": "BENGUET",
                      "region": "60530f205d8baa22bcb55922",
                      "dateCreated": "2021-03-18T08:28:16.403Z",
                      "lastUpdated": "2021-03-18T08:28:16.403Z"
                  },
                  {
                      "_id": "60530f205d8baa22bcb55961",
                      "provinceName": "Biliran",
                      "provinceNameUppercased": "BILIRAN",
                      "region": "60530f205d8baa22bcb5591f",
                      "dateCreated": "2021-03-18T08:28:16.402Z",
                      "lastUpdated": "2021-03-18T08:28:16.402Z"
                  },
                  {
                      "_id": "60530f205d8baa22bcb5595d",
                      "provinceName": "Bohol",
                      "provinceNameUppercased": "BOHOL",
                      "region": "60530f205d8baa22bcb5591e",
                      "dateCreated": "2021-03-18T08:28:16.400Z",
                      "lastUpdated": "2021-03-18T08:28:16.400Z"
                  },
                  {
                      "_id": "60530f205d8baa22bcb55924",
                      "provinceName": "Bukidnon",
                      "provinceNameUppercased": "BUKIDNON",
                      "region": "60530f205d8baa22bcb55913",
                      "dateCreated": "2021-03-18T08:28:16.388Z",
                      "lastUpdated": "2021-03-18T08:28:16.388Z"
                  },
                  {
                      "_id": "60530f205d8baa22bcb55942",
                      "provinceName": "Bulacan",
                      "provinceNameUppercased": "BULACAN",
                      "region": "60530f205d8baa22bcb55919",
                      "dateCreated": "2021-03-18T08:28:16.392Z",
                      "lastUpdated": "2021-03-18T08:28:16.392Z"
                  },
                  {
                      "_id": "60530f205d8baa22bcb5593c",
                      "provinceName": "Cagayan",
                      "provinceNameUppercased": "CAGAYAN",
                      "region": "60530f205d8baa22bcb55918",
                      "dateCreated": "2021-03-18T08:28:16.391Z",
                      "lastUpdated": "2021-03-18T08:28:16.391Z"
                  },
                  {
                      "_id": "60530f205d8baa22bcb55952",
                      "provinceName": "Camarines Norte",
                      "provinceNameUppercased": "CAMARINES NORTE",
                      "region": "60530f205d8baa22bcb5591c",
                      "dateCreated": "2021-03-18T08:28:16.393Z",
                      "lastUpdated": "2021-03-18T08:28:16.393Z"
                  },
                  {
                      "_id": "60530f205d8baa22bcb55953",
                      "provinceName": "Camarines Sur",
                      "provinceNameUppercased": "CAMARINES SUR",
                      "region": "60530f205d8baa22bcb5591c",
                      "dateCreated": "2021-03-18T08:28:16.393Z",
                      "lastUpdated": "2021-03-18T08:28:16.393Z"
                  },
                  {
                      "_id": "60530f205d8baa22bcb55925",
                      "provinceName": "Camiguin",
                      "provinceNameUppercased": "CAMIGUIN",
                      "region": "60530f205d8baa22bcb55913",
                      "dateCreated": "2021-03-18T08:28:16.389Z",
                      "lastUpdated": "2021-03-18T08:28:16.389Z"
                  },
                  {
                      "_id": "60530f205d8baa22bcb55959",
                      "provinceName": "Capiz",
                      "provinceNameUppercased": "CAPIZ",
                      "region": "60530f205d8baa22bcb5591d",
                      "dateCreated": "2021-03-18T08:28:16.396Z",
                      "lastUpdated": "2021-03-18T08:28:16.396Z"
                  },
                  {
                      "_id": "60530f205d8baa22bcb55954",
                      "provinceName": "Catanduanes",
                      "provinceNameUppercased": "CATANDUANES",
                      "region": "60530f205d8baa22bcb5591c",
                      "dateCreated": "2021-03-18T08:28:16.394Z",
                      "lastUpdated": "2021-03-18T08:28:16.394Z"
                  },
                  {
                      "_id": "60530f205d8baa22bcb55948",
                      "provinceName": "Cavite",
                      "provinceNameUppercased": "CAVITE",
                      "region": "60530f205d8baa22bcb5591a",
                      "dateCreated": "2021-03-18T08:28:16.392Z",
                      "lastUpdated": "2021-03-18T08:28:16.392Z"
                  },
                  {
                      "_id": "60530f205d8baa22bcb5595e",
                      "provinceName": "Cebu",
                      "provinceNameUppercased": "CEBU",
                      "region": "60530f205d8baa22bcb5591e",
                      "dateCreated": "2021-03-18T08:28:16.400Z",
                      "lastUpdated": "2021-03-18T08:28:16.400Z"
                  },
                  {
                      "_id": "60530f205d8baa22bcb55929",
                      "provinceName": "Compostela Valley",
                      "provinceNameUppercased": "COMPOSTELA VALLEY",
                      "region": "60530f205d8baa22bcb55914",
                      "dateCreated": "2021-03-18T08:28:16.389Z",
                      "lastUpdated": "2021-03-18T08:28:16.389Z"
                  },
                  {
                      "_id": "60530f205d8baa22bcb5592e",
                      "provinceName": "Cotabato (North Cot.)",
                      "provinceNameUppercased": "COTABATO (NORTH COT.)",
                      "region": "60530f205d8baa22bcb55915",
                      "dateCreated": "2021-03-18T08:28:16.390Z",
                      "lastUpdated": "2021-03-18T08:28:16.390Z"
                  },
                  {
                      "_id": "60530f205d8baa22bcb5592a",
                      "provinceName": "Davao (Davao Del Norte)",
                      "provinceNameUppercased": "DAVAO (DAVAO DEL NORTE)",
                      "region": "60530f205d8baa22bcb55914",
                      "dateCreated": "2021-03-18T08:28:16.389Z",
                      "lastUpdated": "2021-03-18T08:28:16.389Z"
                  },
                  {
                      "_id": "60530f205d8baa22bcb5592b",
                      "provinceName": "Davao Del Sur",
                      "provinceNameUppercased": "DAVAO DEL SUR",
                      "region": "60530f205d8baa22bcb55914",
                      "dateCreated": "2021-03-18T08:28:16.390Z",
                      "lastUpdated": "2021-03-18T08:28:16.390Z"
                  },
                  {
                      "_id": "60530f205d8baa22bcb5592c",
                      "provinceName": "Davao Occidental",
                      "provinceNameUppercased": "DAVAO OCCIDENTAL",
                      "region": "60530f205d8baa22bcb55914",
                      "dateCreated": "2021-03-18T08:28:16.390Z",
                      "lastUpdated": "2021-03-18T08:28:16.390Z"
                  },
                  {
                      "_id": "60530f205d8baa22bcb5592d",
                      "provinceName": "Davao Oriental",
                      "provinceNameUppercased": "DAVAO ORIENTAL",
                      "region": "60530f205d8baa22bcb55914",
                      "dateCreated": "2021-03-18T08:28:16.390Z",
                      "lastUpdated": "2021-03-18T08:28:16.390Z"
                  },
                  {
                      "_id": "60530f205d8baa22bcb55934",
                      "provinceName": "Dinagat Islands",
                      "provinceNameUppercased": "DINAGAT ISLANDS",
                      "region": "60530f205d8baa22bcb55916",
                      "dateCreated": "2021-03-18T08:28:16.391Z",
                      "lastUpdated": "2021-03-18T08:28:16.391Z"
                  },
                  {
                      "_id": "60530f205d8baa22bcb55962",
                      "provinceName": "Eastern Samar",
                      "provinceNameUppercased": "EASTERN SAMAR",
                      "region": "60530f205d8baa22bcb5591f",
                      "dateCreated": "2021-03-18T08:28:16.402Z",
                      "lastUpdated": "2021-03-18T08:28:16.402Z"
                  },
                  {
                      "_id": "60530f205d8baa22bcb5595a",
                      "provinceName": "Guimaras",
                      "provinceNameUppercased": "GUIMARAS",
                      "region": "60530f205d8baa22bcb5591d",
                      "dateCreated": "2021-03-18T08:28:16.398Z",
                      "lastUpdated": "2021-03-18T08:28:16.398Z"
                  },
                  {
                      "_id": "60530f205d8baa22bcb55972",
                      "provinceName": "Ifugao",
                      "provinceNameUppercased": "IFUGAO",
                      "region": "60530f205d8baa22bcb55922",
                      "dateCreated": "2021-03-18T08:28:16.403Z",
                      "lastUpdated": "2021-03-18T08:28:16.403Z"
                  },
                  {
                      "_id": "60530f205d8baa22bcb55937",
                      "provinceName": "Ilocos Norte",
                      "provinceNameUppercased": "ILOCOS NORTE",
                      "region": "60530f205d8baa22bcb55917",
                      "dateCreated": "2021-03-18T08:28:16.391Z",
                      "lastUpdated": "2021-03-18T08:28:16.391Z"
                  },
                  {
                      "_id": "60530f205d8baa22bcb55938",
                      "provinceName": "Ilocos Sur",
                      "provinceNameUppercased": "ILOCOS SUR",
                      "region": "60530f205d8baa22bcb55917",
                      "dateCreated": "2021-03-18T08:28:16.391Z",
                      "lastUpdated": "2021-03-18T08:28:16.391Z"
                  },
                  {
                      "_id": "60530f205d8baa22bcb5595b",
                      "provinceName": "Iloilo",
                      "provinceNameUppercased": "ILOILO",
                      "region": "60530f205d8baa22bcb5591d",
                      "dateCreated": "2021-03-18T08:28:16.399Z",
                      "lastUpdated": "2021-03-18T08:28:16.399Z"
                  },
                  {
                      "_id": "60530f205d8baa22bcb5593d",
                      "provinceName": "Isabela",
                      "provinceNameUppercased": "ISABELA",
                      "region": "60530f205d8baa22bcb55918",
                      "dateCreated": "2021-03-18T08:28:16.391Z",
                      "lastUpdated": "2021-03-18T08:28:16.391Z"
                  },
                  {
                      "_id": "60530f205d8baa22bcb55973",
                      "provinceName": "Kalinga",
                      "provinceNameUppercased": "KALINGA",
                      "region": "60530f205d8baa22bcb55922",
                      "dateCreated": "2021-03-18T08:28:16.403Z",
                      "lastUpdated": "2021-03-18T08:28:16.403Z"
                  },
                  {
                      "_id": "60530f205d8baa22bcb55939",
                      "provinceName": "La Union",
                      "provinceNameUppercased": "LA UNION",
                      "region": "60530f205d8baa22bcb55917",
                      "dateCreated": "2021-03-18T08:28:16.391Z",
                      "lastUpdated": "2021-03-18T08:28:16.391Z"
                  },
                  {
                      "_id": "60530f205d8baa22bcb55949",
                      "provinceName": "Laguna",
                      "provinceNameUppercased": "LAGUNA",
                      "region": "60530f205d8baa22bcb5591a",
                      "dateCreated": "2021-03-18T08:28:16.392Z",
                      "lastUpdated": "2021-03-18T08:28:16.392Z"
                  },
                  {
                      "_id": "60530f205d8baa22bcb55926",
                      "provinceName": "Lanao Del Norte",
                      "provinceNameUppercased": "LANAO DEL NORTE",
                      "region": "60530f205d8baa22bcb55913",
                      "dateCreated": "2021-03-18T08:28:16.389Z",
                      "lastUpdated": "2021-03-18T08:28:16.389Z"
                  },
                  {
                      "_id": "60530f205d8baa22bcb5596b",
                      "provinceName": "Lanao Del Sur",
                      "provinceNameUppercased": "LANAO DEL SUR",
                      "region": "60530f205d8baa22bcb55921",
                      "dateCreated": "2021-03-18T08:28:16.403Z",
                      "lastUpdated": "2021-03-18T08:28:16.403Z"
                  },
                  {
                      "_id": "60530f205d8baa22bcb55963",
                      "provinceName": "Leyte",
                      "provinceNameUppercased": "LEYTE",
                      "region": "60530f205d8baa22bcb5591f",
                      "dateCreated": "2021-03-18T08:28:16.402Z",
                      "lastUpdated": "2021-03-18T08:28:16.402Z"
                  },
                  {
                      "_id": "60530f205d8baa22bcb5596c",
                      "provinceName": "Maguindanao",
                      "provinceNameUppercased": "MAGUINDANAO",
                      "region": "60530f205d8baa22bcb55921",
                      "dateCreated": "2021-03-18T08:28:16.403Z",
                      "lastUpdated": "2021-03-18T08:28:16.403Z"
                  },
                  {
                      "_id": "60530f205d8baa22bcb5594c",
                      "provinceName": "Marinduque",
                      "provinceNameUppercased": "MARINDUQUE",
                      "region": "60530f205d8baa22bcb5591b",
                      "dateCreated": "2021-03-18T08:28:16.393Z",
                      "lastUpdated": "2021-03-18T08:28:16.393Z"
                  },
                  {
                      "_id": "60530f205d8baa22bcb55955",
                      "provinceName": "Masbate",
                      "provinceNameUppercased": "MASBATE",
                      "region": "60530f205d8baa22bcb5591c",
                      "dateCreated": "2021-03-18T08:28:16.394Z",
                      "lastUpdated": "2021-03-18T08:28:16.394Z"
                  },
                  {
                      "_id": "60530f205d8baa22bcb55927",
                      "provinceName": "Misamis Occidental",
                      "provinceNameUppercased": "MISAMIS OCCIDENTAL",
                      "region": "60530f205d8baa22bcb55913",
                      "dateCreated": "2021-03-18T08:28:16.389Z",
                      "lastUpdated": "2021-03-18T08:28:16.389Z"
                  },
                  {
                      "_id": "60530f205d8baa22bcb55928",
                      "provinceName": "Misamis Oriental",
                      "provinceNameUppercased": "MISAMIS ORIENTAL",
                      "region": "60530f205d8baa22bcb55913",
                      "dateCreated": "2021-03-18T08:28:16.389Z",
                      "lastUpdated": "2021-03-18T08:28:16.389Z"
                  },
                  {
                      "_id": "60530f205d8baa22bcb55974",
                      "provinceName": "Mountain Province",
                      "provinceNameUppercased": "MOUNTAIN PROVINCE",
                      "region": "60530f205d8baa22bcb55922",
                      "dateCreated": "2021-03-18T08:28:16.404Z",
                      "lastUpdated": "2021-03-18T08:28:16.404Z"
                  },
                  {
                      "_id": "60530f205d8baa22bcb55976",
                      "provinceName": "National Capital Region - Metro Manila",
                      "provinceNameUppercased": "NATIONAL CAPITAL REGION - METRO MANILA",
                      "region": "60530f205d8baa22bcb55923",
                      "dateCreated": "2021-03-18T08:28:16.404Z",
                      "lastUpdated": "2021-03-18T08:28:16.404Z"
                  },
                  {
                      "_id": "60530f205d8baa22bcb5595c",
                      "provinceName": "Negros Occidental",
                      "provinceNameUppercased": "NEGROS OCCIDENTAL",
                      "region": "60530f205d8baa22bcb5591d",
                      "dateCreated": "2021-03-18T08:28:16.400Z",
                      "lastUpdated": "2021-03-18T08:28:16.400Z"
                  },
                  {
                      "_id": "60530f205d8baa22bcb5595f",
                      "provinceName": "Negros Oriental",
                      "provinceNameUppercased": "NEGROS ORIENTAL",
                      "region": "60530f205d8baa22bcb5591e",
                      "dateCreated": "2021-03-18T08:28:16.401Z",
                      "lastUpdated": "2021-03-18T08:28:16.401Z"
                  },
                  {
                      "_id": "60530f205d8baa22bcb55964",
                      "provinceName": "Northern Samar",
                      "provinceNameUppercased": "NORTHERN SAMAR",
                      "region": "60530f205d8baa22bcb5591f",
                      "dateCreated": "2021-03-18T08:28:16.402Z",
                      "lastUpdated": "2021-03-18T08:28:16.402Z"
                  },
                  {
                      "_id": "60530f205d8baa22bcb55943",
                      "provinceName": "Nueva Ecija",
                      "provinceNameUppercased": "NUEVA ECIJA",
                      "region": "60530f205d8baa22bcb55919",
                      "dateCreated": "2021-03-18T08:28:16.392Z",
                      "lastUpdated": "2021-03-18T08:28:16.392Z"
                  },
                  {
                      "_id": "60530f205d8baa22bcb5593e",
                      "provinceName": "Nueva Vizcaya",
                      "provinceNameUppercased": "NUEVA VIZCAYA",
                      "region": "60530f205d8baa22bcb55918",
                      "dateCreated": "2021-03-18T08:28:16.391Z",
                      "lastUpdated": "2021-03-18T08:28:16.391Z"
                  },
                  {
                      "_id": "60530f205d8baa22bcb5594d",
                      "provinceName": "Occidental Mindoro",
                      "provinceNameUppercased": "OCCIDENTAL MINDORO",
                      "region": "60530f205d8baa22bcb5591b",
                      "dateCreated": "2021-03-18T08:28:16.393Z",
                      "lastUpdated": "2021-03-18T08:28:16.393Z"
                  },
                  {
                      "_id": "60530f205d8baa22bcb5594e",
                      "provinceName": "Oriental Mindoro",
                      "provinceNameUppercased": "ORIENTAL MINDORO",
                      "region": "60530f205d8baa22bcb5591b",
                      "dateCreated": "2021-03-18T08:28:16.393Z",
                      "lastUpdated": "2021-03-18T08:28:16.393Z"
                  },
                  {
                      "_id": "60530f205d8baa22bcb5594f",
                      "provinceName": "Palawan",
                      "provinceNameUppercased": "PALAWAN",
                      "region": "60530f205d8baa22bcb5591b",
                      "dateCreated": "2021-03-18T08:28:16.393Z",
                      "lastUpdated": "2021-03-18T08:28:16.393Z"
                  },
                  {
                      "_id": "60530f205d8baa22bcb55944",
                      "provinceName": "Pampanga",
                      "provinceNameUppercased": "PAMPANGA",
                      "region": "60530f205d8baa22bcb55919",
                      "dateCreated": "2021-03-18T08:28:16.392Z",
                      "lastUpdated": "2021-03-18T08:28:16.392Z"
                  },
                  {
                      "_id": "60530f205d8baa22bcb5593a",
                      "provinceName": "Pangasinan",
                      "provinceNameUppercased": "PANGASINAN",
                      "region": "60530f205d8baa22bcb55917",
                      "dateCreated": "2021-03-18T08:28:16.391Z",
                      "lastUpdated": "2021-03-18T08:28:16.391Z"
                  },
                  {
                      "_id": "60530f205d8baa22bcb5594a",
                      "provinceName": "Quezon",
                      "provinceNameUppercased": "QUEZON",
                      "region": "60530f205d8baa22bcb5591a",
                      "dateCreated": "2021-03-18T08:28:16.393Z",
                      "lastUpdated": "2021-03-18T08:28:16.393Z"
                  },
                  {
                      "_id": "60530f205d8baa22bcb5593f",
                      "provinceName": "Quirino",
                      "provinceNameUppercased": "QUIRINO",
                      "region": "60530f205d8baa22bcb55918",
                      "dateCreated": "2021-03-18T08:28:16.392Z",
                      "lastUpdated": "2021-03-18T08:28:16.392Z"
                  },
                  {
                      "_id": "60530f205d8baa22bcb5594b",
                      "provinceName": "Rizal",
                      "provinceNameUppercased": "RIZAL",
                      "region": "60530f205d8baa22bcb5591a",
                      "dateCreated": "2021-03-18T08:28:16.393Z",
                      "lastUpdated": "2021-03-18T08:28:16.393Z"
                  },
                  {
                      "_id": "60530f205d8baa22bcb55950",
                      "provinceName": "Romblon",
                      "provinceNameUppercased": "ROMBLON",
                      "region": "60530f205d8baa22bcb5591b",
                      "dateCreated": "2021-03-18T08:28:16.393Z",
                      "lastUpdated": "2021-03-18T08:28:16.393Z"
                  },
                  {
                      "_id": "60530f205d8baa22bcb55965",
                      "provinceName": "Samar (Western Samar)",
                      "provinceNameUppercased": "SAMAR (WESTERN SAMAR)",
                      "region": "60530f205d8baa22bcb5591f",
                      "dateCreated": "2021-03-18T08:28:16.402Z",
                      "lastUpdated": "2021-03-18T08:28:16.402Z"
                  },
                  {
                      "_id": "60530f205d8baa22bcb5592f",
                      "provinceName": "Sarangani",
                      "provinceNameUppercased": "SARANGANI",
                      "region": "60530f205d8baa22bcb55915",
                      "dateCreated": "2021-03-18T08:28:16.390Z",
                      "lastUpdated": "2021-03-18T08:28:16.390Z"
                  },
                  {
                      "_id": "60530f205d8baa22bcb55960",
                      "provinceName": "Siquijor",
                      "provinceNameUppercased": "SIQUIJOR",
                      "region": "60530f205d8baa22bcb5591e",
                      "dateCreated": "2021-03-18T08:28:16.401Z",
                      "lastUpdated": "2021-03-18T08:28:16.401Z"
                  },
                  {
                      "_id": "60530f205d8baa22bcb55956",
                      "provinceName": "Sorsogon",
                      "provinceNameUppercased": "SORSOGON",
                      "region": "60530f205d8baa22bcb5591c",
                      "dateCreated": "2021-03-18T08:28:16.394Z",
                      "lastUpdated": "2021-03-18T08:28:16.394Z"
                  },
                  {
                      "_id": "60530f205d8baa22bcb55930",
                      "provinceName": "South Cotabato",
                      "provinceNameUppercased": "SOUTH COTABATO",
                      "region": "60530f205d8baa22bcb55915",
                      "dateCreated": "2021-03-18T08:28:16.390Z",
                      "lastUpdated": "2021-03-18T08:28:16.390Z"
                  },
                  {
                      "_id": "60530f205d8baa22bcb55966",
                      "provinceName": "Southern Leyte",
                      "provinceNameUppercased": "SOUTHERN LEYTE",
                      "region": "60530f205d8baa22bcb5591f",
                      "dateCreated": "2021-03-18T08:28:16.402Z",
                      "lastUpdated": "2021-03-18T08:28:16.402Z"
                  },
                  {
                      "_id": "60530f205d8baa22bcb55931",
                      "provinceName": "Sultan Kudarat",
                      "provinceNameUppercased": "SULTAN KUDARAT",
                      "region": "60530f205d8baa22bcb55915",
                      "dateCreated": "2021-03-18T08:28:16.390Z",
                      "lastUpdated": "2021-03-18T08:28:16.390Z"
                  },
                  {
                      "_id": "60530f205d8baa22bcb5596d",
                      "provinceName": "Sulu",
                      "provinceNameUppercased": "SULU",
                      "region": "60530f205d8baa22bcb55921",
                      "dateCreated": "2021-03-18T08:28:16.403Z",
                      "lastUpdated": "2021-03-18T08:28:16.403Z"
                  },
                  {
                      "_id": "60530f205d8baa22bcb55935",
                      "provinceName": "Surigao Del Norte",
                      "provinceNameUppercased": "SURIGAO DEL NORTE",
                      "region": "60530f205d8baa22bcb55916",
                      "dateCreated": "2021-03-18T08:28:16.391Z",
                      "lastUpdated": "2021-03-18T08:28:16.391Z"
                  },
                  {
                      "_id": "60530f205d8baa22bcb55936",
                      "provinceName": "Surigao Del Sur",
                      "provinceNameUppercased": "SURIGAO DEL SUR",
                      "region": "60530f205d8baa22bcb55916",
                      "dateCreated": "2021-03-18T08:28:16.391Z",
                      "lastUpdated": "2021-03-18T08:28:16.391Z"
                  },
                  {
                      "_id": "60530f205d8baa22bcb55945",
                      "provinceName": "Tarlac",
                      "provinceNameUppercased": "TARLAC",
                      "region": "60530f205d8baa22bcb55919",
                      "dateCreated": "2021-03-18T08:28:16.392Z",
                      "lastUpdated": "2021-03-18T08:28:16.392Z"
                  },
                  {
                      "_id": "60530f205d8baa22bcb5596e",
                      "provinceName": "Tawi-Tawi",
                      "provinceNameUppercased": "TAWI-TAWI",
                      "region": "60530f205d8baa22bcb55921",
                      "dateCreated": "2021-03-18T08:28:16.403Z",
                      "lastUpdated": "2021-03-18T08:28:16.403Z"
                  },
                  {
                      "_id": "60530f205d8baa22bcb55946",
                      "provinceName": "Zambales",
                      "provinceNameUppercased": "ZAMBALES",
                      "region": "60530f205d8baa22bcb55919",
                      "dateCreated": "2021-03-18T08:28:16.392Z",
                      "lastUpdated": "2021-03-18T08:28:16.392Z"
                  },
                  {
                      "_id": "60530f205d8baa22bcb55967",
                      "provinceName": "Zamboanga Del Norte",
                      "provinceNameUppercased": "ZAMBOANGA DEL NORTE",
                      "region": "60530f205d8baa22bcb55920",
                      "dateCreated": "2021-03-18T08:28:16.402Z",
                      "lastUpdated": "2021-03-18T08:28:16.402Z"
                  },
                  {
                      "_id": "60530f205d8baa22bcb55968",
                      "provinceName": "Zamboanga Del Sur",
                      "provinceNameUppercased": "ZAMBOANGA DEL SUR",
                      "region": "60530f205d8baa22bcb55920",
                      "dateCreated": "2021-03-18T08:28:16.402Z",
                      "lastUpdated": "2021-03-18T08:28:16.402Z"
                  },
                  {
                      "_id": "60530f205d8baa22bcb55969",
                      "provinceName": "Zamboanga Sibugay",
                      "provinceNameUppercased": "ZAMBOANGA SIBUGAY",
                      "region": "60530f205d8baa22bcb55920",
                      "dateCreated": "2021-03-18T08:28:16.402Z",
                      "lastUpdated": "2021-03-18T08:28:16.402Z"
                  }
              ]
          }
      }
    title: Response
    language: json
---
