# 🧠 WebCraft AI – Intelligent Website Builder
<br/>
WebCraft AI is a full-stack PERN-based AI website builder that enables users to design, generate, and customize complete websites using artificial intelligence through a modern and responsive web interface. Built with React.js, Node.js, Express.js, and PostgreSQL (Neon) and powered by Prisma ORM, OpenRouter AI, and Stripe payment integration, the application allows users to create AI-generated web projects, manage them efficiently, and unlock premium features through secure online payments.
<br/>

 ## 🌐 Live Demo(DEPLOYED):<br/>
https://weblify-web-psi.vercel.app/
 <br/>

## 🌟 Key Features

<br/>
• AI-powered website generation using OpenRouter models
<br/>
• Prompt-based real-time code and layout creation
<br/>
• Project-based dashboard for managing generated websites
<br/>
• PostgreSQL (Neon) database integration with Prisma ORM
<br/>
• Secure online payments and premium feature access via Stripe
<br/>
• Dynamic template rendering and website customization
<br/>
• Fully responsive and performance-optimized user interface
<br/>
• Scalable RESTful backend built with Node.js and Express
<br/>

## ⚙️ Tech Stack

<br/>
Frontend: React.js (Vite), JavaScript (JSX), Tailwind CSS
<br/>
Backend: Node.js, Express.js
<br/>
Database: PostgreSQL (Neon) with Prisma ORM
<br/>
AI Integration: OpenRouter (Free AI API)
<br/>
Payments: Stripe (secure checkout & subscriptions)
<br/>
Deployement: Vercel
<br/>
Architecture: PERN stack, RESTful APIs
<br/>

## 🧩  Installation & Setup

 1.Sync Neon Database with Prisma  Navigate to the server folder and run the following commands:
```bash
npm install
npx prisma migrate dev --name init
npx prisma generate
```

2. Environment Variables on server side
<br/>
Create a `.env` file inside the server folder with the following variables: 

```bash
NODE_ENV = "development"

TRUSTED_ORIGINS="http://localhost:5173"

# Neon Database Url
DATABASE_URL="------Neon_Database_Url------"

# Better Auth
BETTER_AUTH_SECRET=6jLKNKZaH22s95i60GbxHz5UtpazAluK
BETTER_AUTH_URL='http://localhost:3000'

# OpenRouter API Key
AI_API_KEY='-----AI_API_KEY------'

# Stripe API Keys
STRIPE_SECRET_KEY="------Stripe_Secret_Key------"
STRIPE_WEBHOOK_SECRET='------Stripe_Webhook_Secret------'


```
3. Environment Variables on client side
<br/>
Create a `.env` file inside the client folder with the following variables: 

```bash
VITE_BASEURL='http://localhost:3000'
```

4.Run the following commands in  server folder to run it:
```bash
npm run server
```
5.Start to Run the following commands in client folder::
```bash
npm install
npm run dev
```

## 📝 Prerequisites <br/><br/>

• Node.js (v18 or higher recommended) <br/>
• npm or yarn package manager <br/>
• PostgreSQL account (Neon) <br/>
• OpenRouter account for AI integration <br/>
• Stripe account for payments <br/>
• Vercel account for deployment <br/>
• Modern web browser (Chrome / Edge / Firefox) <br/>

## ⚡ Dependencies <br/><br/>

### 🖌 Frontend <br/>

- `@daveyplate/better-auth-ui` : `^3.2.13` <br/>
- `@tailwindcss/vite` : `^4.1.17` <br/>
- `axios` : `^1.13.2` <br/>
- `better-auth` : `^1.4.5` <br/>
- `class-variance-authority` : `^0.7.1` <br/>
- `clsx` : `^2.1.1` <br/>
- `lucide-react` : `^0.555.0` <br/>
- `react` : `^19.2.0` <br/>
- `react-dom` : `^19.2.0` <br/>
- `react-router-dom` : `^7.9.6` <br/>
- `sonner` : `^2.0.7` <br/>
- `tailwind-merge` : `^3.4.0` <br/>
- `tailwindcss` : `^4.1.17` <br/>

### 🖥 Backend <br/>

- `@prisma/adapter-pg` : `^7.1.0` <br/>
- `@prisma/client` : `^7.1.0` <br/>
- `better-auth` : `^1.4.5` <br/>
- `cors` : `^2.8.5` <br/>
- `dotenv` : `^17.2.3` <br/>
- `express` : `^5.2.1` <br/>
- `openai` : `^6.10.0` <br/>
- `pg` : `^8.16.3` <br/>
- `stripe` : `^20.0.0` <br/>

