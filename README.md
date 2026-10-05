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

The repository includes a [`render.yaml`](./render.yaml) Blueprint that creates both Render services and connects the client to the API automatically:

1. Push this repository and `render.yaml` to your Git provider.
2. In the [Render Dashboard](https://dashboard.render.com), choose **New > Blueprint** and connect this repository and branch.
3. Review and deploy the Blueprint. It creates the API Web Service and the client Static Site; the client receives the API hostname through `VITE_API_URL`.

The API runs on Node.js 22.16.0 and exposes `/health` as its health check. No API key is required. The client variable is optional locally because Vite proxies `/api` to the local Express server.
