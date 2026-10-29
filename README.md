# Error404 — Job Platform

A full-stack job board where employers post listings, candidates apply with resumes and cover letters, and admins moderate users, jobs and support tickets.

**Design:** [Figma](https://www.figma.com/design/gp5XfhU1UvCCuYPDm965kN/Web-UI?node-id=0-1&p=f&t=WdMoPw9Y1dr6hqgZ-0)

> Team project for COSC 360 (UBC Okanagan). This is my fork of [NathanIsCoding/Error404](https://github.com/NathanIsCoding/Error404).

## Features

- **Accounts:** sign up and sign in with JWT auth and bcrypt-hashed passwords, plus editable profiles with photo and resume upload
- **Jobs:** create, edit and delete listings, with search, filters by industry and job type, and pagination
- **Applications:** apply with a resume and cover letter, and employers can update each application's status
- **Profiles:** public profile pages with comments
- **Admin panel:** enable or disable users, grant admin, moderate jobs, and handle support tickets

## Tech stack

| Layer   | Stack                                              |
| ------- | -------------------------------------------------- |
| Client  | React 19, React Router, Vite, Tailwind CSS         |
| Server  | Node.js, Express, Mongoose, JWT, Multer            |
| Data    | MongoDB                                            |
| Testing | Jest + React Testing Library (client), Jest (server) |
| Ops     | Docker Compose                                     |

## Project structure

```
client/   React + Vite frontend (components, pages, tests)
server/   Express API (routes, models, middleware, tests)
docker-compose.yml   API + MongoDB
```

## Getting started

```bash
# API + MongoDB via Docker
docker compose up --build        # API on http://localhost:3000

# or run each side manually
cd server && npm install && npm run dev
cd client && npm install && npm run dev
```

Run the tests with `npm test` in either `client/` or `server/`.
