# Gen-AI Interview App

This repository contains a React frontend and an Express backend for an interview report generator.

## Repository structure

- `Backend/` - Express API server
- `Frontend/` - Vite + React application

## Prerequisites

- Node.js installed
- npm installed

## Backend setup

1. Open a terminal and go to the backend folder:

```bash
cd Backend
```

2. Install dependencies:

```bash
npm install
```

3. Create a `.env` file in `Backend/` and add required environment variables.
   Example:

```env
MONGO_URI=mongodb://localhost:27017/gen-ai
JWT_SECRET=your_jwt_secret
GOOGLE_GENAI_API_KEY=your_google_genai_api_key
```

4. Start the backend server:

```bash
npm run dev
```

The backend runs on `http://localhost:3000` by default.

## Frontend setup

1. Open a second terminal and go to the frontend folder:

```bash
cd Frontend
```

2. Install dependencies:

```bash
npm install
```

3. Start the frontend development server:

```bash
npm run dev
```

The frontend runs on `http://localhost:5173` by default.

## Build frontend for production

From `Frontend/`:

```bash
npm run build
```

To preview the production build locally:

```bash
npm run preview
```

## Notes

- The backend currently allows CORS from `http://localhost:5173`.
- The frontend currently calls the API at `http://localhost:3000`.
- When deploying, update the frontend API base URL and backend CORS origin to your deployed domains.

## Running both services together

Run each service in its own terminal:

- Terminal 1: `cd Backend && npm install && npm run dev`
- Terminal 2: `cd Frontend && npm install && npm run dev`

## Useful scripts

### Backend

- `npm run dev` - start backend with `nodemon`

### Frontend

- `npm run dev` - start Vite development server
- `npm run build` - build production frontend
- `npm run preview` - preview the built frontend
- `npm run lint` - run ESLint
