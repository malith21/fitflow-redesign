# FitFlow Redesign

Full-stack redesign of the FitFlow fitness app, produced for **IT3060 — Human Computer Interaction**, Sri Lanka Institute of Information Technology (Semester 2, 2026).

This repository consolidates the design (Lab 3), usability evaluation (Lab 4), and technology/architecture decisions (Lab 5) for the FitFlow redesign, addressing the pain points identified in the FitFlow Case Study: a personalization gap, high-friction daily logging, weak progress motivation, and social isolation.

## Recommended Technology Stack

| Layer | Choice |
|---|---|
| Frontend | React Native (iOS/Android), companion React web app |
| Backend | Node.js + Express |
| Primary database | PostgreSQL (users, workouts, nutrition logs) |
| Real-time / social database | Firebase Firestore |
| Authentication | Firebase Authentication |
| AI microservice | Python/FastAPI + TensorFlow Lite (on-device) + cloud computer-vision model |
| Cache | Redis |

Full justification: [`docs/tech-stack-summary.md`](docs/tech-stack-summary.md) and [`docs/comparison-matrix.md`](docs/comparison-matrix.md).

## Architecture

See [`docs/architecture.png`](docs/architecture.png) for the high-level system architecture, and [`docs/dataflow.png`](docs/dataflow.png) for data flows across the three critical features (personalized workout plans, social sharing, nutrition tracking). Architecture Decision Records live in [`docs/adr/`](docs/adr).

## Project Structure

```
fitflow-redesign/
├── frontend/            # React Native app
├── backend/             # Node.js/Express services
├── ai-service/          # Python/FastAPI AI microservice
├── docs/                # Tech stack, comparison matrix, architecture, ADRs
├── .github/workflows/   # CI pipeline
├── .gitignore
└── README.md
```

## Getting Started

### Frontend
```bash
cd frontend
npm install
npx react-native run-ios     # or run-android
```

### Backend
```bash
cd backend
npm install
npm run dev
```

### AI Service
```bash
cd ai-service
pip install -r requirements.txt
uvicorn main:app --reload
```

## Related Work

- Lab 3 — FitFlow design direction, wireframes and clickable prototype
- Lab 4 — Usability testing plan, execution and findings
- Lab 5 — Technology comparison, weighted decision matrix, architecture and ADRs (this repository)

## Author

IT23655966 — Pankaji R K, Malabe Campus, Group 3.1
