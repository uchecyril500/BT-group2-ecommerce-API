Project Overview

This is a backend development project for an online store's inventory system. The API support full CRUD operations, allowing an admin to manage products, update stock levels, and potential customers to search for items.

-------Required Features---------

----------Core Resources---------

    1. POST /api/products – Create a new product.
    2. GET /api/products – Return a list of products. Must support:
          Pagination: page and limit (e.g., ?page=1&limit=10).
          Sorting: sort (e.g., ?sort=price for lowest price first).
          Search: name or search (filters products by matching text in name).
    3. GET /api/products/:id – Return a single product by ID.
    4. PUT /api/products/:id – Update a product (e.g., change price or stock).
    5. DELETE /api/products/:id – Remove a product from inventory.
   
--------Data Model (Product)----------
  1. name (String, required, indexed for search)
  2. price (Number, required, min: 0)
  3. description (String, optional)
  4. category (String, required, e.g., "Electronics", "Clothing")
  5. inStock (Boolean, default: true)
  6. createdAt / updatedAt (Timestamps)

-------Shared Technology Stack ---------
   1.  Runtime: Node.js + Express
   2.  Database: MongoDB Atlas (free tier) with Mongoose ODM
   3.  Config: dotenv for environment variables
   4.  Validation: Joi or Mongoose validation logic
   5.  Hosting: Render.com (Web Service)

