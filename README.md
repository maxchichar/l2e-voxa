# L2E Voxa

> Anonymous idea and feedback platform for Learn2Earn students.

**L2E Voxa** is a private, anonymous community platform where verified Learn2Earn students can share ideas, feedback, concerns, and solutions openly without fear of identity exposure or reputational risk.

---

## Tech Stack

| Layer | Technology |
|---|---|
| Backend | Go (Golang) + Gin |
| Database | PostgreSQL |
| Frontend | Next.js (React) |
| Auth | JWT + anonymous session layer |
| AI Features | Groq API (Llama 3) — free tier · Anthropic Claude API when funded |
| Hosting | Railway (backend) + Vercel (frontend) |

---

## Project Structure

```
l2e-voxa/
├── backend/
│   ├── cmd/
│   │   └── server/
│   │       └── main.go
│   ├── internal/
│   │   ├── auth/
│   │   ├── handlers/
│   │   ├── middleware/
│   │   ├── models/
│   │   ├── repository/
│   │   └── services/
│   ├── db/
│   │   └── migrations/
│   ├── config/
│   └── go.mod
├── frontend/
│   ├── app/
│   ├── components/
│   ├── lib/
│   └── package.json
├── .env.example
├── docker-compose.yml
└── README.md
```

---

## Core Features

- **Anonymous Publishing** — posts are never linked to a real identity in public tables
- **Persona Masks** — rotating anonymous personas per session, refreshed every 24 hours
- **Echo Score™** — posts ranked by usefulness and impact, not popularity
- **Pulse Board™** — live dashboard of trending topics and community sentiment
- **Campus Signals™** — campus-specific feeds while maintaining anonymity
- **Solution Battles™** — community votes on the best solution to a posted problem
- **Leadership Inbox™** — escalate high-value posts to leadership without exposing the author
- **Reality Check™** — AI evaluates post quality before publishing
- **Shadow Consensus™** — blind voting, results revealed only after voting closes
- **Signal vs Noise Engine™** — AI-powered feed curation

---

## Getting Started

### Prerequisites

- Go 1.22+
- Node.js 20+
- PostgreSQL 15+
- A Groq API key (free — for AI features during pre-funding phase)

### Clone the repo

```bash
git clone https://github.com/yourusername/l2e-voxa.git
cd l2e-voxa
```

### Backend setup

```bash
cd backend
cp ../.env.example .env
# Fill in your environment variables

go mod tidy
go run cmd/server/main.go
```

### Frontend setup

```bash
cd frontend
npm install
npm run dev
```

### Database setup

```bash
# Run migrations
cd backend
go run db/migrations/migrate.go
```

---

## Environment Variables

```env
# Server
PORT=8080
ENV=development

# Database
DB_HOST=localhost
DB_PORT=5432
DB_USER=postgres
DB_PASSWORD=yourpassword
DB_NAME=l2evoxa

# Auth
JWT_SECRET=your_jwt_secret
JWT_EXPIRY=24h

# AI — currently using Groq (free tier) during pre-funding phase
# Switch to Anthropic Claude API once funding is secured for higher quality and reliability
GROQ_API_KEY=your_groq_api_key
# ANTHROPIC_API_KEY=your_anthropic_api_key  # uncomment when funded

# Frontend
NEXT_PUBLIC_API_URL=http://localhost:8080
```

---

## Roadmap

### MVP (Phase 1)
- [ ] Student verification + auth
- [ ] Anonymous post creation
- [ ] Campus Signals™ feed
- [ ] Echo Score™ ranking
- [ ] Basic voting system

### Phase 2
- [ ] Persona Masks system
- [ ] Solution Battles™
- [ ] Pulse Board™ dashboard
- [ ] Leadership Inbox™

### Phase 3 — AI Layer
> Currently using **Groq (free tier)** with Llama 3 for all AI features. Upgrade to **Anthropic Claude API** is planned once funding is secured — no code changes needed, just a provider swap.

- [ ] Reality Check™ (Groq / Llama 3 → Claude when funded)
- [ ] Signal vs Noise Engine™
- [ ] Shadow Consensus™
- [ ] Confidence Meter™

### Phase 4
- [ ] Idea Heat Map
- [ ] Collective Brain Mode
- [ ] Anonymous Debate Arena
- [ ] Legacy Ideas™ archive
- [ ] Whisper Feed
- [ ] Idea Seasons

---

## Contributing

This platform is exclusively for the Learn2Earn ecosystem. Contributions from verified L2E students and collaborators only.

1. Fork the repo
2. Create a feature branch (`git checkout -b feature/your-feature`)
3. Commit your changes (`git commit -m 'add: your feature'`)
4. Push to the branch (`git push origin feature/your-feature`)
5. Open a Pull Request

---

## License

Private — All rights reserved. Not open for public use outside the Learn2Earn ecosystem.

---

*The strongest communities are not built by the loudest voices. They are built by the most honest ones.*
