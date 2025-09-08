 
# React + TypeScript + Vite

This template provides a minimal setup to get React working in Vite with HMR and some ESLint rules.

Currently, two official plugins are available:

- [@vitejs/plugin-react](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react) uses [Babel](https://babeljs.io/) for Fast Refresh
- [@vitejs/plugin-react-swc](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react-swc) uses [SWC](https://swc.rs/) for Fast Refresh

## Expanding the ESLint configuration

If you are developing a production application, we recommend updating the configuration to enable type-aware lint rules:

```js
export default tseslint.config([
  globalIgnores(['dist']),
  {
    files: ['**/*.{ts,tsx}'],
    extends: [
      // Other configs...

      // Remove tseslint.configs.recommended and replace with this
      ...tseslint.configs.recommendedTypeChecked,
      // Alternatively, use this for stricter rules
      ...tseslint.configs.strictTypeChecked,
      // Optionally, add this for stylistic rules
      ...tseslint.configs.stylisticTypeChecked,

      // Other configs...
    ],
    languageOptions: {
      parserOptions: {
        project: ['./tsconfig.node.json', './tsconfig.app.json'],
        tsconfigRootDir: import.meta.dirname,
      },
      // other options...
    },
  },
])
```

You can also install [eslint-plugin-react-x](https://github.com/Rel1cx/eslint-react/tree/main/packages/plugins/eslint-plugin-react-x) and [eslint-plugin-react-dom](https://github.com/Rel1cx/eslint-react/tree/main/packages/plugins/eslint-plugin-react-dom) for React-specific lint rules:

js
// eslint.config.js
import reactX from 'eslint-plugin-react-x'
import reactDom from 'eslint-plugin-react-dom'

export default tseslint.config([
  globalIgnores(['dist']),
  {
    files: ['**/*.{ts,tsx}'],
    extends: [
      // Other configs...
      // Enable lint rules for React
      reactX.configs['recommended-typescript'],
      // Enable lint rules for React DOM
      reactDom.configs.recommended,
    ],
    languageOptions: {
      parserOptions: {
        project: ['./tsconfig.node.json', './tsconfig.app.json'],
        tsconfigRootDir: import.meta.dirname,
      },
      // other options...
    },
  },
])


# ai-recipe-generator
AI-powered recipe generator web app built with React, AWS Amplify, and Amazon Bedrock (Claude 3 Sonnet). Users enter ingredients and get creative recipe suggestions instantly.
# 🍳 AI Recipe Generator

An AI-powered recipe generator web application built with **React + TypeScript (Vite)**, **AWS Amplify**, and **Amazon Bedrock (Claude 3 Sonnet)**.  

Users can enter a list of ingredients, and the app will generate delicious recipe ideas based on the input.

---

## 🚀 Features
- React + TypeScript frontend (Vite)
- Serverless backend with **AWS Amplify Gen 2**
- AI-generated recipes using **Amazon Bedrock (Claude 3 Sonnet)**
- Authentication and hosting with Amplify
- Deployed via GitHub → Amplify CI/CD

---

## 🛠️ Setup & Development

### Prerequisites
- Node.js (v18 or newer recommended)
- NPM or Yarn
- AWS commercial account with Bedrock access
- Amplify CLI (`npm install -g @aws-amplify/cli`)

### 1. Clone this repository
```bash
git clone https://github.com/<Achini-gf>/ai-recipe-generator.git
cd ai-recipe-generator
 8b11ec32b1bfb38f37a4eaf490f2a02ddf2bfbd7
