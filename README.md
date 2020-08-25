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
![Diagram of Schema](https://i.imgur.com/m6Mo6E4.png)

# Routes

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
| /person?{q}  | GET  | show  |
| /person/:id/edit  | GET  | edit  |
| /person/:id/  | PATCH/PUT  | update  |
| /person/:id  | DELETE  | destroy  |


| q  | type | Description |
| ------------- | ------------- |------------- |
| minAge  | number  | Search by age bracket |
| maxAge  | number  |Search by age bracket  |
| householdSize  | number  |Search by household size  |


