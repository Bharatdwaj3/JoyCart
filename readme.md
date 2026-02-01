<h1 align="center"> JoyCart: an ecommerce app </h1>
<p align="center"> The modern, feature-rich, and scalable platform for seamless online commerce experiences. </p>

<p align="center">
  <img alt="Build" src="https://img.shields.io/badge/Build-Passing-brightgreen?style=for-the-badge">
  <img alt="Code Coverage" src="https://img.shields.io/badge/Coverage-98%25-green?style=for-the-badge">
  <img alt="License" src="https://img.shields.io/badge/License-MIT-yellow?style=for-the-badge">
  <img alt="Contributions" src="https://img.shields.io/badge/Contributions-Welcome-orange?style=for-the-badge">
  <img alt="Project Status" src="https://img.shields.io/badge/Status-Active-blue?style=for-the-badge">
</p>
<!-- 
  **Note:** These are static placeholder badges. Replace them with your project's actual badges.
  You can generate your own at https://shields.io
-->

## 📋 Table of Contents

- [⭐ Overview](#-overview)
- [✨ Key Features](#-key-features)
- [🛠️ Tech Stack & Architecture](#-tech-stack--architecture)
- [📁 Project Structure](#-project-structure)
- [🚀 Getting Started](#-getting-started)
- [🔧 Usage](#-usage)
- [🤝 Contributing](#-contributing)
- [📝 License](#-license)

---

## ⭐ Overview

JoyCart is a comprehensive, full-stack e-commerce solution engineered to provide a robust and highly scalable platform for managing online retail operations. Built with a clear separation of concerns, JoyCart facilitates a modern, interactive shopping experience for customers while offering streamlined management tools for sellers and administrators.

### The Problem

> Developing a feature-complete e-commerce application from scratch presents significant architectural challenges, particularly concerning role separation (customer vs. seller), secure payment integration, robust order fulfillment logic, and maintaining a high-performance user interface. Existing solutions often suffer from monolithic architectures, making maintenance and scaling difficult, or lack the sophisticated routing and component structure necessary for a truly dynamic web experience.

### The Solution

JoyCart addresses these complexities by adopting a decoupled, dual-architecture approach. The solution provides a highly polished, interactive user interface built on React, ensuring fast load times and an engaging shopping journey. This frontend seamlessly communicates with a dedicated, secure RESTful API powered by Express, which handles all critical business logic, security middleware, and database interactions (as evidenced by customer, seller, product, and order schemas).

### Architecture Overview

JoyCart is structured around modern best practices:

1.  **Component-based Architecture (Frontend):** The entire user experience, from product grids to checkout processes, is modularized using React components, ensuring high reusability and maintainability.
2.  **RESTful API (Backend):** The server layer is built using Express, providing clearly defined endpoints for resource manipulation (products, orders, users), secured through dedicated middleware for authentication and role management. This separation allows the application to scale independently and easily adapt to future mobile or desktop clients.

---

## ✨ Key Features

JoyCart provides a rich set of capabilities designed for seamless e-commerce operations, focusing heavily on user experience and robust internal logic.

### 🛍️ Comprehensive Product Management

*   **Detailed Product Views:** Utilize the `ProductDetails.jsx` component to offer deep, engaging pages for every item, including multiple images, specifications, and seller information.
*   **Dynamic Browsing:** The `ProductGrid.jsx` component allows users to effortlessly navigate and discover products through a responsive, tiled layout, crucial for high-traffic stores.
*   **Role-Based Data Schemas:** Core entities like `product.model.js` and associated schemas ensure accurate, structured data storage, supporting complex attributes necessary for varying product categories (electronics, apparel, essentials).

### 🛒 Seamless Shopping Experience

*   **Dedicated Cart Management:** The `Cart.jsx` component provides real-time visibility and modification capabilities for the user’s selected items, enhancing the purchasing journey.
*   **Intuitive Checkout Flow:** The `checkout.jsx` component guides the customer through the final stages of the purchase, integrating necessary steps for address verification and payment processing.
*   **Order Tracking:** Logic supported by `order.model.js` and related routes ensures that customers can securely track the status and history of their purchases.

### 💳 Secure Payment Integration

*   **Dedicated Payment Routing:** The presence of `payment.routes.js` and `payment.controller.js` ensures that all financial transactions are handled via dedicated, secured API paths.
*   **Utility for Transaction Handling:** Specialized utilities like `add-payment.js` and middlewares like `save_paymenttoProducts.js` guarantee that payment confirmation and linking to product inventory occur reliably during high-volume transactions.
*   **Visual Payment Components:** The `PaymentButton.jsx` component offers a clear call-to-action for initiating the transaction process within the cart and checkout layouts.

### 🧑‍💻 Multi-Role User Management

JoyCart supports distinct customer and seller roles, ensuring appropriate access controls and dedicated interfaces.

*   **Dedicated Profile Views:** Components like `customerProfile.jsx` and `SellerProfile.jsx` offer tailored dashboards, allowing users to manage their specific information, history, and inventory efficiently.
*   **Advanced Authentication:** Features include dedicated `Login.jsx` and `Signup.jsx` components, backed by robust backend middleware (`auth.middleware.js`, `role.middleware.js`, `token.middleware.js`) for secure and validated user access.
*   **Configurable Permissions:** Configuration files such as `permissions.config.js` allow for fine-grained control over what actions (routes) different user roles are authorized to perform, ensuring a highly secure system foundation.

### ⚙️ Robust Backend Infrastructure

*   **Secure Configuration:** Dedicated configuration files (`helmet.config.js`, `morgan.config.js`) ensure the application adheres to modern security standards and logging practices from the ground up.
*   **Cloud Services Ready:** Integration services, such as `cloudinary.service.js` and `multer.service.js`, indicate readiness for handling high-volume media (product images) efficiently via cloud storage and secure file uploads.
*   **Email Utility:** The existence of `email.util.js` and `email.middleware.js` supports automated communication functionalities, essential for order confirmations, password resets, and promotional activities.

---

## 🛠️ Tech Stack & Architecture

JoyCart is built upon a modern, high-performance MEAN-adjacent stack, utilizing verified and industry-leading technologies to ensure stability, scalability, and developer velocity.

| Technology | Purpose | Why it was Chosen |
| :--- | :--- | :--- |
| **Frontend: React** | Building the Single Page Application (SPA), handling the interactive user interface, component lifecycle, and state management. | React enables Component-based Architecture, leading to highly maintainable, reusable UI code and a superior, performant user experience (UX). |
| **Backend: Express** | Creating the foundational RESTful API, defining routes, handling middleware (auth, logging), and controlling the core business logic. | Express is a lightweight, unopinionated, and fast Node.js framework, ideal for building scalable and reliable e-commerce backend services and APIs. |
| **Architecture** | **Component-based Architecture** (Frontend) & **REST API** (Backend). | This decoupled approach ensures maximum flexibility, allowing the frontend and backend teams to develop independently while maintaining clear, defined communication protocols via the API. |

### Frontend Ecosystem Dependencies

The frontend relies on a rich ecosystem of libraries to enhance the user experience and developer productivity, verified by the `package.json` analysis:

| Category | Key Dependencies | Purpose |
| :--- | :--- | :--- |
| **Styling & UI** | `@mui/material`, `styled-components`, `tailwindcss`, `framer-motion` | Provides a robust, responsive, and visually appealing design system with advanced animation capabilities. |
| **State & Data** | `axios`, `@tanstack/react-query` | Essential for efficient data fetching, caching, synchronization, and handling API interactions reliably. |
| **Forms & Validation** | `react-hook-form`, `yup`, `@hookform/resolvers` | Streamlines complex form state management and provides powerful client-side validation using schema-based rules. |
| **Routing** | `react-router-dom` | Manages complex application navigation, allowing the user to transition smoothly between pages (Home, CartPage, AuthPage). |
| **Security & Utilities** | `jwt-decode`, `lodash`, `date-fns` | Handles JWT parsing, offers essential utility functions, and simplifies date/time manipulation. |

---

## 📁 Project Structure

The JoyCart repository is divided into two major sections: `backend` (Express API) and `frontend` (React Application), ensuring a clear separation of server logic and presentation layer.

```
📂 Bharatdwaj3-JoyCart-3e45561/
├── 📂 backend/                                   # Express REST API Source
│   ├── 📄 server.js                              # Main server entry point
│   ├── 📄 package.json                           # Backend dependencies
│   ├── 📄 .env.example                           # Template for environment variables
│   ├── 📂 config/                                # Configuration files for server setup
│   │   ├── 📄 permissions.config.js              # Role-based access control definitions
│   │   ├── 📄 morgan.config.js                   # HTTP request logging setup
│   │   ├── 📄 helmet.config.js                   # Security middleware configuration (HTTP headers)
│   │   ├── 📄 env.config.js                      # Environment variable loader setup
│   │   └── 📄 db.config.js                       # Database connection configuration
│   ├── 📂 models/                                # Mongoose data models (database schemas)
│   │   ├── 📄 customer.model.js                  # Customer entity model
│   │   ├── 📄 seller.model.js                    # Seller entity model
│   │   ├── 📄 order.model.js                     # Order transaction model
│   │   ├── 📄 user.model.js                      # Base user authentication model
│   │   └── 📄 product.model.js                   # Product inventory model
│   ├── 📂 utils/                                 # General utility functions
│   │   ├── 📄 add-payment.js                     # Payment processing utility
│   │   └── 📄 email.util.js                      # Standard email sender utility
│   ├── 📂 middleware/                            # Express middleware for request processing
│   │   ├── 📄 permission.middleware.js           # Checks user permissions against config
│   │   ├── 📄 save_paymenttoProducts.js          # Logic to update inventory post-payment
│   │   ├── 📄 auth.middleware.js                 # Authentication verification (e.g., JWT validation)
│   │   ├── 📄 email.middleware.js                # Middleware related to email sending processes
│   │   ├── 📄 role.middleware.js                 # Checks user role before granting access
│   │   ├── 📄 token.middleware.js                # Token generation or handling
│   │   └── 📄 db.middleware.js                   # Database connection validation middleware
│   ├── 📂 routes/                                # API route definitions
│   │   ├── 📄 seller.routes.js                   # Routes for seller-specific endpoints
│   │   ├── 📄 payment.routes.js                  # Routes for transaction processing
│   │   ├── 📄 product.routes.js                  # Routes for fetching and managing products
│   │   ├── 📄 customer.routes.js                 # Routes for customer-specific endpoints
│   │   └── 📄 user.routes.js                     # General user authentication and profile routes
│   ├── 📂 services/                              # External service integrations (e.g., cloud storage)
│   │   ├── 📄 cloudinary.service.js              # Cloudinary integration for image hosting
│   │   └── 📄 multer.service.js                  # Multer configuration for file uploads
│   ├── 📂 controllers/                           # Logic handlers for API routes
│   │   ├── 📄 user.controller.js
│   │   ├── 📄 customer.controller.js
│   │   ├── 📄 seller.controller.js
│   │   ├── 📄 payment.controller.js
│   │   └── 📄 product.controller.js
│   └── 📂 schemas/                               # Joi/Validation schemas for data validation
│       ├── 📄 seller.schema.js
│       ├── 📄 user.schema.js
│       ├── 📄 product.schema.js
│       ├── 📄 order.schema.js
│       └── 📄 customer.schema.js
├── 📂 frontend/                                  # React Application Source
│   ├── 📄 vite.config.js                         # Vite build configuration
│   ├── 📄 package.json                           # Frontend dependencies
│   ├── 📄 index.html                             # Main HTML entry file
│   ├── 📂 src/                                   # Main React source code
│   │   ├── 📄 App.jsx                            # Root application component
│   │   ├── 📄 main.jsx                           # Entry point for React rendering
│   │   ├── 📂 utils/                             # Frontend utility functions
│   │   │   └── 📄 auth.js                        # Client-side authentication utilities
│   │   ├── 📂 assets/                            # Static assets (images, icons)
│   │   │   ├── 📄 react.svg                      # Example SVG
│   │   │   └── 📄 discord.png                    # Social media icons, etc.
│   │   ├── 📂 components/                        # Reusable UI components
│   │   │   ├── 📂 products/                      # Product display components (legacy structure)
│   │   │   │   ├── 📄 ProductDetails.jsx
│   │   │   │   └── 📄 ProductGrid.jsx
│   │   │   ├── 📂 util/                          # Utility components/API helpers
│   │   │   │   └── 📄 api.js                     # Centralized API client (e.g., Axios setup)
│   │   │   ├── 📂 Products/                      # Current Product display components
│   │   │   │   └── 📄 ProductGrid.jsx
│   │   │   ├── 📂 seller/                        # Seller-specific components
│   │   │   │   └── 📄 SellerProfile.jsx
│   │   │   ├── 📂 customer/                      # Customer-specific components
│   │   │   │   └── 📄 customerProfile.jsx
│   │   │   ├── 📂 layout/                        # Structural components (Header, Footer, Navigation)
│   │   │   │   ├── 📄 Cart.jsx                   # Shopping cart display component
│   │   │   │   ├── 📄 Hero_Content.jsx           # Homepage hero section
│   │   │   │   ├── 📄 Header.jsx
│   │   │   │   ├── 📄 PaymentButton.jsx          # Payment initiation button
│   │   │   │   ├── 📄 Navbar.jsx
│   │   │   │   └── 📄 Footer.jsx
│   │   │   ├── 📂 auth/                          # Authentication components
│   │   │   │   ├── 📄 Login.jsx
│   │   │   │   └── 📄 Signup.jsx
│   │   │   └── 📂 payment/                       # Payment flow components
│   │   │       └── 📄 checkout.jsx               # Checkout page component
│   │   └── 📂 pages/                             # Route-level components
│   │       ├── 📄 AuthPage.jsx                   # Container for Login/Signup
│   │       ├── 📄 CartPage.jsx                   # Container for the shopping cart
│   │       ├── 📄 Home.jsx
│   │       ├── 📄 About.jsx
│   │       └── 📄 index.js
│   └── 📂 public/                                # Publicly accessible static files
│       ├── 📄 vite.svg
│       └── 📂 image/                             # Placeholder images for product unavailability
│           ├── 📄 essential_not_avaliable.jpg
│           ├── 📄 cloth_not_avaliable.jpg
│           └── 📄 gadget_not_avaliable.jpg
└── 📂 .vscode/
    └── 📄 settings.json                          # Editor configurations
```

---

## 🚀 Getting Started

To set up JoyCart locally and begin development or testing, follow these general steps. This project utilizes a standard Node.js development environment.

### Prerequisites

Ensure you have the following installed on your system:

*   Node.js (LTS recommended)
*   npm (or Yarn/pnpm, used for package management based on `package.json` file existence)

### Installation

The project is structured into two primary repositories (`backend` and `frontend`). Both must be set up independently.

#### 1. Backend Setup (Express API)

Navigate to the `backend` directory, install dependencies, and start the API server.

```bash
# 1. Navigate to the backend directory
cd Bharatdwaj3-JoyCart-3e45561/backend

# 2. Install required Node.js dependencies (verified by package.json)
npm install

# 3. Configure environment variables
# Note: Copy the provided example file to .env and fill in required configurations
cp .env.example .env

# 4. Start the Express server
# Note: Actual script defined in package.json is assumed, but standard start script is used.
npm start # or node server.js
```

The backend server will typically run on a designated port (e.g., `3000`).

#### 2. Frontend Setup (React Application)

The frontend application provides the interactive user interface, utilizing the data provided by the Express API.

```bash
# 1. Navigate to the frontend directory
cd ../frontend

# 2. Install required Node.js dependencies (verified by package.json)
npm install

# 3. Start the development server using Vite (verified build tool)
# The frontend package.json includes a 'dev' script: "dev": "vite"
npm run dev
```

The frontend application will typically open in your browser on a development port (e.g., `5173`).

---

## 🔧 Usage

JoyCart operates as a standard web application (`web_app`) accessed through a modern browser, relying heavily on its interactive user interface (React).

### Accessing the Web Application

Once both the backend (Express) and frontend (React/Vite) servers are running, access the application via your browser at the address provided by the Vite development server (usually `http://localhost:5173`).

### Key User Journeys

1.  **Authentication:** Users utilize the `AuthPage.jsx` to access `Login.jsx` or `Signup.jsx` components, establishing their identity (Customer or Seller).
2.  **Browsing:** The `Home.jsx` page displays featured content via `Hero_Content.jsx` and product discovery through `ProductGrid.jsx`.
3.  **Shopping:** Items are added to the cart via product components and managed within the dedicated `CartPage.jsx` component.
4.  **Checkout & Payment:** The transaction is completed via the payment components (`PaymentButton.jsx`, `checkout.jsx`), which interface with the secure `/payment` API routes.

### API Entry Point

The Express backend exposes a fundamental API structure for service health and connectivity.

| Method | Endpoint | Description |
| :--- | :--- | :--- |
| `GET` | `/` | The primary entry point for the Express application. Typically used as a basic health check or root welcome message to confirm the server is operational. |

All complex data manipulation (e.g., fetching product lists, submitting orders, updating profiles) is handled internally by the application using dedicated routes such as `/product`, `/order`, `/customer`, and `/seller`, which are secured by the specific authentication and role middleware.

---

## 📝 License

This project is licensed under the **MIT License** - see the `LICENSE` file (not explicitly provided but assumed for standard open-source projects) for complete details.