# 🍔 Feastique - Restaurant Ordering System

A full-stack restaurant ordering system built with React, Ionic, Node.js, Express, and MySQL. This application provides a seamless food ordering experience with real-time order tracking and management.

## ✨ Features

- 🎯 Browse menu items by categories
- 🛒 Add items to cart and place orders
- 💳 Multiple payment options (COD, Online)
- 📦 Real-time order tracking
- 👨‍💼 Admin panel for order management
- 📱 Responsive design with Ionic components
- 🔐 Secure authentication with JWT
- 💾 MySQL database for data persistence

## 🛠️ Tech Stack

### Frontend
- **React** - UI library
- **Ionic React** - Mobile-first UI components
- **React Router** - Navigation
- **Axios** - HTTP client
- **TypeScript** - Type safety
- **Vite** - Build tool

### Backend
- **Node.js** - Runtime environment
- **Express.js** - Web framework
- **MySQL2** - Database driver
- **JWT** - Authentication
- **Bcrypt** - Password hashing
- **CORS** - Cross-origin resource sharing

## 📋 Prerequisites

Before running this project, make sure you have:

- Node.js (v14 or higher)
- MySQL Server (v5.7 or higher)
- npm or yarn package manager

## 🚀 Installation & Setup

### 1. Clone the repository

```bash
git clone https://github.com/Arshil903/feastique.git
cd feastique
```

### 2. Setup Database

1. Start your MySQL server
2. Run the database setup script:

```bash
mysql -u root -p < backend/database.sql
```

Or manually create the database using the SQL file in `backend/database.sql`

### 3. Backend Setup

```bash
cd backend
npm install
```

Create a `.env` file in the backend directory:

```env
PORT=5000
DB_HOST=localhost
DB_USER=root
DB_PASSWORD=your_mysql_password
DB_NAME=mcdonalds_db
JWT_SECRET=your_jwt_secret_key
```

**Important:** Copy `.env.example` to `.env` and fill in your actual credentials. Never commit the `.env` file to Git!

Start the backend server:

```bash
npm start
# Or for development with auto-reload
npm run dev
```

The backend will run on `http://localhost:5000`

### 4. Frontend Setup (Main App)

```bash
# Go back to root directory
cd ..
npm install
npm run dev
```

### 5. Tomato App Setup (Alternative Frontend)

```bash
cd tomato
npm install
npm run dev
```

## 📁 Project Structure

```
feastique/
├── backend/                 # Backend Node.js/Express server
│   ├── database.sql        # Database schema and sample data
│   ├── db.js              # Database connection
│   ├── server.js          # Express server entry point
│   ├── init-db.js         # Database initialization
│   └── package.json       # Backend dependencies
├── src/                    # Frontend React source
│   ├── components/        # Reusable components
│   ├── pages/            # Page components
│   └── App.tsx           # Main app component
├── tomato/                # Alternative Ionic React app
│   ├── public/           # Static assets
│   └── src/             # Tomato app source
└── package.json          # Root dependencies
```

## 🎯 Usage

1. **Browse Menu**: Navigate through different food categories
2. **Add to Cart**: Select items and add them to your cart
3. **Checkout**: Enter delivery details and payment method
4. **Track Order**: Monitor your order status in real-time
5. **Admin Access**: Manage orders and menu items (admin panel)

## 📸 Screenshots

<!-- Add your screenshots here -->

## 🔑 API Endpoints

### Menu Items
- `GET /api/menu` - Get all menu items
- `GET /api/menu/:id` - Get specific menu item
- `POST /api/menu` - Add new menu item (Admin)
- `PUT /api/menu/:id` - Update menu item (Admin)
- `DELETE /api/menu/:id` - Delete menu item (Admin)

### Orders
- `POST /api/orders` - Create new order
- `GET /api/orders/:id` - Get order details
- `PUT /api/orders/:id` - Update order status
- `GET /api/orders` - Get all orders (Admin)

### Authentication
- `POST /api/auth/register` - Register new user
- `POST /api/auth/login` - User login

## 🧪 Testing

```bash
# Run unit tests
npm run test.unit

# Run E2E tests
npm run test.e2e
```

## 🏗️ Building for Production

### Frontend
```bash
npm run build
```

### Backend
The backend runs as-is in production. Consider using PM2 for process management:

```bash
npm install -g pm2
pm2 start backend/server.js --name feastique-api
```

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the project
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👨‍💻 Author

Mohammad Arshil Mansuri - [GitHub Profile](https://github.com/Arshil903)

## 🙏 Acknowledgments

- Ionic Framework for the amazing UI components
- React community for excellent libraries
- All contributors who help improve this project

## 📧 Contact

For any queries or support, please reach out to:
- Email: arshilmansuri903@gmail.com
- GitHub: [@Arshil903](https://github.com/Arshil903)

---

Made with ❤️ for food lovers
