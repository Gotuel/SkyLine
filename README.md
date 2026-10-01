# Skyline Weather

A visual, responsive weather dashboard designed as a portfolio project.

## Stack

- React + Vite
- Node.js + Express
- Open-Meteo API (no API key required)

## Features

- Search weather by city
- Current conditions, apparent temperature, humidity, wind, sunrise and sunset
- Five-day forecast
- Responsive design
- API proxy that keeps third-party requests on the server

## Local setup

```bash
npm run install:all
npm run dev
```

Open `http://localhost:5173`.

## Deploy on Render

Deploy the API first as a **Web Service**:

- Root directory: `server`
- Build command: `npm install`
- Start command: `npm start`
- Health check path: `/health`

Then deploy the React client as a **Static Site**:

- Root directory: `client`
- Build command: `npm run build`
- Publish directory: `dist`
- Environment variable: set `VITE_API_URL` to the public URL of the API service, for example `https://skyline-weather-api.onrender.com`

Render rebuilds the client when this environment variable changes. The variable is optional locally because Vite proxies `/api` to the local Express server.
