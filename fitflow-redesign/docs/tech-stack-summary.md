# FitFlow Technology Stack Summary

Full comparison and justification: see `IT23655966_LAB5_HCI.docx`, Activities 1–3.

## Recommended Stack

| Layer | Choice | Why |
|---|---|---|
| Frontend | React Native | Single codebase for iOS/Android, largest cross-platform ecosystem, strong real-time and AI-plugin support, matches team's JavaScript/React skills. |
| Backend | Node.js + Express | Keeps the stack in one language, mature real-time libraries, straightforward horizontal scaling for an I/O-bound API. |
| Primary database | PostgreSQL | Strong fit for structured, relational health data (users, workouts, nutrition logs); supports GDPR-style auditability. |
| Real-time / social database | Firebase Firestore | Native real-time sync for the Community Feed and notifications without building custom WebSocket infrastructure. |
| Authentication | Firebase Authentication | Native integration with React Native and Firestore; strong security defaults (MFA, token refresh); generous free tier. |
| AI microservice | Python/FastAPI + TensorFlow Lite (on-device) + cloud computer-vision model | Strongest ML ecosystem for recommendation and computer-vision models; on-device TensorFlow Lite supports offline personalization. |
| Cache | Redis | Reduces repeated PostgreSQL reads for hot data (today's plan, sessions); backs API Gateway rate limiting. |

## Eliminated Options and Why

- **Flutter** — strong contender, but React Native scored higher on ecosystem maturity for AI/ML and real-time features specific to FitFlow, and better matches the team's existing JavaScript skillset.
- **Kotlin Multiplatform** — only shares business logic, not UI; would still require building and maintaining two native UIs, conflicting with the project's speed/cost constraints.
- **Swift/SwiftUI** — Apple-only; cannot reach Android or web at all, immediately disqualifying it for FitFlow's cross-platform requirement.
- **MongoDB / DynamoDB (as primary DB)** — weaker fit than PostgreSQL for FitFlow's relational, health-adjacent data and progress-trend reporting queries.
- **AWS Cognito / Auth0 / Supabase Auth** — all viable, but Firebase Authentication was chosen for its tightest native integration with the chosen real-time database (Firestore) and the React Native client SDK.

See the weighted decision matrix in Activity 3 of the main report for full scoring detail.
