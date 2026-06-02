# 🚑 Smart Ambulance Routing & Hospital Readiness AI

> **Save Lives Through Intelligent Dispatch**  
> An AI-powered emergency response system that routes ambulances intelligently—not just by distance, but by real-time hospital capacity, readiness, and resource availability.

[![React](https://img.shields.io/badge/React-18+-61DAFB?style=flat-square&logo=react)](https://react.dev)
[![TypeScript](https://img.shields.io/badge/TypeScript-5+-3178C6?style=flat-square&logo=typescript)](https://www.typescriptlang.org)
[![Vite](https://img.shields.io/badge/Vite-5+-646CFF?style=flat-square&logo=vite)](https://vitejs.dev)

---

## 🎯 Why This Matters

Every second counts in emergency response. Traditional ambulance routing uses distance alone—but what if the nearest hospital is overwhelmed?

**Smart Ambulance Routing fixes this** by:
- 🏥 **Real-time Hospital Status** - Monitor ICU capacity, bed availability, and emergency department load instantly
- 📊 **Predictive Analytics** - Forecast hospital overload before it happens
- 🚨 **Emergency Prioritization** - Match patient severity with hospital readiness
- ⚡ **Optimized Routes** - Route to the best available facility, not the closest
- 💾 **Data-Driven Decisions** - AI learns from historical patterns to improve routing

---

## ✨ Key Features

| Feature | Description |
|---------|-------------|
| 🗺️ **Smart Routing Engine** | AI algorithm considers distance, hospital capacity, specializations, and traffic |
| 🏗️ **Scalable Architecture** | Built with modern React + TypeScript for high-performance dashboards |
| 📡 **Real-time Integration** | Connects with hospital systems, GPS tracking, and emergency databases |
| 🤖 **ML-Powered Forecasting** | Predicts bed availability and emergency department wait times |
| 🎛️ **Interactive Dashboard** | Visual monitoring of ambulances, hospitals, and patient priority queues |
| 📱 **Responsive Design** | Works seamlessly on desktop, tablet, and mobile devices |

---

## 🚀 Quick Start

### Prerequisites
- **Node.js** 18+ ([Download](https://nodejs.org/))
- **npm** or **yarn** package manager
- Basic knowledge of React and TypeScript

### Installation

```bash
# 1️⃣ Clone the repository
git clone https://github.com/Sanskar81105/Smart-Ambulance-Routing-Hospital-Readiness-AI.git
cd Smart-Ambulance-Routing-Hospital-Readiness-AI

# 2️⃣ Install dependencies
npm install
# or with yarn
yarn install

# 3️⃣ Start the development server
npm run dev
# or
yarn dev
```

Open [http://localhost:5173](http://localhost:5173) in your browser to see the application.

---

## 🛠️ Project Setup

This project uses **React + TypeScript + Vite** for optimal development experience with fast refresh and type safety.

### Build & Deployment

```bash
# Build for production
npm run build

# Preview production build locally
npm run preview

# Lint your code
npm run lint
```

### Available Scripts

| Script | Description |
|--------|-------------|
| `npm run dev` | Start development server with HMR |
| `npm run build` | Create optimized production build |
| `npm run preview` | Preview production build locally |
| `npm run lint` | Run ESLint to check code quality |

---

## 🔧 Technology Stack

### Frontend Framework
- **React 18+** - UI library with hooks and concurrent features
- **TypeScript** - Type-safe JavaScript for robust code
- **Vite** - Lightning-fast build tool and dev server

### Build Tools & Plugins

We use two official React plugins for optimal development experience:

<details>
<summary><b>📦 @vitejs/plugin-react</b> (Default)</summary>

Uses [Babel](https://babeljs.io/) (or [oxc](https://oxc.rs) when used with rolldown-vite) for Fast Refresh and JSX compilation.

```bash
npm install @vitejs/plugin-react --save-dev
```

**Best for:** Projects requiring maximum compatibility and customization.

</details>

<details>
<summary><b>⚡ @vitejs/plugin-react-swc</b> (Faster Alternative)</summary>

Uses [SWC](https://swc.rs/) - a super-fast JavaScript compiler written in Rust for even quicker refresh cycles.

```bash
npm install @vitejs/plugin-react-swc --save-dev
```

**Best for:** Projects prioritizing build speed and performance.

</details>

---

## 🎨 Code Quality & Linting

### ESLint Configuration

For production applications, we recommend enabling **type-aware lint rules**:

```js
// eslint.config.js
import tseslint from 'typescript-eslint'
import { defineConfig, globalIgnores } from '@eslint/js'

export default defineConfig([
  globalIgnores(['dist']),
  {
    files: ['**/*.{ts,tsx}'],
    extends: [
      // Core TypeScript linting - choose one level:
      tseslint.configs.recommendedTypeChecked,    // ✅ Recommended
      // tseslint.configs.strictTypeChecked,       // 🔒 Stricter
      // tseslint.configs.stylisticTypeChecked,    // 🎨 With style rules
    ],
    languageOptions: {
      parserOptions: {
        project: ['./tsconfig.node.json', './tsconfig.app.json'],
        tsconfigRootDir: import.meta.dirname,
      },
    },
  },
])
```

### React-Specific Linting

Enhance your lint rules with React-focused plugins:

```js
// eslint.config.js
import reactX from 'eslint-plugin-react-x'
import reactDom from 'eslint-plugin-react-dom'

export default defineConfig([
  globalIgnores(['dist']),
  {
    files: ['**/*.{ts,tsx}'],
    extends: [
      reactX.configs['recommended-typescript'],  // React best practices
      reactDom.configs.recommended,               // React DOM rules
    ],
    languageOptions: {
      parserOptions: {
        project: ['./tsconfig.node.json', './tsconfig.app.json'],
        tsconfigRootDir: import.meta.dirname,
      },
    },
  },
])
```

**Installation:**
```bash
npm install --save-dev eslint-plugin-react-x eslint-plugin-react-dom
```

---

## 🧠 React Compiler (Advanced)

The React Compiler is **not enabled by default** due to potential impact on development and build performance. If you want to use it in a production setup:

```bash
npm install --save-dev babel-plugin-react-compiler
```

See the [official React Compiler documentation](https://react.dev/learn/react-compiler/installation) for detailed setup instructions.

---

## 📁 Project Structure

```
Smart-Ambulance-Routing-Hospital-Readiness-AI/
├── src/
│   ├── components/          # Reusable React components
│   ├── pages/              # Page-level components
│   ├── services/           # API and business logic
│   ├── hooks/              # Custom React hooks
│   ├── types/              # TypeScript type definitions
│   ├── utils/              # Utility functions
│   ├── App.tsx             # Main application component
│   └── main.tsx            # Application entry point
├── public/                 # Static assets
├── dist/                   # Production build output
├── vite.config.ts          # Vite configuration
├── tsconfig.json           # TypeScript configuration
├── eslint.config.js        # ESLint configuration
└── package.json            # Project dependencies
```

---

## 🤝 Contributing

We welcome contributions! Here's how to get involved:

1. **Fork** the repository
2. **Create** a feature branch (`git checkout -b feature/AmazingFeature`)
3. **Commit** your changes (`git commit -m 'Add AmazingFeature'`)
4. **Push** to the branch (`git push origin feature/AmazingFeature`)
5. **Open** a Pull Request

Please ensure your code follows our ESLint rules and includes appropriate TypeScript types.

---

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

---

## 💡 Need Help?

- 📖 [React Documentation](https://react.dev)
- ⚡ [Vite Guide](https://vitejs.dev)
- 🔷 [TypeScript Handbook](https://www.typescriptlang.org/docs/)
- 🚨 [Report an Issue](https://github.com/Sanskar81105/Smart-Ambulance-Routing-Hospital-Readiness-AI/issues)

---

## 🌟 Acknowledgments

Built with ❤️ to improve emergency response and save lives.

Made with [React](https://react.dev) ⚛️ + [TypeScript](https://www.typescriptlang.org) 🔷 + [Vite](https://vitejs.dev) ⚡
