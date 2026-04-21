# Razorpay Payment Testing

A full-stack web application for testing **Razorpay** payment gateway integration.

## Tech Stack

![React](https://img.shields.io/badge/React-18-61DAFB?logo=react&logoColor=white)
![Vite](https://img.shields.io/badge/Vite-5.1-646CFF?logo=vite&logoColor=white)
![TailwindCSS](https://img.shields.io/badge/TailwindCSS-3.4-06B6D4?logo=tailwindcss&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-Express-339933?logo=node.js&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-Mongoose-47A248?logo=mongodb&logoColor=white)
![Razorpay](https://img.shields.io/badge/Razorpay-Payment-02042B?logo=razorpay&logoColor=white)
![Framer Motion](https://img.shields.io/badge/Framer_Motion-11-0055FF?logo=framer&logoColor=white)

## Project Structure

```
Razorpay-Payment-Testing/
├── client/          # Frontend (React + Vite + TailwindCSS)
└── server/          # Backend (Express + MongoDB + Razorpay SDK)
```

## Features

- **Product Display** — Browse and select products from the home page
- **Razorpay Checkout** — Create payment orders and process transactions
- **Payment Verification** — Server-side signature verification for secure payments
- **Payment History** — Stores all payment records in MongoDB
- **Success Page** — Displays payment confirmation with reference ID

## How It Works

1. **Client** fetches products and displays them as cards
2. User clicks **Buy** to initiate a payment
3. **Server** creates a Razorpay order and returns order details
4. **Razorpay Checkout** modal opens for payment
5. After payment, **Server** verifies the signature using HMAC-SHA256
6. Payment record is updated in **MongoDB** and user is redirected to success page

## API Endpoints

| Method | Endpoint             | Description                     |
|--------|----------------------|---------------------------------|
| GET    | `/`                  | Server health check             |
| GET    | `/api/getkey`        | Get Razorpay public key         |
| POST   | `/api/checkout`      | Create a new Razorpay order     |
| POST   | `/api/paymentVerification` | Verify payment signature |

## Deployment

- **Client**: Deployed on Netlify (`netlify.toml` configured)
- **Server**: Deployed on Vercel (`vercel.json` configured)
