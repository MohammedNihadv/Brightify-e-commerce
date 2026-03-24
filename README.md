# 🛍️ Brightify

🌐 https://brightify.online  
📅 Built: March 2026  
🚀 Status: Production  

A full-stack e-commerce platform built from scratch, covering everything from product browsing to real payment processing and deployment.

---

## Overview

Brightify is a modern online store designed to simulate a real-world e-commerce system.  
The project focuses on building a complete production-ready workflow including frontend UI/UX, backend APIs, authentication, payment integration, deployment, and scaling.

---

## Architecture

Frontend and backend are deployed together using a serverless approach.

- React app served as static build  
- Django REST API served via serverless functions  
- API routing handled through Vercel rewrites  
- Supabase used for database + media storage  

---

## Tech Stack

### Frontend
- React (Vite)
- TailwindCSS
- Redux Toolkit
- React Router
- Axios

### Backend
- Django
- Django REST Framework
- JWT Authentication (SimpleJWT)

### Services & Integrations
- Razorpay — payment processing  
- Supabase — PostgreSQL + object storage  
- Brevo — email OTP system  
- Vercel — hosting & CDN  
- GoDaddy — domain management  

---

## Features

### E-commerce Core
- Product listing with categories  
- Product detail pages with reviews  
- Cart system  
- Checkout & order placement  

### Payments
- Razorpay integration  
- Backend payment verification  
- Secure order confirmation  

### User System
- JWT-based authentication  
- Email OTP login system  
- User profile & order history  

### Admin
- Admin dashboard  
- Product & category management  
- Order tracking  

---

## Application Flow

**User Journey:**
Browse → Add to Cart → Checkout → Payment → Verification → Order Confirmation

**Payment Flow:**
1. Order created in backend  
2. Razorpay order generated  
3. Payment modal opened  
4. User completes payment  
5. Backend verifies signature  
6. Order marked as paid  

---

## Deployment

- Hosted on Vercel (frontend + backend)  
- Django runs as serverless functions  
- Custom domain configured via GoDaddy  
- HTTPS enabled by default  
- Global CDN for fast delivery  

---

## Project Structure

```
frontend/
├── components/
├── pages/
├── slices/
├── utils/

backend/
├── store/
├── orders/
├── payments/
├── users/
```

---

## Storage

Supabase is used for product images, category images, and banners.
Images are compressed during upload to reduce size and improve load time.

---

## Security

- JWT authentication  
- Email OTP verification  
- Razorpay signature validation  
- CORS configuration  
- HTTPS enabled  

---

## Performance

Optimizations implemented:
- Lazy loading for all pages  
- Code splitting  
- Image optimization  
- Error boundaries for stability  

**Current status:**
- Good desktop performance  
- Mobile performance needs improvement  
- LCP requires optimization  

---

## Challenges & Fixes

- Debugged Razorpay payment issues  
- Fixed media URL handling for storage  
- Resolved stale chunk errors after deployment  
- Improved UI loading states  
- Fixed navigation and dropdown issues  
- Stabilized codebase after regressions  

---

## Usage

Currently running on Vercel Hobby plan:
- Low request usage  
- Minimal resource consumption  
- Easily scalable  

---

## Roadmap

- Improve performance (reduce LCP)  
- Add search autocomplete  
- Wishlist functionality  
- Email notifications for orders  
- PWA support  
- Enhanced admin analytics  

---

## Goal of the Project

I built this project to challenge myself to go beyond basic UI development. I wanted to get hands-on experience with real-world complexities like integrating actual payment gateways, designing backend architectures, debugging live production deployments, and preparing for freelance work.

---

## Author

**Mohammed Nihad**

I handled the end-to-end development of this platform, from designing the frontend and building the Django APIs to configuring the Vercel deployment and debugging production regressions.
