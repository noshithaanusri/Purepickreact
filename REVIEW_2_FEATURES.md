# PurePick – Review 2 Feature Notes

## Customer module
1. Customer sign up and customer login.
2. Browse/search groceries and filter by category.
3. Add products to the cart; repeated adds increase the quantity without repeated popup alerts.
4. Cart badge displays the current total quantity.
5. Cart review shows product names, quantities, item count, price per line, and grand total before checkout.
6. Customer enters delivery information and places an order.
7. Customer can view order history and cancel an order.

## Admin module
1. Separate admin login.
2. Dashboard displays total orders and revenue from non-cancelled orders.
3. Distinct customer count for customers who have placed at least one order.
4. Count of customer accounts that have not placed an order.
5. Customer table includes name, email, last login when tracked, login count, order count, total non-cancelled spend, and activity status.
6. View customer orders and update order status.
7. Add and delete inventory products.
8. Refresh dashboard data from browser storage.

## Technology used
- React for reusable UI components and state.
- React Router for page navigation and protected admin/customer routes.
- Vite for development server and production build.
- JavaScript for cart, authentication demo, order calculations, and dashboard metrics.
- CSS for responsive styling.
- Browser localStorage for demo persistence.

## Important review explanation
The customer counts are unique by customer email, not by number of orders. “Customers who placed orders” counts unique customer emails found in order records. “Logged in, no order” counts registered customer accounts that do not appear in the order records. The current app is a frontend/localStorage prototype; real multi-device customer analytics require a backend database and secure authentication.
