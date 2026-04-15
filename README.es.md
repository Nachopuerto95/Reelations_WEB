<p align="end">
   <strong>🌐 Cambiar idioma:</strong><br>
   <a href="/README.es.md">
    <img src="https://github.com/Nachopuerto95/multilang/blob/main/ES.png" alt="Español" width="50">
  </a>&nbsp;&nbsp;&nbsp;
  <a href="/README.md">
    <img src="https://github.com/Nachopuerto95/multilang/blob/main/EN.png" alt="English" width="50">
  </a>
</p>

# 🎬 Reelations

<p align="center">
  <img src="https://github.com/Nachopuerto95/Nachopuerto95/blob/main/assets/reelations.gif?raw=true" alt="Demo de Reelations" width="600"/>
</p>

<p align="center">
  <a href="https://project-module2.fly.dev/">
    <img src="https://custom-icon-badges.demolab.com/badge/App%20en%20vivo-6f42c1?logo=link&logoColor=fff" alt="App en vivo"/>
  </a>
</p>

## 📜 Sobre el proyecto

Reelations es una pequeña red social alrededor del cine: buscas pelis, las reseñas, te haces listas, sigues a otros usuarios y comentas sus reviews. Imagina Letterboxd, pero en mucho más pequeño y como proyecto de escuela.

Renderizado en servidor con **Handlebars** sobre un backend **Express + MongoDB**. Las sesiones viven en MongoDB, así que puedes reiniciar el servidor sin tirar a los usuarios.

## ✨ Qué hace

- **Auth** con bcrypt y cookies de sesión respaldadas en `connect-mongo`.
- **Búsqueda de películas** contra una API externa de pelis (estilo TMDB).
- **Reviews**: escribir, editar, borrar. Otros usuarios pueden comentar.
- **Listas**: construir tus propias listas (watchlist, favoritas, lo que sea).
- **Géneros**: navegar por categorías.
- **Perfil**: tu actividad, tus reviews, tus listas.
- **Script de seed** (`npm run seeds`) para poblar la BD en desarrollo.

## 🧱 Stack

- Node.js + Express
- MongoDB + Mongoose
- Handlebars (`hbs`) — vistas en servidor
- `express-session` + `connect-mongo`
- `bcrypt` para contraseñas
- `node-fetch` para la API externa de pelis
- Morgan para logs
- Docker + Fly.io para el deploy

## 🔧 Ejecución local

```bash
npm install
npm run seeds      # poblar la BD (primera vez)
npm run dev        # http://localhost:3000
```

El `.env` necesita: `MONGO_URI`, `SESSION_SECRET` y la API key del servicio de pelis.

## 🚀 Despliegue

En vivo en Fly.io en Madrid (`mad`) como `project-module2`:

```bash
fly deploy
```

👉 [project-module2.fly.dev](https://project-module2.fly.dev/)

## 📂 Estructura

```
Reelations_WEB/
├── app.js
├── bin/
├── configs/          # db, session, hbs helpers, api config
├── controllers/      # home, movies, profile, review, list, user, search
├── middlewares/
├── models/           # User, Movies, Review, List, Genre
├── routes/
├── views/            # plantillas .hbs
├── public/           # css, js, estáticos
├── Dockerfile
└── fly.toml
```

## 🛠️ Contexto

Es el proyecto M2 del bootcamp fullstack que hice antes de entrar en 42. Lo mantengo porque el alcance es acotado y la UI envejece bien. El deploy sigue en pie.
