## Serviceability Requests

**Endpoint Summary**

| Action | Endpoint |
| ------ | -------- |
| List all serviceability requests | `GET /serviceability-requests` |
| Get a serviceability request (includes all serviceability responses) | `GET /serviceability-requests/:id` |
| Create a serviceability request | `POST /serviceability-requests` |
| Update a serviceability request | `PUT /serviceability-requests/:id` |
| Cancel a serviceability request | `POST /serviceability-requests/:id/cancel` |
| Delete a serviceability request | `DELETE /serviceability-requests/:id` |

### List serviceability requests

```
GET /serviceability-requests
```
**Response**

Status: 200 OK
``` JSON
{
  "link": {
    "href": "/api/serviceability-requests"  
  },
  "available": 1,
  "returned": 1,
  "items": [
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
      "serviceDetail": {
        "objectType": "ethernetServiceDetail",
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
      },
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
  "serviceDetail": {
    "objectType": "ethernetServiceDetail",
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
  },
  "desiredResponseDate": "2016-09-26T12:00:00.333Z"
}
```

### Create serviceability request

```
POST /serviceability-requests
```

**Example**

```JSON
{
  "objectType": "serviceabilityRequest-create-update",
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
  "serviceDetail": {
    "objectType": "ethernetServiceDetail",
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
  },
  "desiredResponseDate": "2016-09-26T12:00:00.333Z"
}
```

**Response**

Status: 201 Created
```JSON
{
  "objectType": "serviceabilityRequest-create-update",
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
  "serviceDetail": {
    "objectType": "ethernetServiceDetail",
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
  },
  "desiredResponseDate": "2016-09-26T12:00:00.333Z"
}
```

### Update serviceability request

```
PUT /serviceability-requests/SRQ-CC-13043135
```

**Example**

```JSON
{
  "objectType": "serviceabilityRequest-create-update",
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
    "name": "Jessie McBride",
    "telephoneNumber": "6578885102",
    "email": "j_mcbride@libertyproperty.com"
  },
  "serviceDetail": {
    "objectType": "ethernetServiceDetail",
    "serviceCategory": "ETHERNET",
    "serviceType": "ACCESS_EPL",
    "serviceDetailItems": [
      {
        "objectType": "ethernetDetailItemRequest",
        "bandwidth": {
          "objectType": "informationRateQuantity",
          "amount": 1,
          "quantity": "Gbps"
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
        "pricingTerm": "12",
        "desiredActivationDate": "2016-10-26T12:00:00.333Z"
      }
    ]
  },
  "desiredResponseDate": "2016-09-26T12:00:00.333Z"
}
```

**Response**

Status: 200 OK
```JSON
{
  "objectType": "serviceabilityRequest-create-update",
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
    "name": "Jessie McBride",
    "telephoneNumber": "6578885102",
    "email": "j_mcbride@libertyproperty.com"
  },
  "serviceDetail": {
    "objectType": "ethernetServiceDetail",
    "serviceCategory": "ETHERNET",
    "serviceType": "ACCESS_EPL",
    "serviceDetailItems": [
      {
        "objectType": "ethernetDetailItemRequest",
        "bandwidth": {
          "objectType": "informationRateQuantity",
          "amount": 1,
          "quantity": "Gbps"
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
        "pricingTerm": "12",
        "desiredActivationDate": "2016-10-26T12:00:00.333Z"
      }
    ]
  },
  "desiredResponseDate": "2016-09-26T12:00:00.333Z"
}
```

### Cancel serviceability request

```
POST /serviceability-requests/SRQ-CC-13043135/cancel
```

**Response**

Status: 200 OK

### Delete serviceability request

```
DELETE /serviceability-requests/SRQ-CC-13043135/
```

**Response**

Status: 200 OK

