### Get and Delete Phones API

#### Task:

Extend an existing Express.js application to retrieve and delete phones from the database.


#### Instructions:

1. **Create a Phone Table using NeonConsole:**

   - Columns:
      - id - primary key, auto-increment
      - name - string
      - type - string
      - year_published - integer

2. **Create a Phone (POST /phones):**

   - Implement a route that allows users to add a new phone
   - If the phone is successfully created:
      - Return it as JSON
   - If not:
      - Return a 500 status with an error message 

3. **Get a Phone by ID (GET /phones/:id):**
   
   - Implement a route that returns a single phone based on its id
   - If the phone exists:
      - Return it as JSON
   - If not:
      - Return a 404 status with an error message

4. **Delete a Phone by ID (DELETE /phones/:id):**

   - Implement a route that deletes a phone based on its id
   - If the phone exists:
      - Delete it from the database
      - Return a confirmation message in JSON
   - If the phone does not exist:
      - Return a 404 status with an error message


3. **Expected Interactions:**

   - **POST /phones:**
      - Send a POST request to /phones
      - Example:
        `POST /phones`

      - Response:
        ```json
        {
           "id": 1,
           "name": "iPhone 13",
           "type": "Apple",
           "year_published": 2021
        }
        ```
   - **GET /phones/:id:**
      - Send a GET request to /phones/:id
      - Example:
        `GET /phones/1`
        
      - Response:
        ```json
        {
           "id": 1,
           "name": "iPhone 13",
           "type": "Apple",
           "year_published": 2021
        }
        ```
   - **DELETE /phones/:id:**
      - Send a DELETE request:
        Example:
        `DELETE /phones/1`

      - Success response:
        ```json
        {
           "message": "Phone deleted successfully"
        }
        ```
      - If not found:
        ```json
        {
           "error": "Phone not found"
        }
        ```
        
4. **Reference:**
   - Creating an Express application: https://expressjs.com/en/5x/api.html 

   - Express Routing: https://www.w3schools.com/nodejs/nodejs_express.asp#BasicRouting 

   - PostgreSQL with Node.js: Connection: https://neon.com/docs/guides/express (node-postgres)

   - PostgreSQL with Node.js: Query: https://marmelab.com/postgres-queries/pool.html 

   - PostgreSQL CREATE Table: https://www.w3schools.com/postgresql/postgresql_create_table.php

   - PostgreSQL SELECT: https://www.w3schools.com/postgresql/postgresql_select.php 

   - PostgreSQL INSERT: https://www.w3schools.com/postgresql/postgresql_insert_into.php 

   - PostgreSQL DELETE: https://www.w3schools.com/postgresql/postgresql_delete.php 

