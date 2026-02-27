You’re targeting backend roles (Node + Express + MongoDB), so here are the most frequently asked MERN backend machine test tasks — based on real hiring patterns for freshers (0–1 I’ll focus only on the important 20% that covers 80% of tests.

🔥 1. Authentication System (VERY COMMON – 90% chance)
Task:

Build REST APIs for:

Register user

Login user

JWT authentication

Protected route

Concepts Tested:

Express routing

MongoDB schema

Password hashing (bcrypt)

JWT token generation

Middleware

APIs Expected:
POST /api/auth/register
POST /api/auth/login
GET  /api/user/profile (protected)
Must Know:

Hash password before saving

Compare password using bcrypt

Use JWT in headers

Authorization: Bearer token
🔥 2. CRUD APIs (ALMOST ALWAYS ASKED)
Task:

Build CRUD APIs for:

Products

Books

Users

Tasks (Todo app)

Example:
POST   /api/products
GET    /api/products
GET    /api/products/:id
PUT    /api/products/:id
DELETE /api/products/:id
Concepts Tested:

Mongoose schema

Controllers

Error handling

Status codes (200, 201, 400, 404, 500)

🔥 3. Pagination + Search (Very Common in Pune)
Task:

Add:

Pagination

Search by name

Sorting

Example:
GET /api/products?page=1&limit=10&search=mobile&sort=price
Concepts Tested:
.skip()
.limit()
.sort()
.regex search

If you know this → You are ahead of 70% freshers.

🔥 4. Role-Based Authorization (Medium Level)
Task:

Admin can:

Delete users

Create products

User can:

View products

Concepts Tested:

Middleware

Role check

if (req.user.role !== "admin") {
   return res.status(403)
}
🔥 5. File Upload (Very Frequently Asked Now)
Task:

Upload profile image

Upload product image

Concepts Tested:

multer

Store in:

local folder

Cloudinary (bonus)

🔥 6. Build Simple E-Commerce Backend (Common Assignment)

Features:

Register/Login

Add product

Add to cart

Create order

Concepts:

Reference relationships

user: { type: mongoose.Schema.Types.ObjectId, ref: "User" }

Populate

.populate("user")
🔥 7. API Validation (Important)

Use:

express-validator
OR

Manual validation

Example:

if (!email || !password) {
   return res.status(400).json({ message: "All fields required" })
}
🔥 8. Error Handling Middleware (Advanced but Impressive)
app.use((err, req, res, next) => {
   res.status(500).json({ message: err.message })
})
⚡ 9. Connect to MongoDB Properly

They check if you:

Use .env

Handle connection errors

Use async/await properly

🎯 10. Folder Structure (Very Important in Machine Test)

Expected structure:

/config
/controllers
/models
/routes
/middleware
/server.js

If you code everything in one file → ❌ bad impression.

💎 BONUS (Sometimes Asked)

Rate limiter

Refresh token

Forgot password

Email sending

Swagger documentation

🧠 What Companies Actually Evaluate
Skill	What They Check
Clean Code	Separation of logic
Async/Await	No callback mess
Proper status codes	Professional API
Error handling	No crash
Security basics	Hashing + JWT
🚀 For You (Important – Based on Your Profile)

Since:

You already know MERN

You worked 9 months at eClerx

You’re comfortable with frontend

👉 Focus more on:

Authentication

MongoDB relations

Pagination

Clean architecture

