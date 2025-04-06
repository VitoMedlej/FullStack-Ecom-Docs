# Fullstack eCommerce Template

> A modern fullstack eCommerce template with AI-powered recommendations, custom chatbot, Sanity CMS, Auth0 authentication, full dashboard, and a Node.js API. Built for speed, scalability, and developer experience.

---

## Table of Contents

- [Repositories](#repositories)  
- [Features](#features)  
- [Tech Stack](#tech-stack)  
- [Prerequisites](#prerequisites)  
- [Getting Started](#getting-started)  
- [Environment Variables](#environment-variables)  
  - [Backend](#backend)  
  - [Frontend](#frontend)  
  - [Sanity Studio](#sanity-studio)  
- [Scripts](#scripts)  
- [Contributing](#contributing)  
- [License](#license)  

---

## Repositories

- **Frontend**: https://github.com/yourname/frontend  
- **Backend**: https://github.com/yourname/backend  
- **CMS (Sanity Studio)**: https://github.com/yourname/studio  

---

## Features

- 🛍️ AI‑powered product recommendations  
- 💬 Custom chatbot for customer support  
- ✍️ Sanity CMS for content management  
- 🔒 Auth0 authentication (email/password & social)  
- 📊 Full admin dashboard  
- 🚀 Node.js REST API with rate limiting & CORS  
- 🗄️ MongoDB integration  
- 📱 Responsive UI (mobile & desktop)  

---

## Tech Stack

- **Frontend**: React, Next.js, TypeScript  
- **Backend**: Node.js, Express, TypeScript  
- **CMS**: Sanity v3  
- **Auth**: Auth0  
- **Database**: MongoDB Atlas  
- **AI Tools**: OpenAI, Recombee (or your choice)  

---

## Prerequisites

- Node.js v18+  
- npm or Yarn  
- MongoDB Atlas account  
- Auth0 account  
- Sanity account  
- OpenAI/Recombee API keys (for AI features)  

---

## Getting Started

1. **Clone each repo**  
   ```bash
   git clone https://github.com/yourname/frontend.git
   git clone https://github.com/yourname/backend.git
   git clone https://github.com/yourname/studio.git
Copy & fill .env
In each folder, run:

bash
Copy
Edit
cp .env.example .env
then update values with your own keys/URLs.

Install dependencies

bash
Copy
Edit
cd frontend && npm install
cd backend  && npm install
cd studio   && npm install
Run development servers

bash
Copy
Edit
# Frontend
cd frontend && npm run dev

# Backend
cd backend && npm run dev

# Sanity Studio
cd studio && npm run dev
Open in browser

Frontend: http://localhost:3000

Backend API: http://localhost:8080

Sanity Studio: http://localhost:3333

Environment Variables
⚠️ Make sure each repo’s .env is listed in its .gitignore!

🖥️ Backend (backend/.env.example)
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

# Auth0 (if used)
AUTH0_DOMAIN="your-auth0-domain"
AUTH0_AUDIENCE="your-auth0-audience"

# AI / Recommendations
OPENAI_API_KEY="your_openai_api_key"
RECOMBEE_API_KEY="your_recombee_api_key"
RECOMBEE_DATABASE_ID="your_recombee_database_id"
🌐 Frontend (frontend/.env.example)
env
Copy
Edit
# API
NEXT_PUBLIC_API_URL="http://localhost:8080/api"

# Auth0
NEXT_PUBLIC_AUTH0_DOMAIN="your-auth0-domain"
NEXT_PUBLIC_AUTH0_CLIENT_ID="your-auth0-client-id"

# Sanity
NEXT_PUBLIC_SANITY_PROJECT_ID="your_sanity_project_id"
NEXT_PUBLIC_SANITY_DATASET="production"

# AI Features
NEXT_PUBLIC_OPENAI_API_KEY="your_openai_api_key"
✍️ Sanity Studio (studio/.env.example)
env
Copy
Edit
SANITY_PROJECT_ID="your_sanity_project_id"
SANITY_DATASET="production"
SANITY_API_TOKEN="your_sanity_api_token"
Scripts
Each repo defines its own package.json scripts. See individual READMEs for details:

Frontend: npm run dev, npm run build, npm run start

Backend: npm run dev, npm run build, npm run start

Studio: npm run dev, npm run deploy

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

License
MIT © [Your Name]
