# Little Canvas Books web app starter

## Included files
- `index.html` — browser-only business manager prototype. Records are stored in this browser's localStorage and do not sync between devices. It is not secure enough for real customer data without authentication and a shared backend.
- `track-order.html` — responsive customer order tracking page, prepared for a Supabase RPC connection.
- `little-canvas-books-logo.png` — transparent PNG logo used by both pages.

## Branding and deadlines
- Slogan is intentionally blank. An optional slogan setting is available in the admin prototype for future use.
- New orders default to a delivery deadline six calendar days after the order date. The deadline field can be changed per order.
- The admin dashboard highlights orders due today, due tomorrow, and overdue.
- The customer tracking page can show a delivery countdown when the backend response includes `due_date`, `dueDate`, or `delivery_deadline`. The backend RPC must return a customer-safe due date.
- Countdown uses Asia/Colombo time for the customer page.

## Important limitations before production
1. The admin page is still local-only. It has no login and does not share records between your device and your friend's device.
2. Customer tracking does not work until a Supabase project is configured and the `public_order_tracking` RPC is created and returns a safe response.
3. Do not expose service-role keys, customer contact details, children's photos, payment records, or internal notes in public files or customer-facing responses.
4. Review the database function for enumeration protection and rate limiting before public launch.
5. GitHub Pages hosts static files only; it is not a backend/database.

## Local preview
Keep all three files in the same directory and open `index.html` or `track-order.html` in a browser.
