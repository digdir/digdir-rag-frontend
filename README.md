# RAG Chat Application

> **Note:** This project is a demonstration and is of alpha quality. It is not intended for production use without further development and testing.

A chat application with Retrieval Augmented Generation (RAG) capabilities, consisting of a React frontend and a Node.js backend-for-frontend (BFF) that proxies requests to a Headless RAG API.

## Architecture

```
┌─────────────────┐     ┌─────────────────┐     ┌─────────────────┐
│                 │     │                 │     │                 │
│  React Frontend │────▶│  Node.js BFF    │────▶│  Headless RAG   │
│  (Vite + TS)    │     │  (Express)      │     │  (RAG + Data)   │
│                 │     │                 │     │                 │
└─────────────────┘     └─────────────────┘     └─────────────────┘
```

- **Frontend**: React 19 with TypeScript, Vite, TanStack Query, Zustand, and Tailwind CSS
- **Backend BFF**: Node.js/Express providing authentication and API proxying
- **Headless RAG API**: External RAG service (not included in this repository)

## Quick Start

### Prerequisites

- Node.js 18+
- A running Headless RAG API backend with an API key

### Setup

1. **Install dependencies for both projects:**

```bash
cd frontend && npm install
cd ../backend-bff && npm install
```

2. **Configure the backend:**

```bash
cd backend-bff
cp .env.example .env
# Edit .env with your configuration
```

3. **Start both services:**

```bash
# Terminal 1 - Backend BFF
cd backend-bff && npm run dev

# Terminal 2 - Frontend
cd frontend && npm run dev
```

4. **Access the application:**
   - Frontend: http://localhost:5173
   - Backend BFF: http://localhost:3000

## Project Structure

```
rag-frontend/
├── frontend/          # React frontend application
│   └── README.md      # Frontend-specific documentation
├── backend-bff/       # Node.js backend-for-frontend
│   └── README.md      # Backend-specific documentation
└── README.md          # This file
```

## Documentation

For detailed information about each component, see:

- [Frontend README](frontend/README.md) - React application setup, features, and development
- [Backend BFF README](backend-bff/README.md) - Authentication, API endpoints, and deployment

## Features

- Domain-based email authentication
- Session management
- Conversation management
- RAG-powered chat with streaming responses
- Markdown and LaTeX rendering
- Norwegian Design System UI components

## License

MIT
