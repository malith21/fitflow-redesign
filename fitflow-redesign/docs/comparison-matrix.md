# FitFlow Technology Comparison Matrix

Full detail and scoring rationale: see `IT23655966_LAB5_HCI.docx`, Activity 3.

## Weighting (based on FitFlow project priorities)

| Criterion | Weight | Reason |
|---|---|---|
| Performance | 15% | Directly affects perceived app quality and the animations validated in Lab 3. |
| Scalability | 15% | Needed to support growth beyond the initial user base. |
| Development speed | 15% | Mid-sized team needs to ship the Lab 3 redesign on schedule. |
| Security / compliance | 15% | Health-adjacent data requires GDPR/CCPA-aligned handling (Case Study requirement). |
| Cost efficiency | 10% | Startup-stage budget constraints. |
| AI/ML integration | 10% | Core to the AI workout planner and computer-vision nutrition logging. |
| Real-time features | 10% | Needed for the Community Feed and notifications. |
| Maintainability | 5% | Lower priority than shipping speed for a first release. |
| Web compatibility | 5% | Nice-to-have; mobile is the primary platform. |

## Weighted Totals

### Frontend
| Option | Weighted Score (/5) | Outcome |
|---|---|---|
| React Native | 4.15 | **Recommended** |
| Flutter | 3.60 | Strong second |
| Kotlin Multiplatform | 3.55 | Shared logic only, not full UI |
| Swift/SwiftUI | 2.90 | Eliminated — Apple-only |

### Backend
| Option | Weighted Score (/5) | Outcome |
|---|---|---|
| Node.js / Express | 4.35 | **Recommended** |
| NestJS | 4.15 | Close second |
| Python / FastAPI | 3.85 | Used for the AI microservice instead |
| Go | 3.55 | Highest raw performance, steepest learning curve |

### Data & Auth
| Layer | Choice |
|---|---|
| Primary database | PostgreSQL |
| Real-time / social database | Firebase Firestore |
| Authentication | Firebase Authentication |

## Recommended Stack

**Frontend:** React Native  |  **Backend:** Node.js + Express  |  **Primary DB:** PostgreSQL  |  **Real-time/Social DB:** Firebase Firestore  |  **Auth:** Firebase Authentication  |  **AI:** Python/FastAPI microservice + TensorFlow Lite (on-device)

See the main report (Activity 3.1–3.3) for the full criterion-by-criterion scoring table.
