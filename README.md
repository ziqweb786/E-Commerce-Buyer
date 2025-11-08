# Buyer E-Commerce App

Express-based buyer-facing storefront for an e-commerce demo. The app renders Pug templates and persists buyers, products, and orders in MongoDB via Mongoose.

## Prerequisites
- Node.js 16+ and npm
- MongoDB running locally or accessible via connection string (default expects `mongodb://localhost:27017`)

## Setup
1. Install dependencies:
   ```
   npm install
   ```
2. Configure MongoDB connection (optional):
   - Defaults to `mongodb://localhost:27017/productsList`.
   - Override with an environment variable before starting the app:
     ```
     set MONGODB_URI=mongodb://your-host:port/database
     ```
3. (Optional) Seed starter data:
   - Insert at least one buyer document into the `buyers` collection so login works.
   - Insert one seller document into the `User` collection with a `products` array so the storefront shows inventory.
   - You can use MongoDB Compass, the shell, or a custom `seed.js` script.

## Running
1. Start MongoDB locally (`mongod` listening on port 27017).
2. Launch the server:
   ```
   npm start
   ```
3. Open the app at `http://localhost:4000`. Change the port by setting `PORT` before starting:
   ```
   set PORT=5000
   npm start
   ```

## Available Scripts
- `npm start` launches the Express server using `bin/www`.

## Notes
- Sessions are stored in-memory via `express-session`. For production, plug in a persistent session store.
- Orders are generated when a logged-in buyer submits the shipping form; ensure the `cart` cookie contains items created via the product pages.


