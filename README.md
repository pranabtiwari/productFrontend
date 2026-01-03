🛍️ ProdStore

ProdStore is a full-stack product sharing platform where users can upload their own products, showcase them with images and descriptions, and interact through comments.
Authentication is handled with Clerk, data is stored in Neon PostgreSQL, and the backend is powered by Node.js + Express + Drizzle ORM, while the frontend is built with Vite + React.

🌐 Live Website:
👉 https://prodstore.vercel.app/

✨ Features

🔐 Authentication with Clerk

Secure sign up / sign in

User identity synced with database

📦 Product Management

Create products with:

Title

Image URL

Description

View all products

View single product details

Edit & delete your own products

💬 Comments System

Authenticated users can comment on products

Only comment owners can delete their comments

Product owners can manage their content

🧑‍💻 User Sync

Clerk user IDs are synced to the database

Ensures ownership and permissions across products & comments

🧱 Tech Stack
Frontend

Vite

React

React Router

TanStack React Query

Axios

Tailwind CSS / DaisyUI

Clerk (Frontend SDK)

Backend

Node.js

Express

Drizzle ORM

PostgreSQL (Neon)

Clerk (Express Middleware)

Database

Neon PostgreSQL

Drizzle schema & relations

Foreign key constraints with cascading deletes

📁 Repositories

Frontend
👉 https://github.com/pranabtiwari/productFrontend

Backend
👉 https://github.com/pranabtiwari/productBackend (!!! PRIVATE REPOSITORY !!!)



🗄️ Database Models (Simplified)
Users

id (Clerk user ID)

email

name

imageUrl

Products

id

title

description

imageUrl

userId (FK → users)

Comments

id

content

userId (FK → users)

productId (FK → products)

🔒 Authorization Rules

Only authenticated users can:

Create products

Comment on products

Users can only:

Edit/delete their own products

Delete their own comments

Ownership is verified using Clerk userId

🚀 Running Locally
1️⃣ Clone repositories
git clone https://github.com/pranabtiwari/productFrontend
git clone https://github.com/pranabtiwari/productBackend (!!! PRIVATE REPOSITORY !!!)

2️⃣ Backend setup
cd productBackend
npm install


Create .env file:

PORT=3000
DATABASE_URL=your_neon_database_url
CLERK_SECRET_KEY=your_clerk_secret_key
FRONTEND_URL=http://localhost:5173


Run backend:

npm start

3️⃣ Frontend setup
cd productFrontend
npm install


Create .env file:

VITE_API_URL=http://localhost:3000/api
VITE_CLERK_PUBLISHABLE_KEY=your_clerk_publishable_key


Run frontend:

npm run dev

🌍 Deployment

Frontend → Vercel

Backend → Render

Database → Neon PostgreSQL

SPA routing is handled using Vercel rewrites to support page refresh and direct links.



👨‍💻 Author

Pranab Tiwari
Full-Stack Developer
GitHub: https://github.com/pranabtiwari

⭐️ Support

If you found this project helpful, consider giving it a ⭐ on GitHub!
