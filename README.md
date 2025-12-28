# Rikiki-Live-Scoreboard

A real-time live scoreboard application for the Rikiki (Oh Hell) card game.
The game itself is played with real cards; this application manages players, rounds, bids, tricks taken, and live standings.

The application supports:

- Creating and joining games via a shared Game ID
- Real-time updates using WebSockets
- Player and spectator modes
- Live standings and bidding phases
- No persistence (current game only)

## Tech Stack
### Frontend:

- React
- Material UI (MUI)
- WebSockets
- Vite
- JavaScript

### Backend

- Java 21+
- Spring Boot
- Spring WebSocket
- Maven

### Infrastructure

- GitHub Actions (CI)
- GitHub branch protection rules
- Docker (prepared, optional)
- No database (in-memory game state)

## Project Structure
```bash
rikiki-live-scoreboard/
├── backend/        # Spring Boot backend
├── frontend/       # React frontend
├── .github/
│   └── workflows/  # CI pipelines
└── README.md
```

## Local Development
### Backend
```bash
cd backend
./mvnw spring-boot:run
```


Backend runs on:
http://localhost:8080

### Frontend
```bash
cd frontend
npm install
npm run dev
```

Frontend runs on:
http://localhost:5173

## Branching Strategy

- **main**
  - Stable releases only
  - Protected branch
  - CI must pass
  - PR review required


- **develop**
  - Active development
  - All feature branches merge here
  - CI required

- **feature/***
  - One feature per branch
  - Merge into develop via PR

## CI/CD

- GitHub Actions builds and tests:
  - Backend (Maven)
  - Frontend (Node + Vite)

- Runs on:
  - Pull requests to `develop`
  - Pushes to `develop`


## Project Status

🚧 In active development