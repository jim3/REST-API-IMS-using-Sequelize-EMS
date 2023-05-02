## RESTful API Inventory App for Fasteners :: ESM Edition

### Description

**NOTE**: This is the *exact* same repo as this project: [REST-API-IMS-using-Sequelize](https://github.com/jim3/REST-API-IMS-using-Sequelize). The only difference is that this repo uses the ECMAScript "ESM" module system. I wanted to experiment and see the differences and also decide if new projects should get the ESM treatment or not. I'll probably end up deleting this repo in the future but leaving as reference for now...

A RESTful API for an inventory management application for parts (fasteners). Express.js handles the routing and server-side logic. Sequelize ORM is used to interact with a SQLite3 database. 
The focus of the project is to learn more about how to build RESTful API's. There is a front-end to simply demonstrate how the API works. Things I plan to implement in 
the future are listed at the bottom of the README.


### Features

-   Create, Read, Update and Delete parts (CRUD)

### Tech Stack

-   Node.js
-   Express
-   Sequelize ORM
-   SQLite3

---

[Demo](https://jimmy3.xyz) expect → `502`'s

---

### API Endpoints for Parts

| Method | Endpoint       | Description    |
| ------ | -------------- | -------------- |
| GET    | /api/parts     | Read all parts |
| GET    | /api/parts/:id | Read one part  |
| POST   | /api/parts     | Create a part  |
| PUT    | /api/parts/:id | Update a part  |
| DELETE | /api/parts/:id | Delete a part  |

---

### API Endpoints for Accounts

| Method | Endpoint          | Description       |
| ------ | ----------------- | ----------------- |
| GET    | /api/accounts     | Read all accounts |
| GET    | /api/accounts/:id | Read one account  |
| POST   | /api/accounts     | Create an account |
| PUT    | /api/accounts/:id | Update an account |
| DELETE | /api/accounts/:id | Delete an account |

---

#### Installation

-   git clone `${repo}`
-   Run `npm install`
-   Run `node index.js`
-   Navigate to `${localhost}${port}` in your browser for the front-end app
-   Navigate to `${localhost}${port}/api/parts` in your browser for the API

---

#### Example of API call

`${localhost}/api/parts` | `https://jimmy3.xyz/api/parts`

#### Example of API response

```json
[
  {
    "id": 1,
    "partName": "nuts",
    "partType": "hex",
    "quantity": 5,
    "price": 0.09,
    "createdAt": "2023-04-15T11:04:14.575Z",
    "updatedAt": "2023-04-15T11:04:14.575Z"
  },
  {
    "id": 2,
    "partName": "washers",
    "partType": "lock",
    "quantity": 125,
    "price": 0.13,
    "createdAt": "2023-04-15T12:50:02.098Z",
    "updatedAt": "2023-04-15T12:50:02.098Z"
  }
]
```

---

#### Things planned to implement in the future (in no particular order)
-   Add a front-end for the accounts table for Login/Logout functionality with authentication.
-   Search for parts by part type, part name, quantity and price
-   Sort parts by part type, part name, quantity and price
