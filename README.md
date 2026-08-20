# KVS Hospital — Full-Stack Management System

React/Vite public site with an Express/PostgreSQL REST API, JWT authentication, bcrypt password storage, role middleware, validated registration, appointment collision protection and seeded KVS leadership/partner information.

## Run locally

1. Install Node.js 20+ and PostgreSQL 15+.
2. Create a PostgreSQL database called `kvs_hospital`; copy `backend/.env.example` to `backend/.env` and configure it.
3. Run `npm install`, `npm --prefix backend install`, and `npm --prefix frontend install`.
4. Run `npm --prefix backend run seed`, then `npm run dev`.

The public site runs at `http://localhost:5173`; API at `http://localhost:4000`.

## Public deployment (Render)

This repository includes `render.yaml`, which creates the API, the static web site, and PostgreSQL. After Render creates both services, set `VITE_API_URL` on **kvs-hospital-web** to `https://<your-api-service>.onrender.com/api`, set `FRONTEND_URL` on **kvs-hospital-api** to the static site's URL, then redeploy both services. Run `npm run seed` in the API service Shell once to populate the KVS content and development accounts.

Development-only accounts use the addresses specified in the brief and password `KvsDevOnly!2026`. Change all development credentials and `JWT_SECRET` before production deployment.
