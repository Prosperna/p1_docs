---
title: /business-profile/store/update/store-pixel
position_number: 1.4
type: put
description: Save/Update store FB Pixel tracking code

content_markdown: |-
  | ***Request Body***         | ***Data Type*** | ***Required*** | ***Description*** |
  |--------------------|-----------|----------|------------------------------------|
  | storeId               | string    | Yes      | Store id |
  | storeFbPixel               | string    | Yes      | **PAID FEATURE** Updated store FB Pixel tracking code |

left_code_blocks:
  - code_block: |-
      var axios = require('axios');
      var data = JSON.stringify({
        "storeId": "636f0d682b74aa4017606d52",
        "storeFbPixel": "fb_pixel"
      });

      var config = {
        method: 'put',
        url: 'api.prosperna.com/v1/business-profile/store/update/store-pixel',
        data : data
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
          "message": "Facebook Pixel successfully updated.",
          "data": {
              "store": {
                  "additionalFee": 0,
                  "xenplatform_user_id": "",
                  "alreadyAvailedPaidPlan": false,
                  "_id": "63760ee5a3444c4d444c158c",
                  "storeOwner": "63760ee35f12fa931cbb3dea",
                  "storeName": "updated_store_name",
                  "storeAlias": "updatedstorename",
                  "storeIndustry": "604718297aa0fb376c0fcca9",
                  "storeSharingPrefixDesc": "",
                  "storeLogo": "store_logo_url",
                  "storePrimaryColor": "#d05353",
                  "storeSecondaryColor": "#000",
                  "cookiePolicy": true,
                  "cookiePolicyTheme": "Dark",
                  "requireSelectingStoreLocation": true,
                  "shouldSaveFbLead": false,
                  "isGuestCheckoutVerification": false,
                  "isStoreEnabled": false,
                  "isEnabledOnlinePayment": false,
                  "isVerifiedBankForOnlinePayment": false,
                  "convenienceFeeSeller": 50,
                  "convenienceFeeBuyer": 0,
                  "shippingOptions": {
                      "STANDARD": null,
                      "SAMEDAY_SCHED": null,
                      "OWN_BOOKING": false,
                      "PICKUP": false
                  },
                  "alreadyAvailedPlusPlan": false,
                  "payPlanType": "PLUS",
                  "billingType": "NONE",
                  "billing": {
                      "free_visitor_limit": 100,
                      "paid_visitor_limit": 0,
                      "p1_users": 1,
                      "paid_p1_users": 0
                  },
                  "billingVerificationId": [],
                  "alreadyClaimedFreeTrial": false,
                  "redirectToCustomDomain": false,
                  "redirectToCustomSubDomain": false,
                  "billingCutOffDate": 17,
                  "dateCreated": "2022-11-17T10:37:25.120Z",
                  "lastUpdated": "2022-11-17T10:37:25.121Z",
                  "storeSlogan": "New slogan",
                  "facebookLink": "facebook_link",
                  "instagramLink": "instagram_link",
                  "linkedinLink": "linkedin_link",
                  "twitterLink": "twitter_link",
                  "customSubDomain": "custom_p1_subdomain",
                  "customDomain": "custom_domain_link",
                  "fbPixel": "fb_pixel_code",
                  "googleTrackingCode": "google_tracking_code",
                  "privacyPolicyLink": "privacy_policy_link",
                  "updatedAt": "2023-03-26T05:57:13.881Z",
                  "lastTransaction": "2023-03-26T05:57:13.900Z",
                  "storeFavicon": "storefavicon_url",
              }
          }
      }
    title: Response
    language: json
---
