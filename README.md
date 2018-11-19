# RESTful Web API with Node.js Framework

Build a RESTful API using (Express)[https://expressjs.com] framework that will interface with the private blockchain.

## Getting Started

These instructions will get you a copy of the project up and running on your local machine.

### Prerequisites

Installing Node and NPM is pretty straightforward using the installer package available from the (Node.js® web site)[https://nodejs.org/en/].

### Configuring your project

- Install project dependencies
```
npm install
```
- Run 
```
node app.js
```

### Endpoints

- GET Block
  - http://localhost:8000/block/:index
  - The web API contains a GET endpoint that responds to a request using a URL path with a block height parameter
  - Output
    - The block object with JSON format
    - If there is no block with such index, status code: 404
    - If error occurs while fetching the block, status code: 500
- POST Block
  - http://localhost:8000/block
  - The web API contains a POST endpoint that allows posting a new block with the data payload option to add data to the block body
  - Input
  ```
  {
      "body": "Testing block with test string data"
  }
  ```
  - Output
    - The added block object with JSON format
    - If there is no content on the payload, status code: 500
    - If error occurs while adding the block, status code: 500
