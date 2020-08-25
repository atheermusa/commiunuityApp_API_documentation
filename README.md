# commiunuityApp_API_documentation
We are building a neighbourhood collaboration site and we want to make a system to keep track of people, houses, and addresses of those houses.
   - Each person has a name, age and number of people in their household
   - Each house has an address and an owner
   - Each address has a postcode and street address

The REST API will need to enable users to:
   - Store people, houses and addresses
   - Look up a house, it’s address and owner
   - Look up people in our neighbourhood within certain age brackets and with specific household sizes

***

# Schema 
![Diagram of Schema](https://i.imgur.com/T43PFbs.png)

# HTTP Status Codes

| Staus Code  | Description |
| ------------- | ------------- |
| 200 OK  | The request succeeded.  |
| 201 Created  | A POST method successfully created a resource. If the resource was already created by a previous execution of the same method, for example, the server returns the HTTP 200 OK status code.  |
| 202 Accepted  | The server accepted the request and will execute it later.  |
| 204 No Content  | The server successfully executed the method but returns no response body.  |
| 400 Bad Request  | INVALID_REQUEST. Request is not well-formed, syntactically incorrect, or violates schema.  |
| 401 Unauthorized  | AUTHENTICATION_FAILURE. Authentication failed due to invalid authentication credentials.  |
| 403 Forbidden  | NOT_AUTHORIZED. Authorization failed due to insufficient permissions.  |
| 404 Not Found  | RESOURCE_NOT_FOUND. The specified resource does not exist.  |
| 405 Method Not Allowed  | METHOD_NOT_SUPPORTED. The server does not implement the requested HTTP method.  |
| 415 Unsupported Media Type  | UNSUPPORTED_MEDIA_TYPE. The server does not support the request payload’s media type.  |
| 422 Unprocessable Entity  | UNPROCESSABLE_ENTITY. The API cannot complete the requested action, or the request action is semantically incorrect or fails business validation.  |
| 429 Unprocessable Entity  | RATE_LIMIT_REACHED. Too many requests. Blocked due to rate limiting.  |
| 500 Internal Server Error  | INTERNAL_SERVER_ERROR. An internal server error has occurred.  |
| 503 Service Unavailable  | SERVICE_UNAVAILABLE. Service Unavailable.  |



# Routes

Base url: alexandAtheer/

| Path  | HTTP Verb | Action |
| ------------- | ------------- |------------- |
| /house  | GET  | index |
| /house/new  | GET  |new  |
| /house  | POST  |create  |
| /house/:id  | GET  |show  |
| /house/:id/address  | GET  | show  |
| /house/:id/owner  | GET  | show  |
| /house/:id/edit  | GET  | edit  |
| /house/:id/  | PATCH/PUT  | update  |
| /house/:id  | DELETE  | destroy  |

| Path  | HTTP Verb | Action |
| ------------- | ------------- |------------- |
| /person  | GET  | index |
| /person/new  | GET  |new  |
| /person  | POST  |create  |
| /person/:id  | GET  |show  |
| /person?{queryParameters}  | GET  | show  |
| /person/:id/edit  | GET  | edit  |
| /person/:id/  | PATCH/PUT  | update  |
| /person/:id  | DELETE  | destroy  |



| queryParameters  | type | Description |
| ------------- | ------------- |------------- |
| minAge  | number  | Search by age bracket |
| maxAge  | number  |Search by age bracket  |
| householdSize  | number  |Search by household size  |


# Request & Response - Example

![Request & Response - Eg](https://i.imgur.com/UEXipio.png)



