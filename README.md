# Admin Dashboard Console

A premium, responsive, dark-themed management dashboard console built with **Vue 3**, **TypeScript**, and **Vite**.

This dashboard integrates with the `api21` backend engine to provide system administrators with tools for session monitoring, environment variables configuration, and an interactive remote SSH web terminal.

---

## 🛠️ Technology Stack

- **Framework:** Vue 3 (Composition API with `<script setup>`)
- **Language:** TypeScript
- **Build Tool:** Vite
- **UI Components:** PrimeVue
- **Icons:** Lucide Vue Next & PrimeIcons
- **Web Terminal:** Xterm.js

---

## ⚙️ Configuration & Environment Variables

Create a `.env` (or `.env.local`) file in the project root:

```env
VITE_API_BASE_URL=http://localhost:8080/admin
```

- **`VITE_API_BASE_URL`**: Points to the base path of the admin endpoints in the backend server.

---

## 🚀 Getting Started

### 1. Install Dependencies
```bash
npm install
```

### 2. Run Locally (Development)
```bash
npm run dev
```

### 3. Build for Production
```bash
npm run build
```

### 4. Preview Production Build
```bash
npm run preview
```

---

## 📦 Automated Deployment (CI/CD)

The project includes a GitHub Actions CI/CD pipeline ([deploy.yml](.github/workflows/deploy.yml)) to build and deploy to Vercel on commits to the `main` branch.

### 🔑 Configuration

Configure the following secrets and variables in your GitHub repository:

#### 📂 GitHub Environment Variables (Variables)
Add under **Settings > Secrets and variables > Actions > Variables** (or under `production` Environment variables):

- `VITE_API_BASE_URL`: The production API server URL.

#### 🔒 GitHub Secrets
Add under **Settings > Secrets and variables > Actions > Secrets**:

- `VERCEL_TOKEN`: Your Vercel API Personal Access Token.
- `VERCEL_ORG_ID`: Your Vercel account or organization ID.
- `VERCEL_PROJECT_ID`: The project ID of your deployment target in Vercel.
