# PurePick – Project Review 2

PurePick is a grocery shopping demo built with **React + Vite**. It includes separate Customer and Admin modules, Local Storage authentication, shopping cart, checkout, order tracking/status management and inventory management. Product/category/hero pictures from the supplied project are retained in `public/images`.

## Run locally
1. Install Node.js (LTS).
2. Extract this ZIP and open the `PurePick_Review2_ReactVite` folder in VS Code.
3. Open Terminal and run:
   ```bash
   npm install
   npm run dev
   ```
4. Open the localhost URL printed by Vite.

## Demo login
- **Admin:** `admin@purepick.com`
- **Password:** `admin123`
- Customer: use **Sign up** to create an account, then log in as Customer.

## Deploy to Vercel
1. Create a GitHub repository and upload/push all files in this folder (including `package.json`, `src`, `public`, `vite.config.js`, and `vercel.json`).
2. In Vercel choose **Add New → Project**, import the GitHub repository.
3. Framework preset: **Vite**. Build command: `npm run build`. Output directory: `dist`.
4. Click Deploy. `vercel.json` includes an SPA rewrite so routes work on refresh.
5. Test the deployed URL: sign up/login as customer, add products, place an order, then log out and login as admin to update the order and manage inventory.
6. Add your GitHub repository URL and Vercel deployment URL to your review presentation.

## Git commands
```bash
git init
git add .
git commit -m "PurePick React Vite review project"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/YOUR-REPOSITORY.git
git push -u origin main
```

## Modules
- **Customer:** signup/login, browse/search/filter products, cart, delivery details, place/cancel orders, view order history.
- **Admin:** protected admin login, dashboard statistics, view all customer orders, update order status, add/delete inventory products.

## Important demo limitation
Authentication and project data use browser Local Storage as required for this academic demo. This is not production-grade security: credentials and data are stored in the browser and are not shared across different devices/browsers. Use a backend/database and hashed passwords before real-world deployment. The admin demo credentials are visible in this README for review purposes.

## Review 2 updates

- Separate Customer and Admin login modes are available from the login page.
- The Admin dashboard includes total orders, revenue, distinct customers who placed orders, and customer accounts with no order history.
- The Customer information table shows name, email, last login (for logins tracked by this version), login count, order count, total non-cancelled spend, and order activity. Use **Refresh dashboard** to reload orders, inventory, and customer records.
- Adding products to the cart no longer opens an alert for every click. A small confirmation is shown only once per browser session; the cart badge updates as quantities change.
- The cart/order summary displays each selected product, quantity, item count, and total before the customer places the order.

## Demo credentials and data notes

- Admin email: `admin@purepick.com`
- Admin password: `admin123`
- Customers can create an account from **Sign up**.
- This project is a frontend demonstration using browser `localStorage`. Customer accounts, login activity, carts, and orders are stored in the current browser on the current device. It is not a production multi-user database, and data will not automatically synchronize between different devices or browsers. For a real deployment, connect authentication and order storage to a backend/database and never store plain-text passwords.
