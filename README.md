<div align="center">

# 🍕 CraveDash

### *Your Cravings, Delivered Fast* ⚡

[![Made with React](https://img.shields.io/badge/React-18.0-61DAFB?style=flat-square&logo=react)](https://reactjs.org/)
[![Spring Boot](https://img.shields.io/badge/Spring%20Boot-3.4.3-6DB33F?style=flat-square&logo=spring)](https://spring.io/projects/spring-boot)
[![MongoDB](https://img.shields.io/badge/MongoDB-5.0-47A248?style=flat-square&logo=mongodb)](https://www.mongodb.com/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=flat-square)](https://opensource.org/licenses/MIT)

**A modern, full-stack food delivery platform built with React, Spring Boot, and MongoDB**

[Features](#-features) • [Tech Stack](#-tech-stack) • [Getting Started](#-getting-started) • [API Docs](#-api-documentation) • [Contributing](#-contributing)

---

</div>

## 📖 About

**CraveDash** is a comprehensive online food delivery solution that brings restaurants and customers together. Built with modern web technologies, it provides a seamless experience for browsing menus, placing orders, processing payments, and managing deliveries in real-time.

### 🎯 Key Highlights

- 🚀 **Fast & Responsive** - Lightning-fast React frontend with Vite
- 🔒 **Secure** - JWT authentication and Spring Security
- 💳 **Payment Ready** - Integrated Razorpay payment gateway
- ☁️ **Cloud-Powered** - AWS S3 for scalable image storage
- 📱 **Mobile-First** - Fully responsive across all devices
- 🎨 **Modern UI** - Clean, intuitive interface with Bootstrap 5

---

## ✨ Features

### � For Customers

| Feature | Description |
|---------|-------------|
| 🔍 **Smart Search** | Quickly find your favorite dishes with intelligent search |
| 🛒 **Cart Management** | Easy add/remove items with real-time cart updates |
| 👤 **User Accounts** | Secure registration and login with JWT tokens |
| 💳 **Secure Payments** | Multiple payment options via Razorpay integration |
| 📦 **Order Tracking** | Real-time order status updates and history |
| 📱 **Responsive Design** | Seamless experience on desktop, tablet, and mobile |
| ⭐ **Reviews & Ratings** | Share your dining experience with the community |

### 🎛️ For Administrators

| Feature | Description |
|---------|-------------|
| ➕ **Menu Management** | Add, edit, and remove food items with ease |
| 📊 **Order Dashboard** | View and manage all orders in real-time |
| 📈 **Analytics** | Track sales, popular items, and customer insights |
| 👥 **User Management** | Manage customer accounts and permissions |
| 🖼️ **Image Upload** | Direct AWS S3 integration for food images |
| 🔔 **Real-time Alerts** | Instant notifications for new orders |

---

## 🏗️ System Architecture

```
┌─────────────────────────────────────────────────────────────┐
│                      Client Layer                            │
│  ┌──────────────────┐         ┌──────────────────┐          │
│  │  Customer Portal │         │  Admin Dashboard │          │
│  │   (React + Vite) │         │   (React + Vite) │          │
│  └────────┬─────────┘         └────────┬─────────┘          │
└───────────┼────────────────────────────┼────────────────────┘
            │                             │
            └──────────────┬──────────────┘
                           │
┌──────────────────────────▼─────────────────────────────────┐
│                   Application Layer                         │
│              ┌─────────────────────────┐                    │
│              │   REST API (Spring Boot) │                   │
│              │   - Spring Security      │                   │
│              │   - JWT Authentication   │                   │
│              └───────────┬──────────────┘                   │
└──────────────────────────┼────────────────────────────────-┘
                           │
        ┌──────────────────┼──────────────────┐
        │                  │                  │
┌───────▼────────┐  ┌──────▼──────┐  ┌───────▼────────┐
│   MongoDB      │  │   AWS S3    │  │   Razorpay     │
│  (Database)    │  │  (Storage)  │  │  (Payments)    │
└────────────────┘  └─────────────┘  └────────────────┘
```

---

## 🛠️ Tech Stack

<table>
<tr>
<td width="50%" valign="top">

### Frontend 🎨

- **React 18** - UI library for building interactive interfaces
- **Vite** - Next-generation frontend build tool
- **Bootstrap 5** - Modern CSS framework
- **React Router v6** - Client-side routing
- **Axios** - HTTP client for API calls
- **React Toastify** - Beautiful toast notifications
- **Context API** - Global state management

</td>
<td width="50%" valign="top">

### Backend ⚙️

- **Spring Boot 3.4.3** - Enterprise Java framework
- **Spring Security** - Authentication & authorization
- **Spring Data MongoDB** - Database integration
- **JWT (JSON Web Tokens)** - Stateless authentication
- **Maven** - Build automation and dependency management
- **Lombok** - Reduce boilerplate code

</td>
</tr>
<tr>
<td width="50%" valign="top">

### Database & Cloud ☁️

- **MongoDB** - NoSQL document database
- **AWS S3** - Cloud object storage
- **Razorpay** - Payment gateway integration

</td>
<td width="50%" valign="top">

### Development Tools 🔧

- **Java 21** - Latest LTS Java version
- **Node.js 18+** - JavaScript runtime
- **npm** - Node package manager
- **Git** - Version control system

</td>
</tr>
</table>

---

## 🚀 Getting Started

### Prerequisites

Ensure you have the following installed on your system:

```bash
✅ Java 21 or higher
✅ Node.js 18+ and npm
✅ MongoDB 5+ (local or cloud instance)
✅ Git
✅ AWS Account (optional for development)
✅ Razorpay Account (optional for development)
```

### Installation Steps

#### 1️⃣ Clone the Repository

```bash
git clone https://github.com/Shobhits1/CraveDash.git
cd CraveDash
```

#### 2️⃣ Backend Setup (Spring Boot API)

Navigate to the backend directory:

```bash
cd foodiesapi
```

Create `application.properties` in `src/main/resources/`:

```properties
# Server Configuration
server.port=8080

# MongoDB Configuration
spring.data.mongodb.uri=mongodb://localhost:27017/cravedash
spring.data.mongodb.database=cravedash

# AWS S3 Configuration
aws.access.key=YOUR_AWS_ACCESS_KEY
aws.secret.key=YOUR_AWS_SECRET_KEY
aws.region=us-east-1
aws.s3.bucketname=cravedash-images

# JWT Configuration
jwt.secret.key=your-super-secret-jwt-key-at-least-32-characters-long
jwt.expiration=86400000

# Razorpay Configuration
razorpay.key.id=YOUR_RAZORPAY_KEY_ID
razorpay.key.secret=YOUR_RAZORPAY_KEY_SECRET

# File Upload Configuration
spring.servlet.multipart.max-file-size=10MB
spring.servlet.multipart.max-request-size=10MB
```

Start the backend server:

```bash
# For Windows
mvnw.cmd spring-boot:run

# For macOS/Linux
./mvnw spring-boot:run
```

Backend will run on: `http://localhost:8080`

#### 3️⃣ Customer Frontend Setup

Open a new terminal and navigate to the customer frontend:

```bash
cd foodies
npm install
npm run dev
```

Customer portal will run on: `http://localhost:5173`

#### 4️⃣ Admin Panel Setup

Open another terminal and navigate to the admin panel:

```bash
cd adminpanel
npm install
npm run dev
```

Admin panel will run on: `http://localhost:5174`

---

## 📁 Project Structure

```
CraveDash/
│
├── 📂 foodies/                          # Customer Frontend Application
│   ├── 📂 public/                       # Static assets
│   ├── 📂 src/
│   │   ├── 📂 assets/                   # Images, fonts, icons
│   │   ├── 📂 components/               # Reusable React components
│   │   │   ├── Navbar.jsx
│   │   │   ├── FoodCard.jsx
│   │   │   ├── Cart.jsx
│   │   │   ├── Footer.jsx
│   │   │   └── ...
│   │   ├── 📂 context/                  # React Context providers
│   │   │   └── StoreContext.jsx
│   │   ├── 📂 pages/                    # Page components
│   │   │   ├── Home.jsx
│   │   │   ├── Menu.jsx
│   │   │   ├── Cart.jsx
│   │   │   ├── Orders.jsx
│   │   │   └── ...
│   │   ├── 📂 services/                 # API integration services
│   │   │   └── api.js
│   │   ├── 📂 utils/                    # Utility functions
│   │   ├── App.jsx                      # Main app component
│   │   └── main.jsx                     # Entry point
│   ├── package.json
│   ├── vite.config.js
│   └── .env
│
├── 📂 adminpanel/                       # Admin Dashboard Application
│   ├── 📂 public/
│   ├── 📂 src/
│   │   ├── 📂 assets/
│   │   ├── 📂 components/               # Admin components
│   │   │   ├── Sidebar.jsx
│   │   │   ├── AddFood.jsx
│   │   │   ├── OrderList.jsx
│   │   │   └── ...
│   │   ├── 📂 pages/                    # Admin pages
│   │   │   ├── Dashboard.jsx
│   │   │   ├── FoodManagement.jsx
│   │   │   ├── OrderManagement.jsx
│   │   │   └── ...
│   │   ├── 📂 services/                 # API services
│   │   ├── App.jsx
│   │   └── main.jsx
│   ├── package.json
│   ├── vite.config.js
│   └── .env
│
├── 📂 foodiesapi/                       # Spring Boot Backend
│   ├── 📂 src/
│   │   ├── 📂 main/
│   │   │   ├── 📂 java/in/bushansirgur/foodiesapi/
│   │   │   │   ├── 📂 config/          # Configuration classes
│   │   │   │   │   ├── SecurityConfig.java
│   │   │   │   │   ├── CorsConfig.java
│   │   │   │   │   ├── AwsConfig.java
│   │   │   │   │   └── JwtConfig.java
│   │   │   │   ├── 📂 controller/      # REST API controllers
│   │   │   │   │   ├── AuthController.java
│   │   │   │   │   ├── FoodController.java
│   │   │   │   │   ├── OrderController.java
│   │   │   │   │   ├── CartController.java
│   │   │   │   │   └── PaymentController.java
│   │   │   │   ├── 📂 entity/          # MongoDB entities/models
│   │   │   │   │   ├── User.java
│   │   │   │   │   ├── Food.java
│   │   │   │   │   ├── Order.java
│   │   │   │   │   ├── Cart.java
│   │   │   │   │   └── Payment.java
│   │   │   │   ├── 📂 repository/      # Data access layer
│   │   │   │   │   ├── UserRepository.java
│   │   │   │   │   ├── FoodRepository.java
│   │   │   │   │   ├── OrderRepository.java
│   │   │   │   │   └── CartRepository.java
│   │   │   │   ├── 📂 service/         # Business logic layer
│   │   │   │   │   ├── AuthService.java
│   │   │   │   │   ├── FoodService.java
│   │   │   │   │   ├── OrderService.java
│   │   │   │   │   ├── S3Service.java
│   │   │   │   │   └── PaymentService.java
│   │   │   │   ├── 📂 dto/             # Data Transfer Objects
│   │   │   │   ├── 📂 exception/       # Custom exceptions
│   │   │   │   ├── 📂 security/        # Security utilities
│   │   │   │   │   └── JwtUtil.java
│   │   │   │   └── FoodiesApiApplication.java
│   │   │   └── 📂 resources/
│   │   │       ├── application.properties
│   │   │       └── application-dev.properties
│   │   └── 📂 test/                    # Unit & integration tests
│   ├── pom.xml                         # Maven dependencies
│   ├── mvnw                            # Maven wrapper (Unix)
│   └── mvnw.cmd                        # Maven wrapper (Windows)
│
├── 📂 food images/                      # Sample food images
├── .gitignore
├── LICENSE
└── README.md
```

---

## 🔌 API Documentation

### Base URL
```
http://localhost:8080/api
```

### Authentication Endpoints

| Method | Endpoint | Description | Auth Required |
|--------|----------|-------------|---------------|
| `POST` | `/auth/register` | Register a new user | ❌ |
| `POST` | `/auth/login` | User login | ❌ |
| `GET` | `/auth/profile` | Get current user profile | ✅ |
| `PUT` | `/auth/profile` | Update user profile | ✅ |

**Request Example (Register):**
```json
{
  "name": "Shobhit Singh",
  "email": "shobhit@example.com",
  "password": "securePassword123",
  "phone": "+91-9876543210"
}
```

**Response Example:**
```json
{
  "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9...",
  "user": {
    "id": "507f1f77bcf86cd799439011",
    "name": "Shobhit Singh",
    "email": "shobhit@example.com"
  }
}
```

---

### Food Management Endpoints

| Method | Endpoint | Description | Auth Required |
|--------|----------|-------------|---------------|
| `GET` | `/foods` | Get all food items | ❌ |
| `GET` | `/foods/{id}` | Get food item by ID | ❌ |
| `GET` | `/foods/category/{category}` | Get foods by category | ❌ |
| `POST` | `/foods` | Add new food item | ✅ Admin |
| `PUT` | `/foods/{id}` | Update food item | ✅ Admin |
| `DELETE` | `/foods/{id}` | Delete food item | ✅ Admin |

**Request Example (Add Food):**
```json
{
  "name": "Margherita Pizza",
  "description": "Classic pizza with tomato sauce and mozzarella",
  "price": 299.99,
  "category": "Pizza",
  "image": "pizza-margherita.jpg",
  "available": true
}
```

---

### Cart Endpoints

| Method | Endpoint | Description | Auth Required |
|--------|----------|-------------|---------------|
| `GET` | `/cart` | Get user's cart | ✅ |
| `POST` | `/cart/add` | Add item to cart | ✅ |
| `PUT` | `/cart/update/{foodId}` | Update cart item quantity | ✅ |
| `DELETE` | `/cart/remove/{foodId}` | Remove item from cart | ✅ |
| `DELETE` | `/cart/clear` | Clear entire cart | ✅ |

---

### Order Endpoints

| Method | Endpoint | Description | Auth Required |
|--------|----------|-------------|---------------|
| `POST` | `/orders` | Create new order | ✅ |
| `GET` | `/orders/user` | Get user's orders | ✅ |
| `GET` | `/orders/{id}` | Get order by ID | ✅ |
| `GET` | `/orders/all` | Get all orders | ✅ Admin |
| `PUT` | `/orders/{id}/status` | Update order status | ✅ Admin |
| `DELETE` | `/orders/{id}` | Cancel order | ✅ |

**Order Status Values:**
- `PENDING` - Order placed, awaiting confirmation
- `CONFIRMED` - Order confirmed by restaurant
- `PREPARING` - Food is being prepared
- `OUT_FOR_DELIVERY` - Order is on the way
- `DELIVERED` - Order delivered successfully
- `CANCELLED` - Order cancelled

---

### Payment Endpoints

| Method | Endpoint | Description | Auth Required |
|--------|----------|-------------|---------------|
| `POST` | `/payment/create` | Create Razorpay order | ✅ |
| `POST` | `/payment/verify` | Verify payment signature | ✅ |

---

## 🔐 Environment Configuration

### Backend Environment Variables

Create `application.properties` in `foodiesapi/src/main/resources/`:

```properties
# Server Configuration
server.port=8080
server.servlet.context-path=/api

# MongoDB Configuration
spring.data.mongodb.uri=mongodb://localhost:27017/cravedash
spring.data.mongodb.database=cravedash

# AWS S3 Configuration
aws.access.key=YOUR_AWS_ACCESS_KEY_ID
aws.secret.key=YOUR_AWS_SECRET_ACCESS_KEY
aws.region=us-east-1
aws.s3.bucketname=cravedash-food-images

# JWT Configuration
jwt.secret.key=your-very-secure-secret-key-at-least-32-characters-long-for-production
jwt.expiration=86400000
jwt.refresh.expiration=604800000

# Razorpay Configuration
razorpay.key.id=rzp_test_YOUR_KEY_ID
razorpay.key.secret=YOUR_RAZORPAY_SECRET

# File Upload Configuration
spring.servlet.multipart.max-file-size=10MB
spring.servlet.multipart.max-request-size=10MB
spring.servlet.multipart.enabled=true

# Logging
logging.level.in.bushansirgur.foodiesapi=DEBUG
```

### Frontend Environment Variables

Create `.env` in both `foodies/` and `adminpanel/` directories:

```env
VITE_API_URL=http://localhost:8080/api
VITE_RAZORPAY_KEY_ID=rzp_test_YOUR_KEY_ID
VITE_APP_NAME=CraveDash
```

---

## 🧪 Testing

### Run Backend Tests

```bash
cd foodiesapi
./mvnw test
```

### Run Frontend Tests

```bash
# Customer Portal
cd foodies
npm test

# Admin Panel
cd adminpanel
npm test
```

### Run All Tests

```bash
# Backend
cd foodiesapi && ./mvnw clean test

# Frontend
cd foodies && npm test && cd ../adminpanel && npm test
```

---

## 📦 Production Build

### Build Backend

```bash
cd foodiesapi
./mvnw clean package

# Run the JAR file
java -jar target/foodiesapi-0.0.1-SNAPSHOT.jar
```

### Build Frontend Applications

```bash
# Customer Portal
cd foodies
npm run build
# Output: dist/

# Admin Panel
cd adminpanel
npm run build
# Output: dist/
```

### Deployment Options

- **Frontend:** Vercel, Netlify, AWS S3 + CloudFront
- **Backend:** AWS EC2, Heroku, Railway, DigitalOcean
- **Database:** MongoDB Atlas (Cloud)
- **Storage:** AWS S3
- **Payment:** Razorpay Production Keys

---

## 🤝 Contributing

Contributions are what make the open-source community such an amazing place! Any contributions you make are **greatly appreciated**. 🙏

### How to Contribute

1. **Fork** the project
2. **Clone** your fork
   ```bash
   git clone https://github.com/your-username/CraveDash.git
   ```
3. Create a **feature branch**
   ```bash
   git checkout -b feature/AmazingFeature
   ```
4. **Commit** your changes
   ```bash
   git commit -m 'Add some AmazingFeature'
   ```
5. **Push** to the branch
   ```bash
   git push origin feature/AmazingFeature
   ```
6. Open a **Pull Request**

### Contribution Guidelines

- ✅ Follow existing code style and conventions
- ✅ Write clear, descriptive commit messages
- ✅ Add tests for new features
- ✅ Update documentation as needed
- ✅ Ensure all tests pass before submitting PR
- ✅ Keep PRs focused on a single feature or fix
- ✅ Be respectful and constructive in discussions

---

## 🐛 Issues & Feature Requests

Found a bug or have a feature idea? Please [open an issue](https://github.com/Shobhits1/CraveDash/issues) on GitHub.

**When reporting bugs, please include:**
- 📝 Clear description of the issue
- 🔄 Steps to reproduce
- 💻 Expected vs actual behavior
- 🖼️ Screenshots (if applicable)
- 🌐 Browser/OS information
- 📋 Error logs or stack traces

---

## 📄 License

This project is licensed under the **MIT License**.

```
MIT License

Copyright (c) 2024-2026 Shobhit Singh

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

See [LICENSE](LICENSE) file for more details.

---

## 👨‍💻 Author

<div align="center">

### **Shobhit Singh**

Full Stack Developer | Java & React Enthusiast | Open Source Contributor

[![GitHub](https://img.shields.io/badge/GitHub-Shobhits1-181717?style=for-the-badge&logo=github)](https://github.com/Shobhits1)
[![Email](https://img.shields.io/badge/Email-Contact-D14836?style=for-the-badge&logo=gmail)](mailto:shobhit@example.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0077B5?style=for-the-badge&logo=linkedin)](https://linkedin.com/in/shobhitsingh)
[![Portfolio](https://img.shields.io/badge/Portfolio-Visit-FF5722?style=for-the-badge&logo=google-chrome)](https://shobhitsingh.dev)

</div>

---

## 🌟 Show Your Support

If you found this project helpful or learned something from it, please consider giving it a ⭐ **star** on GitHub!

<div align="center">

[![GitHub stars](https://img.shields.io/github/stars/Shobhits1/CraveDash?style=social)](https://github.com/Shobhits1/CraveDash/stargazers)
[![GitHub forks](https://img.shields.io/github/forks/Shobhits1/CraveDash?style=social)](https://github.com/Shobhits1/CraveDash/network/members)
[![GitHub watchers](https://img.shields.io/github/watchers/Shobhits1/CraveDash?style=social)](https://github.com/Shobhits1/CraveDash/watchers)

</div>

---

## 📊 Project Statistics

<div align="center">

![GitHub repo size](https://img.shields.io/github/repo-size/Shobhits1/CraveDash?style=flat-square)
![GitHub code size](https://img.shields.io/github/languages/code-size/Shobhits1/CraveDash?style=flat-square)
![GitHub language count](https://img.shields.io/github/languages/count/Shobhits1/CraveDash?style=flat-square)
![GitHub top language](https://img.shields.io/github/languages/top/Shobhits1/CraveDash?style=flat-square)
![GitHub last commit](https://img.shields.io/github/last-commit/Shobhits1/CraveDash?style=flat-square)
![GitHub commit activity](https://img.shields.io/github/commit-activity/m/Shobhits1/CraveDash?style=flat-square)

</div>

---

## 🙏 Acknowledgments

Special thanks to the amazing open-source community and the following technologies:

- [React](https://reactjs.org/) - A JavaScript library for building user interfaces
- [Spring Boot](https://spring.io/projects/spring-boot) - Java-based framework for building web applications
- [MongoDB](https://www.mongodb.com/) - NoSQL database for modern applications
- [Vite](https://vitejs.dev/) - Next generation frontend tooling
- [Bootstrap](https://getbootstrap.com/) - Popular CSS framework
- [AWS](https://aws.amazon.com/) - Cloud computing services
- [Razorpay](https://razorpay.com/) - Payment gateway solution

---

## 📞 Support

Need help? Feel free to reach out:

- 📧 Email: shobhit@example.com
- 💬 GitHub Issues: [Create an issue](https://github.com/Shobhits1/CraveDash/issues)
- 🐦 Twitter: [@shobhitsingh](https://twitter.com/shobhitsingh)

---

<div align="center">

### 💖 Made with passion and ☕ by Shobhit Singh

**CraveDash** - *Satisfying cravings, one delivery at a time*

🍕 🍔 🍜 🍰 🥗 🍱

[⬆ Back to Top](#-cravedash)

---

**⭐ Star this repo if you find it helpful!**

</div>
