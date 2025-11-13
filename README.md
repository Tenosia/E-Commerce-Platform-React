# NextFront - E-Commerce Frontend Application

A modern e-commerce frontend application built with React, TypeScript, and Apollo GraphQL. This application provides a complete shopping experience with product browsing, cart management, checkout flow, and order tracking.

## 🚀 Features

- **Product Catalog**: Browse and view detailed product information
- **Shopping Cart**: Add/remove items, manage quantities
- **User Authentication**: Login functionality with token-based authentication
- **Checkout Flow**: 
  - Address selection and management
  - Order summary and review
- **Order Management**: View and track past orders
- **GraphQL Integration**: Seamless data fetching with Apollo Client
- **Responsive Design**: Built with styled-components for modern UI

## 🛠️ Tech Stack

- **Frontend Framework**: React 16.9.0
- **Language**: TypeScript 3.6.2 (with JavaScript support)
- **GraphQL Client**: Apollo Client 2.6.4
- **Routing**: React Router DOM 5.0.1
- **Styling**: Styled Components 4.3.2
- **Build Tool**: Create React App (react-scripts 3.1.1)
- **State Management**: Apollo Client Cache + Local State
- **Date Handling**: Moment.js 2.24.0
- **UI Components**: rc-input-number

## 📋 Prerequisites

Before you begin, ensure you have the following installed:
- Node.js (v12 or higher recommended)
- Yarn package manager
- A running GraphQL backend server (default: `http://localhost:4000`)

## 🔧 Installation

1. Clone the repository:
```bash
git clone <repository-url>
cd nextFrondEnd
```

2. Install dependencies:
```bash
yarn install
```

## 🏃 Getting Started

1. **Start the development server**:
```bash
yarn start
```

The application will open at `http://localhost:3000` (default React port).

2. **Ensure your GraphQL backend is running**:
   - The app expects a GraphQL API at `http://localhost:4000`
   - Update the URI in `src/App.js` if your backend runs on a different port

3. **Build for production**:
```bash
yarn build
```

## 📁 Project Structure

```
src/
├── apollo/              # Apollo Client configuration
│   ├── gql/            # GraphQL queries and types
│   │   ├── address.js
│   │   ├── orders.tsx
│   │   ├── summary.tsx
│   │   └── types.tsx
│   └── resolvers.js    # Local Apollo resolvers
├── components/          # Reusable React components
│   ├── addressCard.js
│   ├── bill.tsx
│   ├── cartDetail.js
│   ├── header.js
│   ├── loginForm.js
│   ├── order-summary.js
│   ├── orders.tsx
│   ├── productDetail.js
│   └── styledHtml.tsx
├── pages/              # Page components
│   ├── home.js
│   ├── products.js
│   ├── product.js
│   ├── login.js
│   ├── cart.js
│   ├── address.js
│   ├── summary.tsx
│   ├── orders.tsx
│   └── baseLayout.js
├── App.js              # Main app component with routing
├── index.js            # Application entry point
└── index.css           # Global styles
```

## 🗺️ Routes

- `/` - Home page
- `/products` - Product listing page
- `/product/:id` - Individual product detail page
- `/login` - User login page
- `/cart` - Shopping cart page
- `/checkout/address` - Address selection for checkout
- `/checkout/summary` - Order summary and review
- `/orders` - User orders page

## 🔐 Authentication

The application uses token-based authentication:
- Tokens are stored in `localStorage`
- Authentication state is managed through Apollo Client local state
- Protected routes should be implemented based on `isLoggedIn` state

## 🎨 Styling

The project uses `styled-components` for component-level styling. Global styles can be found in `src/index.css`.

## 🧪 Testing

Run tests with:
```bash
yarn test
```

## 📦 Build

Create a production build:
```bash
yarn build
```

The build folder will contain the optimized production-ready files.

## 🔧 Configuration

### Apollo Client Configuration

The Apollo Client is configured in `src/App.js`:
- GraphQL endpoint: `http://localhost:4000`
- Uses InMemoryCache for client-side caching
- Includes local resolvers for extended functionality

### TypeScript Configuration

TypeScript settings are defined in `tsconfig.json`. The project supports both `.js` and `.tsx` files.

## 🐛 Troubleshooting

- **GraphQL Connection Issues**: Ensure your backend server is running on `http://localhost:4000`
- **Authentication Problems**: Check that tokens are being stored correctly in localStorage
- **Build Errors**: Clear `node_modules` and reinstall dependencies

## 📝 Scripts

- `yarn start` - Start development server
- `yarn build` - Create production build
- `yarn test` - Run test suite
- `yarn eject` - Eject from Create React App (irreversible)

## 🤝 Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is private and proprietary.

## 👥 Authors

Tenosia Project Team

---

**Note**: This is a frontend application that requires a GraphQL backend to function properly. Make sure your backend server is configured and running before starting the development server.
