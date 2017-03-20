## Serviceability Requests

**Endpoint Summary**

| Action | Endpoint |
| ------ | -------- |
| List all Serviceability Responses | GET /serviceability-responses |
| Create a new Serviceability Response | POST /serviceability-responses |
| Get a single Serviceability Response | GET /serviceability-responses/{id} |
| Update the Serviceability Response by replacing the serviceability attribute with the instance provided | PUT /serviceability-responses/{id} |
| Remove an existing Serviceability Response based on the ID provided in query string | DELETE /serviceability-responses/{id} |
| Cancel a Serviceability Response | POST /serviceability-responses/{id}/cancel |

### List serviceability responses

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
