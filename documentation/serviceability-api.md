## Serviceability

Serviceability provides an API, schemas, and sample apps (reference implementations) to help determine if a particular service is available (or could be made available) via a particular medium (e.g. Fiber, HFC) at a particular location. But it doesn't stop there: serviceability also provides fluid transitions to the quoting and site survey processes.

The Endpoint Summary table describes each Serviceability API endpoint. Following the table is an example of each action at each endpoint, including sample request and response payloads.


**Endpoint Summary**

| Action | Endpoint |
| ------ | -------- |
| List all Serviceability Requests | GET /serviceability-requests |
| Create a new Serviceability Request | POST /serviceability-requests |
| Get a single Serviceability Request | GET /serviceability-requests/{id} |
| Update the Serviceability Request by replacing the serviceability attribute with the instance provided | PUT /serviceability-requests/{id} |
| Remove an existing Serviceability Request based on the ID provided in query string | DELETE /serviceability-requests/{id} |
| Submit a Serviceability Request | POST /serviceability-requests/{id}/submit |
| Cancel a Serviceability Request | POST /serviceability-requests/{id}/cancel |
| List all Serviceability Responses | GET /serviceability-responses |
| Create a new Serviceability Response | POST /serviceability-responses |
| Get a single Serviceability Response | GET /serviceability-responses/{id} |
| Update the Serviceability Response by replacing the serviceability attribute with the instance provided | PUT /serviceability-responses/{id} |
| Remove an existing Serviceability Response based on the ID provided in query string | DELETE /serviceability-responses/{id} |
| Submit a Serviceability Response | POST /serviceability-responses/{id}/submit |
| Cancel a Serviceability Response | POST /serviceability-responses/{id}/cancel |
| Accepts a serviceability response/pricing term | POST /serviceability-responses/{id}/accept/{term} |
| Unaccepts a serviceability response/pricing term | POST /serviceability-responses/{id}/unaccept/{term} |


**Endpoint Descriptions and Examples**

### List all Serviceability Requests

```
GET /serviceability-requests
```
Retrieve all Serviceability Requests.

**Response**

Status: 200 OK
``` JSON
{
}
```
