# CampusGuard — Smart Campus Security & Guard Co-Pilot (Frontend)

<div align="center">

![React](https://img.shields.io/badge/React-19.3-61DAFB?style=for-the-badge&logo=react&logoColor=black)
![Vite](https://img.shields.io/badge/Vite-8.3-646CFF?style=for-the-badge&logo=vite&logoColor=white)
![Tesseract.js](https://img.shields.io/badge/ANPR_OCR-Tesseract_LSTM-5C2D91?style=for-the-badge)
![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)
![Build](https://img.shields.io/badge/Build-Passing-brightgreen?style=for-the-badge)

**An AI-powered, real-time security management, ANPR gate kiosk, and digital guard co-pilot ecosystem designed for modern educational campuses and gated enterprises.**

[Live Demo](#quick-start) • [Features](#key-modules--features) • [Installation](#quick-start) • [Contributing](#team-contribution-guide) • [API Configuration](#backend-integration)

</div>

---

## 📋 Table of Contents
- [Overview](#overview)
- [Key Modules & Features](#key-modules--features)
- [Tech Stack](#tech-stack)
- [Directory Structure](#directory-structure)
- [Quick Start](#quick-start)
- [Backend Integration](#backend-integration)
- [Available NPM Scripts](#available-npm-scripts)
- [Team Contribution Guide (Fork & PR Workflow)](#team-contribution-guide)

---

## 🛡️ Overview

**CampusGuard Frontend** provides an ultra-responsive, zero-latency digital dashboard for security guards, gatekeepers, campus administrators, and visiting guests. Built with modern React 19 and Vite, it delivers state-of-the-art Automatic Number Plate Recognition (ANPR), QR-based self-service visitor passes, multi-tenant administrative controls, automated barrier gate triggers, and multilingual voice notifications.

---

## ⚡ Key Modules & Features

| Module | Route / Page | Description |
| :--- | :--- | :--- |
| **ANPR License Plate Scanner** | `/#vehicles` | Multi-ROI adaptive OCR detecting Indian license plates (cars, commercial buses, tractors, scooties) with zero-delay barrier automation. |
| **Security Gate Kiosk** | `/#gate-kiosk` | Real-time entry/exit tracking, live vehicle monitoring, and biometric check-in. |
| **Visitor Self-Pass Portal** | `/#self-pass` | Dynamic QR code generation, guest photo capture, and digital pass verification. |
| **Student Out-Pass System** | `/#out-pass` | Digital leave request validation, hostel out-pass scanning, and gate pass verification. |
| **Guard Co-Pilot Radar** | `/#copilot` | AI situational awareness co-pilot, night-patrol radar, and incident defection. |
| **Duty Attendance & Shift Handover** | `/#shifts` / `/#duty` | Biometric shift handover logs, equipment checklists, and guard patrol checkpoints. |
| **Campus Emergency SOS** | `/#emergency` | One-touch emergency campus sirens, lockdown actuators, and multi-channel SMS dispatcher. |
| **Admin & Multi-Tenant Dashboard** | `/#admin` / `/#tenant` | Role-based security analytics, daily occupancy statistics, and audit logs. |

---

## 🛠️ Tech Stack

- **Framework:** React 19.3 (Functional components & hooks)
- **Bundler & Dev Server:** Vite 8.3
- **Computer Vision & OCR:** Tesseract.js (LSTM Neural Network with Multi-ROI slicing)
- **Styling:** Modular Responsive CSS Design System (Custom Dark/Light Themes, Glassmorphism)
- **Icons:** Lucide React (`lucide-react`)
- **QR Generation:** `qrcode`
- **Testing:** Playwright E2E Suite (`@playwright/test`)
- **Linting:** Oxlint (`oxlint`)

---

## 📁 Directory Structure

```text
campusguard-frontend/
├── public/                  # Static assets, audio notifications & sample ANPR media
│   ├── images/              # Demonstration sample vehicle photos
│   └── favicon.svg          # Application icon
├── src/
│   ├── assets/              # Logos and SVG vector graphics
│   ├── components/          # Reusable UI components (Navbar, Sidebar, Modals, QR Generator)
│   ├── context/             # Authentication & tenant state management (AuthContext.jsx)
│   ├── hooks/               # Custom hooks (Speech recognition, audio synthesizer)
│   ├── pages/               # Primary application modules & route views
│   │   ├── VehiclesManager.jsx    # ANPR Number Plate Scanner & Fleet Tracker
│   │   ├── GateKiosk.jsx          # Live Security Gate Station
│   │   ├── VisitorPassManager.jsx # Guest & Contractor Passes
│   │   ├── AdminDashboard.jsx     # Security Operations Center
│   │   ├── ShiftHandoverManager.jsx # Digital Duty Handover
│   │   └── EmergencySOS.jsx       # Campus Alert Dispatcher
│   ├── services/            # Axios REST API client & backend connection layer
│   ├── utils/               # Voice command parsers, date helpers, color tokens
│   ├── App.jsx              # Main router & layout controller
│   ├── main.jsx             # React DOM entry point
│   └── index.css            # Core design system & theme variables
├── .env.example             # Template for local environment variables
├── package.json             # NPM dependencies and scripts
└── vite.config.js           # Vite configuration & dev server proxy
```

---

## 🚀 Quick Start

### Prerequisites
- **Node.js:** `v18.x` or higher
- **NPM:** `v9.x` or higher

### 1. Clone the Repository
```bash
git clone https://github.com/ajithaganesan02-pixel/campusguard-frontend.git
cd campusguard-frontend
```

### 2. Install Dependencies
```bash
npm install
```

### 3. Configure Environment
Copy `.env.example` to `.env`:
```bash
cp .env.example .env
```

### 4. Run Development Server
```bash
npm run dev
```
Open **[http://localhost:5173/](http://localhost:5173/)** in your browser.

---

## 🔌 Backend Integration

This frontend communicates with the **[CampusGuard Backend](https://github.com/ajithaganesan02-pixel/campusguard-backend)** (FastAPI service).
- **Default API URL:** `http://localhost:8080/api/v1`
- Configure in `.env`:
  ```env
  VITE_API_BASE_URL=http://localhost:8080/api/v1
  ```

---

## 📜 Available NPM Scripts

| Command | Description |
| :--- | :--- |
| `npm run dev` | Starts Vite local development server on port 5173 with HMR |
| `npm run build` | Compiles optimized production bundle into `dist/` |
| `npm run preview` | Previews the production build locally |
| `npm run lint` | Runs Oxlint linter for code quality checks |
| `npm run test:e2e` | Runs Playwright end-to-end automated tests |

---

## 🤝 Team Contribution Guide (Fork & PR Workflow)

We follow the standard GitHub Forking & Pull Request model:

1. **Fork** this repository to your personal GitHub account.
2. **Clone** your fork locally:
   ```bash
   git clone https://github.com/<your-username>/campusguard-frontend.git
   cd campusguard-frontend
   ```
3. Add the upstream remote:
   ```bash
   git remote add upstream https://github.com/ajithaganesan02-pixel/campusguard-frontend.git
   ```
4. Create a dedicated feature branch:
   ```bash
   git checkout -b feature/your-feature-name
   ```
5. Commit your changes with descriptive messages:
   ```bash
   git commit -m "feat(ui): add new visitor pass print preview"
   ```
6. Push to your fork:
   ```bash
   git push origin feature/your-feature-name
   ```
7. Open a **Pull Request (PR)** targeting the `develop` branch of `ajithaganesan02-pixel/campusguard-frontend`.

---

## 📄 License
This project is licensed under the MIT License.
