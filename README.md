# Fullstack TypeScript eCommerce Template🛒 - Documentation📄

> A modern fullstack TypeScript eCommerce template with AI‑powered recommendations (Recombee), custom chatbot, Sanity CMS, Auth0 authentication, full dashboard, and a Node.js API. Built for speed, scalability, and developer experience.

---

## Table of Contents

- [Repositories](#repositories)  
- [Features](#features)  
- [Tech Stack](#tech-stack)  
- [Prerequisites](#prerequisites)  
- [Getting Started](#getting-started)  
- [Environment Variables](#environment-variables)  
  - [Backend](#backend)  
  - [Ecommerce (frontend & Sanity)](#ecommerce-frontend--sanity)  
- [Sanity Client Config (frontend)](#sanity-client-config-frontend)  
- [Backend package.json (excerpt)](#backend-packagejson-excerpt)  
- [Scripts](#scripts)  
- [Contributing](#contributing)  
- [License](#license)  

---

## Repositories

- **Ecommerce (frontend + Sanity)**  
  https://github.com/VitoMedlej/ecommerce-site-template  
- **Backend**  
  https://github.com/VitoMedlej/express-ts-backend
- **Dashboard**    
  https://github.com/VitoMedlej/ecommerce-dashboard-template
---

## Features

- 🛍️ AI‑powered product recommendations (Recombee)  
- 💬 Custom chatbot for customer support  
- ✍️ Sanity CMS for content management  
- 🔒 Auth0 authentication (email/password & social)  
- 📊 Full admin dashboard  
- 🚀 Node.js REST API with rate limiting & CORS  
- 🗄️ MongoDB integration  
- 📱 Responsive UI (mobile & desktop)  

---

## Tech Stack

- **All code in TypeScript**  
- **Frontend**: React, Next.js  
- **Backend**: Node.js, Express  
- **CMS**: Sanity v3  
- **Auth**: Auth0  
- **Database**: MongoDB Atlas  
- **AI Tools**: Recombee  

---

## Prerequisites

- Node.js v18+  
- npm or Yarn  
- MongoDB Atlas account  
- Auth0 account  
- Sanity account  
- Recombee account & API key  

---

## Getting Started

1. **Clone repos**  
   ```bash
   git clone https://github.com/VitoMedlej/ecommerce-site-template.git
   git clone https://github.com/VitoMedlej/express-ts-backend.git
Copy & fill .env

bash
Copy
Edit
# Ecommerce (frontend & Sanity)
cd ecommerce-site-template
cp .env.example .env

# Backend
cd ../express-ts-backend
cp .env.example .env
Fill in your own keys/URLs.

Install dependencies

bash
Copy
Edit
# Ecommerce
cd ../ecommerce-site-template
npm install

# Backend
cd ../express-ts-backend
npm install
Run dev servers

bash
Copy
Edit
# Frontend
cd ecommerce-site-template
npm run dev

# Sanity Studio
cd ecommerce-site-template/sanity
npm run dev

# Backend
cd ../../express-ts-backend
npm run dev
Open in browser

Frontend: http://localhost:3000

Backend API: http://localhost:8080

Sanity Studio: http://localhost:3333

Environment Variables
⚠️ Ensure each repo’s .env is in .gitignore

Backend (express-ts-backend/.env.example)
env
Copy
Edit
# Environment
NODE_ENV="development"           # 'development' | 'production'
PORT="8080"                      # server port
HOST="localhost"                 # server hostname
IS_PROD="false"                  # 'true' in production

# CORS
CORS_ORIGIN="http://localhost:*" # allowed origin(s)

# Rate Limiting
COMMON_RATE_LIMIT_WINDOW_MS="1000"
COMMON_RATE_LIMIT_MAX_REQUESTS="20"

# Auth
JWT_SECRET="your_jwt_secret"

# MongoDB
MONGODB_CONNECTION="mongodb+srv://user:pass@cluster0.ewclu.net/?retryWrites=true&w=majority&appName=NewCluster"
MONGODB_CONNECTION_READONLY="mongodb+srv://user:pass@cluster0.dk2g9.mongodb.net/?retryWrites=true&w=majority&appName=NewCluster"
MONGO_DB_NAME="your_db_name"

# Auth0
AUTH0_DOMAIN="your-auth0-domain"
AUTH0_AUDIENCE="your-auth0-audience"

# Recombee
RECOMBEE_API_KEY="your_recombee_api_key"
RECOMBEE_DATABASE_ID="your_recombee_database_id"
Ecommerce (frontend & Sanity) (ecommerce-site-template/.env.example)
env
Copy
Edit
# Frontend
NEXT_PUBLIC_API_URL="http://localhost:8080/api"
NEXT_PUBLIC_AUTH0_DOMAIN="your-auth0-domain"
NEXT_PUBLIC_AUTH0_CLIENT_ID="your-auth0-client-id"
NEXT_PUBLIC_SANITY_PROJECT_ID="your_sanity_project_id"
NEXT_PUBLIC_SANITY_DATASET="production"
NEXT_PUBLIC_SANITY_TOKEN="your_sanity_token"
NEXT_PUBLIC_SANITY_USE_CDN="true"
NEXT_PUBLIC_SANITY_API_VERSION="2024-01-01"

# Sanity Studio
SANITY_PROJECT_ID="your_sanity_project_id"
SANITY_DATASET="production"
SANITY_USE_CDN="true"
SANITY_API_VERSION="2024-01-01"
SANITY_API_TOKEN="your_sanity_api_token"
Sanity Client Config (frontend)
ts
Copy
Edit
// lib/sanityClient.ts
import { createClient } from 'next-sanity';

export const sanityClient = createClient({
  projectId: process.env.NEXT_PUBLIC_SANITY_PROJECT_ID || "8hww7tr9",
  dataset: process.env.NEXT_PUBLIC_SANITY_DATASET || "production",
  useCdn: process.env.NEXT_PUBLIC_SANITY_USE_CDN === "true",
  apiVersion: process.env.NEXT_PUBLIC_SANITY_API_VERSION || "2024-01-01",
  token: process.env.NEXT_PUBLIC_SANITY_TOKEN,
});
Backend package.json (excerpt)
json
Copy
Edit
// express-ts-backend/package.json
{
  "name": "express-typescript-boilerplate",
  "version": "1.0.14",
  "description": "An Express boilerplate backend",
  "author": "Edwin Hernandez",
  "repository": "edwinhern/express-typescript-2024"
}
Scripts
See each repo’s package.json:

Ecommerce

npm run dev

npm run build

npm run start

Backend

npm run dev

npm run build

npm run start

Contributing
Fork the repo.

Create a branch:

bash
Copy
Edit
git checkout -b feat/your-feature
Commit your changes:

bash
Copy
Edit
git commit -m "feat: add awesome feature"
Push & open a PR.
