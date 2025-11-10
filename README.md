🛍 E-Commerce Website
A production-grade full-stack E-Commerce application built with the MERN stack (MongoDB, Express.js, React.js, Node.js). This project demonstrates a complete workflow from frontend to backend to database, featuring modern design, clean code, and comprehensive documentation.

🎯 Features
Product Browsing: Browse and explore products with search and category filtering
Product Details: View detailed product information
Shopping Cart: Add, update, and remove items from cart
Checkout: Mock checkout process (no real payment processing)
Responsive Design: Modern, clean UI that works on all devices
Real-time Cart Updates: Dynamic cart count and total calculation
🛠 Tech Stack
Frontend
React.js - UI library
React Router DOM - Client-side routing
Tailwind CSS - Utility-first CSS framework
Context API - State management for cart
Axios - HTTP client for API calls
Vite - Build tool and dev server
Backend
Node.js - Runtime environment
Express.js - Web framework
MongoDB - NoSQL database
Mongoose - MongoDB object modeling
Express Validator - Input validation
CORS - Cross-origin resource sharing
📁 Project Structure
ecommerce-app/
├── backend/
│   ├── config/
│   │   └── db.js                 # MongoDB connection
│   ├── controllers/
│   │   ├── productController.js  # Product business logic
│   │   └── cartController.js     # Cart business logic
│   ├── models/
│   │   ├── Product.js            # Product schema
│   │   └── Cart.js               # Cart schema
│   ├── routes/
│   │   ├── productRoutes.js      # Product routes
│   │   └── cartRoutes.js         # Cart routes
│   ├── server.js                 # Express server
│   ├── package.json
│   └── .env.example
├── frontend/
│   ├── src/
│   │   ├── components/
│   │   │   ├── Navbar.jsx        # Navigation bar
│   │   │   ├── ProductCard.jsx   # Product card component
│   │   │   └── CartItem.jsx      # Cart item component
│   │   ├── context/
│   │   │   └── CartContext.jsx   # Cart state management
│   │   ├── pages/
│   │   │   ├── Home.jsx          # Product listing page
│   │   │   ├── ProductDetails.jsx # Product detail page
│   │   │   ├── Cart.jsx          # Shopping cart page
│   │   │   └── Checkout.jsx      # Checkout page
│   │   ├── App.jsx               # Main app component
│   │   ├── main.jsx              # React entry point
│   │   └── index.css             # Global styles
│   ├── index.html
│   ├── package.json
│   ├── vite.config.js
│   └── tailwind.config.js
└── README.md
🚀 Setup Instructions
Prerequisites
Node.js (v18 or higher)
MongoDB Atlas account (or local MongoDB instance)
npm or yarn
Backend Setup
Navigate to backend directory

cd backend
Install dependencies

npm install
Create .env file

cp .env.example .env
Configure environment variables

PORT=5000
MONGODB_URI=your_mongodb_atlas_connection_string
NODE_ENV=development
Start the server

npm start
# Or for development with auto-reload
npm run dev
The server will run on http://localhost:5000

Frontend Setup
Navigate to frontend directory

cd frontend
Install dependencies

npm install
Create .env file (optional)

VITE_API_URL=http://localhost:5000/api
Start the development server

npm run dev
The app will run on http://localhost:3000

🗄 Database Setup
MongoDB Atlas Setup
Create a free account at MongoDB Atlas
Create a new cluster
Create a database user
Whitelist your IP address (or use 0.0.0.0/0 for development)
Get your connection string and add it to backend/.env
Seed Data
To populate the database with sample products, you can use the seed script:

cd backend
node seed.js
Or manually create products using the API:

POST http://localhost:5000/api/products
Content-Type: application/json

{
  "name": "Product Name",
  "description": "Product description",
  "price": 29.99,
  "image": "https://example.com/image.jpg",
  "category": "electronics",
  "stock": 100
}
🔗 API Endpoints
Products
GET /api/products - Get all products
GET /api/products/:id - Get single product
POST /api/products - Create new product (admin)
Cart
GET /api/cart - Get cart items
POST /api/cart - Add item to cart
DELETE /api/cart/:id - Remove item from cart
PUT /api/cart/:id - Update cart item quantity
Health Check
GET /api/health - Server health check
🎨 UI/UX Features
Modern Design: Clean, professional interface
Responsive Layout: Works on desktop, tablet, and mobile
Interactive Elements: Hover effects, transitions, and animations
Cart Badge: Dynamic cart count in navbar
Search & Filter: Search products and filter by category
Product Images: Image handling with fallback placeholders
Form Validation: Client-side validation for checkout
📦 Deployment
Frontend Deployment (Vercel)
Push your code to GitHub
Import project in Vercel
Set build command: npm run build
Set output directory: dist
Add environment variable: VITE_API_URL=your_backend_url
Backend Deployment (Render)
Push your code to GitHub
Create a new Web Service in Render
Connect your repository
Set build command: npm install
Set start command: npm start
Add environment variables:
MONGODB_URI
PORT
NODE_ENV=production
Database (MongoDB Atlas)
Already cloud-hosted
Ensure IP whitelist includes Render's IPs
Update connection string in production environment
🧪 Testing
Manual Testing
Product Browsing

Navigate to home page
Search for products
Filter by category
Click on product to view details
Cart Functionality

Add products to cart
Update quantities
Remove items
Verify cart total
Checkout

Fill out shipping information
Submit order (mock)
Verify cart is cleared
📝 Environment Variables
Backend (.env)
PORT=5000
MONGODB_URI=mongodb+srv://username:password@cluster.mongodb.net/ecommerce
NODE_ENV=development
Frontend (.env)
VITE_API_URL=http://localhost:5000/api
🐛 Troubleshooting
Common Issues
MongoDB Connection Error

Verify MongoDB Atlas connection string
Check IP whitelist settings
Ensure database user has proper permissions
CORS Error

Verify CORS is enabled in backend
Check API URL in frontend environment variables
Port Already in Use

Change PORT in backend/.env
Update VITE_API_URL in frontend/.env
📚 Additional Resources
React Documentation
Express.js Documentation
MongoDB Atlas Documentation
Tailwind CSS Documentation
Vite Documentation
👤 Author
Built for internship evaluation demonstration.

📄 License
This project is open source and available under the MIT License.
