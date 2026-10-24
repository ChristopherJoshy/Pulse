<div align="center">
  <img width="100%" src="https://capsule-render.vercel.app/api?type=waving&color=0:042f2e,35:0f766e,70:14b8a6,100:facc15&height=190&section=header&text=Pulse&fontSize=68&fontColor=ffffff&animation=twinkling&fontAlignY=36&desc=Campus%20events%20from%20discovery%20to%20verified%20points.&descAlignY=58&descSize=16" alt="Pulse animated header" />

  <p>
    <img src="https://img.shields.io/badge/Client-React%20%2B%20Vite-61DAFB?style=for-the-badge&logo=react&logoColor=111827" alt="React and Vite" />
    <img src="https://img.shields.io/badge/API-Express%20%2B%20TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white" alt="Express and TypeScript" />
    <img src="https://img.shields.io/badge/Data-MongoDB-47A248?style=for-the-badge&logo=mongodb&logoColor=white" alt="MongoDB" />
    <a href="LICENSE"><img src="https://img.shields.io/badge/License-MIT-FDE68A?style=for-the-badge" alt="MIT License" /></a>
  </p>
</div>

## 🎓 What it does

Pulse is a campus opportunity and activity-points platform prototype. Students browse events, register, and present a QR code for attendance; organizers and advisors have separate views for verification and approval. The backend records events, registrations, notifications, discussions, and points-ledger entries.

<p align="center"><img src="copetitions%20%20data/comp1.jpeg" width="46%" alt="Example campus event poster" /></p>

## 🔄 Event lifecycle

```mermaid
flowchart LR
  A[Organizer posts event] --> B[Student discovers and registers]
  B --> C[QR attendance check]
  C --> D[Advisor review]
  D --> E[Points ledger update]
```

## 🧰 Stack

| Layer | Tools |
|---|---|
| Frontend | React 18, Vite, TypeScript, Tailwind, Framer Motion |
| API | Express, TypeScript, Bun scripts |
| Database | MongoDB/Mongoose |
| QR and UI | `html5-qrcode`, `qrcode.react`, Lucide |
| Deploy config | `render.json` |

## 🚀 Run locally

Start the backend:

```bash
git clone https://github.com/ChristopherJoshy/Pulse.git
cd pulse/backend
bun install
Copy-Item .env.example .env  # PowerShell; use cp on macOS/Linux
bun run dev
```

Start the frontend separately:

```bash
cd pulse/frontend
npm install
npm run dev
```

Configure MongoDB and the frontend API URL locally. The repository includes seeded profiles and example event material.

## 🗂️ Layout

```text
frontend/             student, organizer and advisor screens
backend/src/          Express routes, controllers and MongoDB models
copetitions  data/    sample event poster assets
code-wiki.md          implementation notes
```

## ⚠️ Authentication is demo-only

The current UI intentionally allows role switching and profile creation for demonstration. The backend endpoints load seeded profiles and create profiles; this is **not production authentication or authorization**. Do not deploy this build with real student records, personal data, or activity-point decisions until authentication, server-side role checks, and audit controls are implemented and reviewed.

## 📄 License

MIT. See [`LICENSE`](LICENSE).