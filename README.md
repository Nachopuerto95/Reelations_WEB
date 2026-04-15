<p align="end">
   <strong>🌐 Change language:</strong><br>
   <a href="README.es.md">
    <img src="https://github.com/Nachopuerto95/multilang/blob/main/ES.png" alt="Español" width="50">
  </a>&nbsp;&nbsp;&nbsp;
  <a href="/README.md">
    <img src="https://github.com/Nachopuerto95/multilang/blob/main/EN.png" alt="English" width="50">
  </a>
</p>

# 🎬 Reelations

<p align="center">
  <img src="https://github.com/Nachopuerto95/Nachopuerto95/blob/main/assets/reelations.gif?raw=true" alt="Reelations demo" width="600"/>
</p>

<p align="center">
  <a href="https://project-module2.fly.dev/">
    <img src="https://custom-icon-badges.demolab.com/badge/Live%20app-6f42c1?logo=link&logoColor=fff" alt="Live app"/>
  </a>
</p>

## 📜 About

Reelations is a small social network around films: you search movies, review them, build lists, follow other users and comment on what they watched. Think Letterboxd, but much smaller and built as a school project.

Server-side rendered with **Handlebars** on top of an **Express + MongoDB** backend. Sessions live in MongoDB so you can restart the server without kicking everyone out.

## ✨ What it does

- **Auth** with bcrypt and session cookies backed by `connect-mongo`.
- **Movie search** against an external movies API (TMDB-style).
- **Reviews**: write, edit, delete. Other users can comment.
- **Lists**: build your own lists of films (watchlist, favourites, whatever you want).
- **Genres**: browse by category.
- **Profile**: your activity, your reviews, your lists.
- **Seed script** (`npm run seeds`) to populate the DB for development.

## 🧱 Stack

- Node.js + Express
- MongoDB + Mongoose
- Handlebars (`hbs`) — server-side views
- `express-session` + `connect-mongo`
- `bcrypt` for passwords
- `node-fetch` for the external movie API
- Morgan for logging
- Docker + Fly.io for deploy

## 🔧 Run locally

```bash
npm install
npm run seeds      # seed the DB (first run)
npm run dev        # http://localhost:3000
```

`.env` needs: `MONGO_URI`, `SESSION_SECRET`, and the API key for the movies service.

## 🚀 Deploy

Live on Fly.io in Madrid (`mad`) as `project-module2`:

```bash
fly deploy
```

👉 [project-module2.fly.dev](https://project-module2.fly.dev/)

## 📂 Layout

```
Reelations_WEB/
├── app.js
├── bin/
├── configs/          # db, session, hbs helpers, api config
├── controllers/      # home, movies, profile, review, list, user, search
├── middlewares/
├── models/           # User, Movies, Review, List, Genre
├── routes/
├── views/            # .hbs templates
├── public/           # css, js, static assets
├── Dockerfile
└── fly.toml
```

## 🛠️ Context

This was the M2 project of the full-stack bootcamp I did before joining 42. It's the one I keep running because the scope is tight and the UI ages well. Deploy is still up.
