# ADR-0001: Frontend Framework Selection

**Status:** Accepted

## Context

FitFlow needs a single team to ship consistent iOS, Android and (ideally) web experiences quickly, support AI/computer-vision features, and handle real-time social updates, while keeping long-term maintenance cost low for a mid-sized team. Four options were evaluated: Flutter, React Native, Kotlin Multiplatform, and Swift/SwiftUI.

## Decision

**React Native** is selected as the primary frontend framework.

## Rationale

- Single JavaScript/TypeScript codebase across iOS and Android, extendable to web through a companion React app sharing components and design tokens.
- Largest ecosystem of the cross-platform options for FitFlow's specific needs: real-time libraries (Firebase, Socket.IO), animation libraries for the progress-ring/hero-card UI validated in Lab 3, and TensorFlow Lite / ML Kit bridges for on-device AI.
- Lower hiring/onboarding cost — JavaScript/React skills are more widely available than Dart (Flutter) or a native Kotlin/Swift specialist pairing.
- Performance is near-native and sufficient for FitFlow's UI complexity (cards, charts, camera capture).
- Swift/SwiftUI was eliminated immediately (Apple-only, no Android/web path). Kotlin Multiplatform only shares business logic, still requiring two separately-built native UIs, which conflicts with the project's speed and cost constraints.

## Consequences

- The team standardizes on JavaScript/TypeScript across the mobile frontend and (via Node.js) the backend, reducing context-switching.
- A small amount of platform-specific native code may still be used inside the React Native app where needed (e.g. camera/ML performance tuning), without abandoning the shared codebase.
- Full scoring detail: see `docs/comparison-matrix.md` and Activity 1 of the main Lab 5 report.
