# FitFlow Redesign

Full-stack redesign of the **FitFlow fitness application**, developed for **IT3060 — Human Computer Interaction** at the **Sri Lanka Institute of Information Technology (SLIIT), Semester 2 — 2026**.

This repository contains the design, usability evaluation, technology decisions, architecture, and implementation of the FitFlow redesign. The project focuses on addressing key usability problems identified in the original FitFlow case study, including **limited personalization, high-friction daily logging, weak progress motivation, and social isolation**.

## Project Objectives

The FitFlow redesign aims to provide a more personalized, motivating, and user-friendly fitness experience through:

* Personalized workout recommendations
* Simplified daily fitness and nutrition logging
* Improved progress tracking and motivation
* Social interaction and community features
* AI-assisted fitness features
* Cross-platform mobile and web experiences

## Key Features

### Personalized Workout Plans

Provides personalized workout recommendations based on user information, fitness goals, preferences, and activity data.

### Easy Daily Logging

Reduces the effort required to record workouts, nutrition, and other fitness-related activities.

### Progress Tracking

Provides users with meaningful progress information to help them understand their fitness journey and stay motivated.

### Social Sharing

Allows users to share fitness achievements and interact with other users through social features.

### Nutrition Tracking

Enables users to record and monitor their nutrition and related health information.

### AI-Assisted Features

Uses AI technologies to support fitness-related functionality, including computer-vision-based features and personalized recommendations.

## Technology Stack

| Layer                       | Technology              |
| --------------------------- | ----------------------- |
| Mobile Frontend             | React Native            |
| Web Frontend                | React                   |
| Backend                     | Node.js + Express       |
| Primary Database            | PostgreSQL              |
| Real-time / Social Database | Firebase Firestore      |
| Authentication              | Firebase Authentication |
| AI Service                  | Python + FastAPI        |
| On-device AI                | TensorFlow Lite         |
| Cloud AI                    | Computer Vision Model   |
| Cache                       | Redis                   |

The technology stack was selected through a structured technology comparison and decision-making process documented in the project documentation.

## System Architecture

The FitFlow system follows a **full-stack, service-oriented architecture** consisting of mobile and web clients, backend services, databases, authentication services, caching, and AI services.

### Main Components

* **React Native Application** — Provides the primary mobile experience for Android and iOS.
* **React Web Application** — Provides a companion web interface.
* **Node.js + Express Backend** — Handles APIs, business logic, and communication between application components.
* **PostgreSQL** — Stores structured data such as users, workouts, and nutrition logs.
* **Firebase Firestore** — Supports real-time and social-related data.
* **Firebase Authentication** — Provides user authentication and account management.
* **Python/FastAPI AI Service** — Provides AI-related backend functionality.
* **TensorFlow Lite** — Supports selected on-device AI functionality.
* **Redis** — Provides caching to improve application performance.

## Architecture Documentation

The repository includes documentation covering the system architecture and major data flows.

* `docs/architecture.png` — High-level system architecture
* `docs/dataflow.png` — Data flows for critical system features
* `docs/tech-stack-summary.md` — Technology stack summary and justification
* `docs/comparison-matrix.md` — Technology comparison and weighted decision matrix
* `docs/adr/` — Architecture Decision Records

### Critical Data Flows

The architecture documentation describes data flows for:

1. **Personalized Workout Plans**
2. **Social Sharing**
3. **Nutrition Tracking**

## Project Structure

```text
fitflow-redesign/
├── frontend/             # React Native mobile application
├── backend/              # Node.js and Express backend services
├── ai-service/           # Python/FastAPI AI microservice
├── docs/                 # Project documentation and architecture
│   ├── architecture.png
│   ├── dataflow.png
│   ├── tech-stack-summary.md
│   ├── comparison-matrix.md
│   └── adr/              # Architecture Decision Records
├── .github/
│   └── workflows/        # CI/CD workflows
├── .gitignore
└── README.md
```

## Getting Started

### Prerequisites

Make sure the following tools are installed before running the project:

* Node.js
* npm
* React Native development environment
* Python
* pip
* PostgreSQL
* Redis
* Firebase project configuration

### Frontend

Navigate to the frontend directory and install the dependencies:

```bash
cd frontend
npm install
```

Run the application on iOS:

```bash
npx react-native run-ios
```

Or run it on Android:

```bash
npx react-native run-android
```

### Backend

Navigate to the backend directory:

```bash
cd backend
npm install
npm run dev
```

The Node.js/Express backend will start in development mode.

### AI Service

Navigate to the AI service:

```bash
cd ai-service
pip install -r requirements.txt
```

Start the FastAPI development server:

```bash
uvicorn main:app --reload
```

## Environment Configuration

Create the required environment configuration files for the frontend, backend, AI service, Firebase, PostgreSQL, and Redis.

Example backend configuration:

```env
PORT=5000
DATABASE_URL=your_postgresql_connection_string
REDIS_URL=your_redis_connection_string
```

> Do not commit passwords, API keys, Firebase credentials, or other sensitive information to GitHub.

## HCI Design Process

The FitFlow redesign was developed as part of the HCI coursework through multiple stages.

### Lab 3 — Design

The design phase focused on:

* Identifying user problems
* Defining the redesign direction
* Creating wireframes
* Developing the user interface concept
* Creating a clickable prototype

### Lab 4 — Usability Evaluation

The usability evaluation phase focused on:

* Preparing a usability testing plan
* Conducting usability testing
* Observing user interactions
* Identifying usability issues
* Analysing user feedback
* Documenting usability findings

### Lab 5 — Technology & Architecture

The technology and architecture phase focused on:

* Comparing alternative technologies
* Preparing a weighted decision matrix
* Selecting the technology stack
* Designing the system architecture
* Defining system data flows
* Creating Architecture Decision Records (ADRs)

## Related Work

* **Lab 3** — FitFlow design direction, wireframes, and clickable prototype
* **Lab 4** — Usability testing plan, execution, and findings
* **Lab 5** — Technology comparison, weighted decision matrix, architecture, and ADRs

## Future Improvements

Potential future improvements include:

* Advanced AI-based workout recommendations
* More detailed fitness analytics
* Improved social and community features
* Additional wearable-device integrations
* Personalized nutrition recommendations
* Enhanced real-time collaboration
* Expanded AI computer-vision capabilities

## Academic Information

**Module:** IT3060 — Human Computer Interaction
**Institution:** Sri Lanka Institute of Information Technology (SLIIT)
**Semester:** Semester 2 — 2026
**Campus:** Malabe Campus
**Group:** 2.1
**Student ID:** IT23715110

## Author

**IT23715110**

Sri Lanka Institute of Information Technology
Malabe Campus — Group 2.1
