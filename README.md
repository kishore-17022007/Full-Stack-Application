# 🌾 FarmFresh – Full-Stack Marketplace for Farmers & Consumers

**FarmFresh** is a MERN-based e-commerce application that allows farmers to sell fresh products directly to consumers. Customers can follow farmers, browse products, add items to cart, and place orders. Farmers can manage their products, track earnings, and monitor customer interactions.

---

## 🚀 Key Features

### 👨‍🌾 Farmer Features
- Create and manage profile  
- Add, edit, and remove products  
- View earnings and sales analytics  
- Receive consumer comments and ratings  

### 🛒 Consumer Features
- Register and manage profile  
- Follow farmers and explore their produce  
- Add items to cart and checkout  
- Review purchased products and farmers  

### 🔐 System Features
- Secure authentication using JWT  
- Role-based protected routes  
- Product categories, ratings, discounts  
- Order tracking and comments management  

---
## 🛡️ API Documentation

### 🔐 Authentication Routes

| Action | Route | Method |
|--------|-------|--------|
| Login User | `api/v1/auth/login` | POST |
| Check Email Exists | `api/v1/auth/userExists/email/:email` | GET |
| Check Username Exists | `api/v1/auth/userExists/name/:name` | GET |
| Register Farmer | `api/v1/auth/register/farmer` | POST |
| Register Consumer | `api/v1/auth/register/consumer` | POST |
| Get Logged User Info | `api/v1/auth` | GET |

### 👨‍🌾 Farmer Routes

| Action | Route | Method |
|--------|-------|--------|
| Get Farmer Products | `api/v1/farmers/:farmerID/products` | GET |
| Add Comment to Farmer | `api/v1/farmers/:farmerID/comments` | PATCH |
| Get Farmer Profile | `api/v1/farmers/:farmerID` | GET |
| Update Farmer | `api/v1/farmers/` | PATCH |

### 👨 Consumer Routes

| Action | Route | Method |
|--------|-------|--------|
| Get Shopping Cart | `api/v1/consumers/shoppingCart` | GET |
| Follow Farmer | `api/v1/consumers/followFarmer` | PATCH |
| Unfollow Farmer | `api/v1/consumers/unFollowFarmer` | PATCH |
| Get Consumer Profile | `api/v1/consumers/:consumerID` | GET |
| Update Consumer | `api/v1/consumers` | PATCH |

### 🌾 Product Routes

| Action | Route | Method |
|--------|-------|--------|
| Get All Products | `api/v1/products/` | GET |
| Add New Product | `api/v1/products/` | POST |
| Get Top Rated Products | `api/v1/products/topRatedProducts` | GET |
| Get Discounted Products | `api/v1/products/discountedProducts` | GET |
| Get Recent (Last 30 Days) | `api/v1/products/lastThirtyDayProducts/:farmerID` | GET |
| Get Product By ID | `api/v1/products/:productID` | GET |
| Delete Product | `api/v1/products/:productID` | DELETE |
| Update Product | `api/v1/products/:productID` | PATCH |
| Get Products by Category | `api/v1/products/category/:parentCategory` | GET |
| Product Order Detail | `api/v1/products/orderDetail/:productID` | GET |

### 🚚 Order Routes

| Action | Route | Method |
|--------|-------|--------|
| Get User Orders | `api/v1/orders/` | GET |
| Add Order | `api/v1/orders/` | POST |
| Get Orders Needing Review | `api/v1/orders/reviewOrders` | GET |
| Farmer Earnings (Last 30 Days) | `api/v1/orders/getEarningsForLast30Days` | GET |
| Update Order | `api/v1/orders/:orderID` | PATCH |
| Delete Order | `api/v1/orders/:orderID` | DELETE |

### 💬 Comment Routes

| Action | Route | Method |
|--------|-------|--------|
| Farmer Comment Count | `api/v1/comments/farmer/:farmerID/count` | GET |
| Get Farmer Comments | `api/v1/comments/farmer/:farmerID` | GET |
| Product Comment Count | `api/v1/comments/product/:productID/count` | GET |
| Get Product Comments | `api/v1/comments/product/:productID` | GET |

---