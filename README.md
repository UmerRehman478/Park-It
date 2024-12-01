# 🚗 Park It!

# Parking Ticket Purchase App 🚗

Parkit is a simple parking ticket purchase application that integrates with **Stripe** for payment processing. Built with **Next.js**, **Chakra UI**, and a **Redis-backed session store**, Parkit ensures a smooth user experience for purchasing and validating parking tickets.

## Features

- **Dynamic Rate Display**: Fetch and display parking rates dynamically.
- **License Plate Registration**: Users can input their license plate to generate a unique parking ticket.
- **Secure Payments with Stripe**:
  - Payment sessions are created using Stripe Checkout.
  - Metadata like the license plate is securely passed to Stripe for processing.
  - Stripe webhooks handle payment status updates.
- **Session Management**: Redis is used to store and validate parking ticket sessions for 24 hours.
- **User Feedback**: Displays success messages post-payment.

## Components

### Frontend (Next.js and Chakra UI)

- **Home**: Users enter their license plate and view the current parking rate.
- **Success**: Confirms successful payments with a user-friendly message.

### API

- **`/api/ticket`**: Handles ticket purchase requests by creating a Stripe payment session.
- **`/api/rate`**: Fetches the parking rate.

### Backend Utilities

- **Stripe Webhooks**: Listens for payment events and updates ticket sessions.
- **Redis**: Stores license plate sessions for ticket validation.

## Prerequisites

Please ensure you have the latest version of Node.js installed on your machine. [Get it here](https://nodejs.org/en/)


## Getting Started

Navigate to the directory where this project is cloned and install all dependencies:

```bash
npm install
```

Then, run the development server:

```bash
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

You can start editing the page by modifying `pages/index.tsx`. The page auto-updates as you edit the file.

The `pages/api` directory is mapped to `/api/*`. Files in this directory are treated as [API routes](https://nextjs.org/docs/api-routes/introduction) instead of React pages.

## Learn More

To learn more about Next.js, take a look at the following resources:

- [Next.js Documentation](https://nextjs.org/docs) - learn about Next.js features and API.
- [Learn Next.js](https://nextjs.org/learn) - an interactive Next.js tutorial.

You can check out [the Next.js GitHub repository](https://github.com/vercel/next.js/) - your feedback and contributions are welcome!

To learn more about Stripe, take a look at the following resources: 
- [Stripe Getting started](https://stripe.com/docs/development/get-started) - learn about Stripe with any programming language
- [Stripe Checkout](https://stripe.com/docs/payments/checkout) - Learn about the low-code checkout platform
