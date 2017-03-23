## Serviceability Responses

**Endpoint Summary**

| Action | Endpoint |
| ------ | -------- |
| List all Serviceability Responses | GET /serviceability-responses |
| Create a new Serviceability Response | POST /serviceability-responses |
| Get a single Serviceability Response | GET /serviceability-responses/{id} |
| Update the Serviceability Response by replacing the serviceability attribute with the instance provided | PUT /serviceability-responses/{id} |
| Remove an existing Serviceability Response based on the ID provided in query string | DELETE /serviceability-responses/{id} |
| Cancel a Serviceability Response | POST /serviceability-responses/{id}/cancel |

**Endpoint Descriptions and Examples**

### List all Serviceability responses

```
GET /serviceability-responses
```
Retrieve all Serviceability Responses.

**Response**

Status: 200 OK
``` JSON
{
  "link": {
    "href": "/api/serviceability-responses"  
  },
  "available": 1,
  "returned": 1,
  "items": [
    {
      "objectType": "serviceabilityResponse",
      "id": "SRR-CC-13043135",
      "link": {
        "href": "/api/serviceability-requests/SRR-CC-13043135"
      },
      "servicebilityRequestId": "SRQ-CC-13043135",
      "buyerId": "Comcast",
      "sellerId": "Cox",
      "status": "UNDER_REVIEW",
      "projectId": "PRJ-CC-12345678",
      "mpoeOnly": false,
      "expirationDate": "2016-09-26T12:00:00.333Z",
      "serviceSite" :{
        "siteAddressType": "FORMATTED_ADDRESS",
        "siteAddress": {
          "addressLine1": "5630 E SANTA ANA CANYON RD",
          "addressLine2": "STE 100",
          "city": "ANAHEIM",
          "stateOrProvince": "CA",
          "country": "USA",
          "postCode": "92807",
          "postCodeExtension": "1234"
        }
      },
      "serviceabilityConfidence": {
        "objectType": "serviceabilityConfidence",
        "color": "YELLOW",
        "estimatedResponseDate": "2016-09-26T12:00:00.333Z",
        "reason": "Site Survey Required"
      },
      "installationInterval": 45,
      "serviceDetails": [
        {
          "objectType": "serviceDetailResponse",
          "productSpecs": [
            {
              "objectType": "productSpecResponse",
              "productName": "Fast Access EPL",
              "productCode": "AE 1G",
              "productType": "ACCESS_EPL",
              "productCategory": "ETHERNET",
              "productSpecDetails": [
                {
                  "objectType": "ethernetProductSpecDetail",
                  "id": "PRODSPEC_6512",
                  "serviceCategory": "ETHERNET",
                  "bandwidth": {
                    "objectType": "informationRateQuantity",
                    "amount": 10,
                    "quantity": "Mbps"
                  },
                  "accessMedium": "COAX",
                  "accessTechnology": "DOCSIS_3.1",
                  "classOfService": "HIGH",
                  "sellerClassOfService": "Real Time",
                  "mtuSize": 1526,
                  "colorForwardingEnabled": false,
                  "enniLocation": {
                    "objectType": "enniLocationResponse",
                    "enniLocationAddressType": "ADDRESS_REFERENCE",
                    "enniLocationAddress": {
                      "objectType": "addressReference",
                      "referenceType": "CLLI",
                      "reference": "ANHMCA17"
                    }
                  }
                },
                {
                  "objectType": "uniProductSpecDetail",
                  "id": "PRODSPEC_U45",
                  "portSpeed": {
                    "objectType": "informationRateQuantity",
                    "amount": 10,
                    "quantity": "Gbps"
                  }
                }
              ],
              "quote": {
                %%%%%%%%%%%%%%%%%%%%%%%%% zipper %%%%%%%%%%%%%%%%%%%%%%%%%%
              }
                }
              ]
            }
          ]
        }
      ],
      "desiredResponseDate": "2016-09-26T12:00:00.333Z"
    }
  ]
}
```

### Get serviceability request

```
GET /serviceability-requests/:id
```
**Response**

Status: 200 OK
``` JSON
{
  "objectType": "serviceabilityRequest",
  "id": "SRQ-CC-13043135",
  "link": {
    "href": "/api/serviceability-requests/SRQ-CC-13043135"
  },
  "buyerId": "Comcast",
  "sellerId": "Cox",
  "status": "Submitted",
  "projectId": "PRJ-CC-12345678",
  "pricingMethod": "CONTRACT",
  "pricingReference": "CC-MES-0192",
  "serviceSite" :{
    "siteAddressType": "FORMATTED_ADDRESS",
    "siteAddress": {
      "addressLine1": "5630 E SANTA ANA CANYON RD",
      "addressLine2": "STE 100",
      "city": "ANAHEIM",
      "stateOrProvince": "CA",
      "country": "USA",
      "postCode": "92807",
      "postCodeExtension": "1234"
    }
  },
  "primarySiteContact": {
    "objectType": "contact",
    "name": "Frederick Fullerton",
    "telephoneNumber": "6574459867",
    "email": "f_fullerton@libertyproperty.com"
  },
  "alternateSiteContact": {
    "objectType": "contact",
    "name": "Betty Buckminster",
    "telephoneNumber": "7147651026",
    "email": "b_buckminster@libertyproperty.com"
  },
  "serviceDetails": [
    {
      "objectType": "serviceDetailRequest",
      "serviceCategory": "ETHERNET",
      "serviceType": "ACCESS_EPL",
      "serviceDetailItems": [
        {
          "objectType": "ethernetDetailItemRequest",
          "bandwidth": {
            "objectType": "informationRateQuantity",
            "amount": 100,
            "quantity": "Mbps"
          },
          "maxPortSpeed": {
            "objectType": "informationRateQuantity",
            "amount": 1,
            "quantity": "Gbps"
          },
          "interfaceType": "OPTICAL",
          "accessMedium": "FIBER",
          "newEnniRequired": false,
          "buyerEnniId": "CC-ENNI-12345678",
          "classOfService": "HIGH",
          "pricingTerm": "24",
          "desiredActivationDate": "2016-10-26T12:00:00.333Z"
        }
      ]
    }
  ],
  "desiredResponseDate": "2016-09-26T12:00:00.333Z"
}
```