### Development Tools <br/>

- `nodemon` : `^3.1.7` <br/>

## 🔄 Project Flow <br/><br/>

1. User Registration & Login <br/>
Users sign up or log in using secure authentication (Better Auth / Clerk) <br/><br/>

2. AI Website Prompt <br/>
Users provide prompts or inputs describing the website they want to generate <br/><br/>

3. Website Generation <br/>
The AI (via OpenRouter) generates website code, layouts, and content dynamically <br/><br/>

4. Project Management <br/>
Generated websites are saved in the user’s dashboard for editing, previewing, or deploying <br/><br/>

5. Payment & Premium Features <br/>
Users can unlock advanced templates or features via Stripe payment gateway <br/>

## 🔌 API Endpoints <br/><br/>

### Authentication <br/>
Authentication is handled via Better Auth / Clerk. <br/>
No custom login/register endpoints are implemented. <br/><br/>

### Projects / Websites <br/>
- GET `/api/projects` – Get all AI-generated websites <br/>
- GET `/api/projects/:id` – Get details of a specific website <br/>
- POST `/api/projects` – Create a new AI-generated website <br/><br/>

### Payments <br/>
- POST `/api/payment/checkout` – Initiate Stripe payment session for premium features <br/>
- GET `/api/payment/history` – View payment history / invoices <br/><br/>

### AI Generation <br/>
- POST `/api/ai/generate` – Generate website code and layout from user prompt <br/>
- GET `/api/ai/status/:id` – Check status of a website generation request <br/>

## 🧪 Testing <br/><br/>

- Test authentication flows (signup & login) <br/>
- Verify AI website generation requests and project creation <br/>
- Test Stripe payments using test keys <br/>
- Check protected routes for role-based access <br/>
- Validate API responses using Postman or similar tools <br/>

## 🛠️ Troubleshooting <br/><br/>

### Server Issues <br/>
- Ensure Neon DATABASE_URL is correct in `.env` <br/>
- Check if server port is already in use <br/><br/>

### Authentication Issues <br/>
- Verify Better Auth / Clerk API keys <br/>
- Check allowed origins in authentication dashboard <br/><br/>

### Payment Issues <br/>
- Use Stripe test keys for local testing <br/>
- Confirm webhook secrets are correct <br/><br/>

### Frontend Issues <br/>
- Run `npm install` before starting the client <br/>
- Ensure backend server is running <br/>

## 📈 Future Enhancements <br/><br/>
- Advanced AI templates and layouts <br/>
- Project versioning and collaboration features <br/>
- Enhanced payment workflows and subscriptions <br/>
- Deployment automation to Vercel or custom domains <br/>

## 🤝 Contributing <br/><br/>
Contributions are currently not accepted for this project. <br/>
This repository is maintained as a complete full-stack project for learning, portfolio, and demonstration purposes. <br/>

 ## 📄  License <br/>
This project is licensed under the MIT License. <br/><br/>

## 💡 Acknowledgements <br/><br/>
- Better Auth / Clerk for authentication and user management <br/>
- Stripe for secure payment processing <br/>
- Neon for PostgreSQL database services <br/>
- OpenRouter for AI-powered website generation <br/>
- React & Node.js open-source community <br/>


# React + TypeScript + Vite

This template provides a minimal setup to get React working in Vite with HMR and some ESLint rules.

Currently, two official plugins are available:

- [@vitejs/plugin-react](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react) uses [Babel](https://babeljs.io/) (or [oxc](https://oxc.rs) when used in [rolldown-vite](https://vite.dev/guide/rolldown)) for Fast Refresh
- [@vitejs/plugin-react-swc](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react-swc) uses [SWC](https://swc.rs/) for Fast Refresh

## React Compiler

The React Compiler is not enabled on this template because of its impact on dev & build performances. To add it, see [this documentation](https://react.dev/learn/react-compiler/installation).

## Expanding the ESLint configuration

If you are developing a production application, we recommend updating the configuration to enable type-aware lint rules:

```js
export default defineConfig([
  globalIgnores(['dist']),
  {
    files: ['**/*.{ts,tsx}'],
    extends: [
      // Other configs...

      // Remove tseslint.configs.recommended and replace with this
      tseslint.configs.recommendedTypeChecked,
      // Alternatively, use this for stricter rules
      tseslint.configs.strictTypeChecked,
      // Optionally, add this for stylistic rules
      tseslint.configs.stylisticTypeChecked,

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

```js
// eslint.config.js
import reactX from 'eslint-plugin-react-x'
import reactDom from 'eslint-plugin-react-dom'

export default defineConfig([
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
```
