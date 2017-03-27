## Serviceability Responses

**Endpoint Summary**

| Action | Endpoint |
| ------ | -------- |
| List all Serviceability Responses | GET /serviceability-responses |
| Get a single Serviceability Response | GET /serviceability-responses/{id} |
| Create a new Serviceability Response | POST /serviceability-responses |
| Replace the Serviceability Response by replacing the serviceability attribute with the instance provided | PUT /serviceability-responses/{id} |
| Update the Serviceability Response | PATCH /serviceability-responses/{id} |
| Remove an existing Serviceability Response based on the ID provided in query string | DELETE /serviceability-responses/{id} |
| Cancel a Serviceability Response | POST /serviceability-responses/{id}/cancel |


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
      "status": "UNDER_REVIEW",
      "projectId": "PRJ-CC-12345678",
      "servicebilityRequestId": "SRQ-CC-13043135",
      "buyerId": "Comcast",
      "sellerId": "Cox",
      "mpoeOnly": false,
      "expirationDate": "2016-09-26T12:00:00.333Z",
      "serviceSite" :{
        "objectType": "serviceSiteInformation",
        "siteCustomerName": "Quik Clean and Press",
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
      "confidence": {
        "objectType": "serviceabilityConfidence",
        "color": "YELLOW",
        "estimatedResponseDate": "2016-09-26T12:00:00.333Z",
        "reason": "Site Survey Required"
      },
      "installationInterval": 45,
      "productSpecification": {
        "objectType": "productSpecification",
        "id": "PRD_GA_998",
        "productName": "Fast Access EPL",
        "productCode": "AE 1G",
        "productType": "ACCESS_EPL",
        "productCategory": "ETHERNET",
        "productSpecDetail": {
          "objectType": "ethernetProductSpecDetail",
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
        "quote": {
          "objectType": "quote",
          "id": "QT_GA_88754",
          "pricing": [
            {
              "objectType": "pricing",
              "pricingTerm": 24,
              "oneTimeCharges": [
                {
                  "objectType": "oneTimeCharge",
                  "name": "Provisioning",
                  "price": {
                    "amount": 65,
                    "units": "USD"
                  }
                }
              ],
              "recurringCharges": [
                {
                  "objectType": "recurringCharge",
                  "name": "Installation",
                  "period": "MONTHLY",
                  "price": {
                    "amount": 150,
                    "units": "USD"
                  }
                }
              ]
            }
          ]
        },
        "features": [
          {
            "objectType": "productSpecification",
            "id": "PRD_UA_234",
            "productName": "1 Gb UNI",
            "productCode": "U 1G",
            "productType": "UNI",
            "productCategory": "ETHERNET",
            "productSpecDetail": {
              "objectType": "uniProductSpecDetail",
              "portSpeed": {
                "objectType": "informationRateQuantity",
                "amount": 10,
                "quantity": "Mbps"
              }
            },
            "quote": {
              "objectType": "quote",
              "id": "QT_U_623",
              "pricing": [
                {
                  "objectType": "pricing",
                  "pricingTerm": 24,
                  "oneTimeCharges": [
                    {
                      "objectType": "oneTimeCharge",
                      "name": "Installation",
                      "price": {
                        "amount": 1100,
                        "units": "USD"
                      }
                    }
                  ],
                  "recurringCharges": [
                    {
                      "objectType": "recurringCharge",
                      "name": "Installation",
                      "period": "MONTHLY",
                      "price": {
                        "amount": 85,
                        "units": "USD"
                      }
                    }
                  ]
                }
              ]
            },
            "construction": {
              "quote": {
                "objectType": "quote",
                "id": "QT_CON_3483",
                "pricing": [
                  {
                    "objectType": "pricing",
                    "pricingTerm": 24,
                    "oneTimeCharges": [
                      {
                        "objectType": "oneTimeCharge",
                        "name": "Facilities to building",
                        "price": {
                          "amount": 1500,
                          "units": "USD"
                        }
                      },
                      {
                        "objectType": "oneTimeCharge",
                        "name": "Inside cabling to suite",
                        "price": {
                          "amount": 650,
                          "units": "USD"
                        }
                      }
                    ]
                  }
                ]
              }
            }
          }
        ]
      }
    }
  ]
}
```

### Get a Serviceability response

```
GET /serviceability-responses/:id
```

Retrieve a Serviceability Response by id.

**Response**

Status: 200 OK
``` JSON
{
  "objectType": "serviceabilityResponse",
  "id": "SRR-CC-726349",
  "link": {
    "href": "/api/serviceability-requests/SRR-CC-726349"
  },
  "status": "UNDER_REVIEW",
  "projectId": "PRJ-CC-12345678",
  "servicebilityRequestId": "SRQ-CC-726349",
  "buyerId": "Comcast",
  "sellerId": "Cox",
  "mpoeOnly": false,
  "expirationDate": "2016-09-26T12:00:00.333Z",
  "serviceSite" :{
    "objectType": "serviceSiteInformation",
    "siteCustomerName": "Quik Clean and Press",
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
  "confidence": {
    "objectType": "serviceabilityConfidence",
    "color": "YELLOW",
    "estimatedResponseDate": "2016-09-26T12:00:00.333Z",
    "reason": "Site Survey Required"
  },
  "installationInterval": 45,
  "productSpecification": {
    "objectType": "productSpecification",
    "id": "PRD_UA_234",
    "productName": "1 Gb UNI",
    "productCode": "U 1G",
    "productType": "UNI",
    "productCategory": "ETHERNET",
    "productSpecDetail": {
      "objectType": "uniProductSpecDetail",
      "portSpeed": {
        "objectType": "informationRateQuantity",
        "amount": 10,
        "quantity": "Mbps"
      }
    },
    "quote": {
      "objectType": "quote",
      "id": "QT_U_623",
      "pricing": [
        {
          "objectType": "pricing",
          "pricingTerm": 24,
          "oneTimeCharges": [
            {
              "objectType": "oneTimeCharge",
              "name": "Installation",
              "price": {
                "amount": 1100,
                "units": "USD"
              }
            }
          ],
          "recurringCharges": [
            {
              "objectType": "recurringCharge",
              "name": "Installation",
              "period": "MONTHLY",
              "price": {
                "amount": 85,
                "units": "USD"
              }
            }
          ]
        }
      ]
    },
    "construction": {
      "quote": {
        "objectType": "quote",
        "id": "QT_CON_3483",
        "pricing": [
          {
            "objectType": "pricing",
            "pricingTerm": 24,
            "oneTimeCharges": [
              {
                "objectType": "oneTimeCharge",
                "name": "Facilities to building",
                "price": {
                  "amount": 1500,
                  "units": "USD"
                }
              },
              {
                "objectType": "oneTimeCharge",
                "name": "Inside cabling to suite",
                "price": {
                  "amount": 650,
                  "units": "USD"
                }
              }
            ]
          }
        ]
      }
    }
  }
}
```

### Create a Serviceability Response

```
POST /serviceability-responses
```
Retrieve all Serviceability Responses.

**Request**

``` JSON
{
  "objectType": "serviceabilityResponse",
  "status": "UNDER_REVIEW",
  "projectId": "PRJ-CC-12345678",
  "servicebilityRequestId": "SRQ-CC-13043135",
  "buyerId": "Comcast",
  "sellerId": "Cox",
  "mpoeOnly": false,
  "expirationDate": "2016-09-26T12:00:00.333Z",
  "serviceSite" :{
    "objectType": "serviceSiteInformation",
    "siteCustomerName": "Quik Clean and Press",
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
  "confidence": {
    "objectType": "serviceabilityConfidence",
    "color": "YELLOW",
    "estimatedResponseDate": "2016-09-26T12:00:00.333Z",
    "reason": "Site Survey Required"
  },
  "installationInterval": 45,
  "productSpecification": {
    "objectType": "productSpecification",
    "id": "PRD_GA_998",
    "productName": "Fast Access EPL",
    "productCode": "AE 1G",
    "productType": "ACCESS_EPL",
    "productCategory": "ETHERNET",
    "productSpecDetail": {
      "objectType": "ethernetProductSpecDetail",
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
    "quote": {
      "objectType": "quote",
      "id": "QT_GA_88754",
      "pricing": [
        {
          "objectType": "pricing",
          "pricingTerm": 24,
          "oneTimeCharges": [
            {
              "objectType": "oneTimeCharge",
              "name": "Provisioning",
              "price": {
                "amount": 65,
                "units": "USD"
              }
            }
          ],
          "recurringCharges": [
            {
              "objectType": "recurringCharge",
              "name": "Installation",
              "period": "MONTHLY",
              "price": {
                "amount": 150,
                "units": "USD"
              }
            }
          ]
        }
      ]
    }
  }
}
```

**Response**

Status: 201 Created
``` JSON
{
  "objectType": "serviceabilityResponse",
  "id": "SRR-CC-726349",
  "link": {
    "href": "/api/serviceability-requests/SRR-CC-726349"
  },
  "status": "UNDER_REVIEW",
  "projectId": "PRJ-CC-12345678",
  "servicebilityRequestId": "SRQ-CC-13043135",
  "buyerId": "Comcast",
  "sellerId": "Cox",
  "mpoeOnly": false,
  "expirationDate": "2016-09-26T12:00:00.333Z",
  "serviceSite" :{
    "objectType": "serviceSiteInformation",
    "siteCustomerName": "Quik Clean and Press",
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
  "confidence": {
    "objectType": "serviceabilityConfidence",
    "color": "YELLOW",
    "estimatedResponseDate": "2016-09-26T12:00:00.333Z",
    "reason": "Site Survey Required"
  },
  "installationInterval": 45,
  "productSpecification": {
    "objectType": "productSpecification",
    "id": "PRD_GA_998",
    "productName": "Fast Access EPL",
    "productCode": "AE 1G",
    "productType": "ACCESS_EPL",
    "productCategory": "ETHERNET",
    "productSpecDetail": {
      "objectType": "ethernetProductSpecDetail",
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
    "quote": {
      "objectType": "quote",
      "id": "QT_GA_88754",
      "pricing": [
        {
          "objectType": "pricing",
          "pricingTerm": 24,
          "oneTimeCharges": [
            {
              "objectType": "oneTimeCharge",
              "name": "Provisioning",
              "price": {
                "amount": 65,
                "units": "USD"
              }
            }
          ],
          "recurringCharges": [
            {
              "objectType": "recurringCharge",
              "name": "Installation",
              "period": "MONTHLY",
              "price": {
                "amount": 150,
                "units": "USD"
              }
            }
          ]
        }
      ]
    }
  }
}
```

### Replace a Serviceability Response

```
PUT /serviceability-responses/:id
```
Update a Serviceability Request by providing a full replacement.

**Request**

``` JSON
{
  "objectType": "serviceabilityResponse",
  "status": "UNDER_REVIEW",
  "projectId": "PRJ-CC-12345678",
  "servicebilityRequestId": "SRQ-CC-13043135",
  "buyerId": "Comcast",
  "sellerId": "Cox",
  "mpoeOnly": false,
  "expirationDate": "2016-09-26T12:00:00.333Z",
  "serviceSite" :{
    "objectType": "serviceSiteInformation",
    "siteCustomerName": "Quik Clean and Press",
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
  "confidence": {
    "objectType": "serviceabilityConfidence",
    "color": "YELLOW",
    "estimatedResponseDate": "2016-09-26T12:00:00.333Z",
    "reason": "Site Survey Required"
  },
  "installationInterval": 45,
  "productSpecification": {
    "objectType": "productSpecification",
    "id": "PRD_GA_998",
    "productName": "Fast Access EPL",
    "productCode": "AE 1G",
    "productType": "ACCESS_EPL",
    "productCategory": "ETHERNET",
    "productSpecDetail": {
      "objectType": "ethernetProductSpecDetail",
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
    "quote": {
      "objectType": "quote",
      "id": "QT_GA_88754",
      "pricing": [
        {
          "objectType": "pricing",
          "pricingTerm": 24,
          "oneTimeCharges": [
            {
              "objectType": "oneTimeCharge",
              "name": "Provisioning",
              "price": {
                "amount": 65,
                "units": "USD"
              }
            }
          ],
          "recurringCharges": [
            {
              "objectType": "recurringCharge",
              "name": "Installation",
              "period": "MONTHLY",
              "price": {
                "amount": 150,
                "units": "USD"
              }
            }
          ]
        }
      ]
    }
  }
}
```

**Response**

Status: 200 OK
``` JSON
{
  "objectType": "serviceabilityResponse",
  "id": "SRR-CC-726349",
  "link": {
    "href": "/api/serviceability-requests/SRR-CC-726349"
  },
  "status": "UNDER_REVIEW",
  "projectId": "PRJ-CC-12345678",
  "servicebilityRequestId": "SRQ-CC-13043135",
  "buyerId": "Comcast",
  "sellerId": "Cox",
  "mpoeOnly": false,
  "expirationDate": "2016-09-26T12:00:00.333Z",
  "serviceSite" :{
    "objectType": "serviceSiteInformation",
    "siteCustomerName": "Quik Clean and Press",
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
  "confidence": {
    "objectType": "serviceabilityConfidence",
    "color": "YELLOW",
    "estimatedResponseDate": "2016-09-26T12:00:00.333Z",
    "reason": "Site Survey Required"
  },
  "installationInterval": 45,
  "productSpecification": {
    "objectType": "productSpecification",
    "id": "PRD_GA_998",
    "productName": "Fast Access EPL",
    "productCode": "AE 1G",
    "productType": "ACCESS_EPL",
    "productCategory": "ETHERNET",
    "productSpecDetail": {
      "objectType": "ethernetProductSpecDetail",
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
    "quote": {
      "objectType": "quote",
      "id": "QT_GA_88754",
      "pricing": [
        {
          "objectType": "pricing",
          "pricingTerm": 24,
          "oneTimeCharges": [
            {
              "objectType": "oneTimeCharge",
              "name": "Provisioning",
              "price": {
                "amount": 65,
                "units": "USD"
              }
            }
          ],
          "recurringCharges": [
            {
              "objectType": "recurringCharge",
              "name": "Installation",
              "period": "MONTHLY",
              "price": {
                "amount": 150,
                "units": "USD"
              }
            }
          ]
        }
      ]
    }
  }
}
```

### Update a Serviceability Response

```
PATCH /serviceability-responses/:id
```
Update a Serviceability Request.

**Request**

``` JSON
{
  "objectType": "serviceabilityResponse",
  "status": "UNDER_REVIEW",
  "projectId": "PRJ-CC-12345678",
  "servicebilityRequestId": "SRQ-CC-13043135",
  "buyerId": "Comcast",
  "sellerId": "Cox",
  "mpoeOnly": false,
  "expirationDate": "2016-09-26T12:00:00.333Z",
  "serviceSite" :{
    "objectType": "serviceSiteInformation",
    "siteCustomerName": "Quik Clean and Press",
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
  "confidence": {
    "objectType": "serviceabilityConfidence",
    "color": "YELLOW",
    "estimatedResponseDate": "2016-09-26T12:00:00.333Z",
    "reason": "Site Survey Required"
  },
  "installationInterval": 45,
  "productSpecification": {
    "objectType": "productSpecification",
    "id": "PRD_GA_998",
    "productName": "Fast Access EPL",
    "productCode": "AE 1G",
    "productType": "ACCESS_EPL",
    "productCategory": "ETHERNET",
    "productSpecDetail": {
      "objectType": "ethernetProductSpecDetail",
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
    "quote": {
      "objectType": "quote",
      "id": "QT_GA_88754",
      "pricing": [
        {
          "objectType": "pricing",
          "pricingTerm": 24,
          "oneTimeCharges": [
            {
              "objectType": "oneTimeCharge",
              "name": "Provisioning",
              "price": {
                "amount": 65,
                "units": "USD"
              }
            }
          ],
          "recurringCharges": [
            {
              "objectType": "recurringCharge",
              "name": "Installation",
              "period": "MONTHLY",
              "price": {
                "amount": 150,
                "units": "USD"
              }
            }
          ]
        }
      ]
    }
  }
}
```

**Response**

Status: 200 OK
``` JSON
{
  "objectType": "serviceabilityResponse",
  "id": "SRR-CC-726349",
  "link": {
    "href": "/api/serviceability-requests/SRR-CC-726349"
  },
  "status": "UNDER_REVIEW",
  "projectId": "PRJ-CC-12345678",
  "servicebilityRequestId": "SRQ-CC-13043135",
  "buyerId": "Comcast",
  "sellerId": "Cox",
  "mpoeOnly": false,
  "expirationDate": "2016-09-26T12:00:00.333Z",
  "serviceSite" :{
    "objectType": "serviceSiteInformation",
    "siteCustomerName": "Quik Clean and Press",
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
  "confidence": {
    "objectType": "serviceabilityConfidence",
    "color": "YELLOW",
    "estimatedResponseDate": "2016-09-26T12:00:00.333Z",
    "reason": "Site Survey Required"
  },
  "installationInterval": 45,
  "productSpecification": {
    "objectType": "productSpecification",
    "id": "PRD_GA_998",
    "productName": "Fast Access EPL",
    "productCode": "AE 1G",
    "productType": "ACCESS_EPL",
    "productCategory": "ETHERNET",
    "productSpecDetail": {
      "objectType": "ethernetProductSpecDetail",
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
    "quote": {
      "objectType": "quote",
      "id": "QT_GA_88754",
      "pricing": [
        {
          "objectType": "pricing",
          "pricingTerm": 24,
          "oneTimeCharges": [
            {
              "objectType": "oneTimeCharge",
              "name": "Provisioning",
              "price": {
                "amount": 65,
                "units": "USD"
              }
            }
          ],
          "recurringCharges": [
            {
              "objectType": "recurringCharge",
              "name": "Installation",
              "period": "MONTHLY",
              "price": {
                "amount": 150,
                "units": "USD"
              }
            }
          ]
        }
      ]
    }
  }
}
```

### Cancel a Serviceability Response

```
POST /orders/{id}/cancel
```
Allow a Seller to Cancel a Serviceability Response.

**Response**

Status: 201 Cancelled


### Cancel a Serviceability Response

```
DELETE /orders/{id}
```
Allow a Seller to Cancel a Serviceability Response.

**Response**

Status: 204 Success
