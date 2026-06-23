💍 Matrimony (Rishtey)

A full-stack matrimonial web application built for the South Indian community. Users can browse profiles, send interests, chat with accepted connections, and manage their own profile — all in one place.

📸 Screenshots

Landing Page · Matches Dashboard · Profile View — Browse profiles on the homepage · Filter by religion, age, location · View detailed profile info

🚀 Tech Stack

LayerTechnologyFrontendReact 19, 
Vite 7, 
TypeScript 5.9StylingTailwind CSS 4, 
shadcn/ui, 
Framer MotionRoutingWouterBackendNode.js 22, 
Express 5DatabasePostgreSQL + Drizzle ORMValidationZod v4, 
drizzle-zodAPI CodegenOrval

⚙️ Prerequisites

Make sure you have these installed:


Node.js v22+
pnpm v11+ — install with npm install -g pnpm
PostgreSQL database URL — get a free one from Neon or Supabase


🛠️ Setup & Installation

Step 1 — Clone the repository:

bashgit clone https://github.com/puniths1011-png/Matrimony.git
cd Matrimony

Step 2 — Install dependencies:

bashpnpm install --ignore-scripts

Step 3 — Windows only — install missing native binaries:

powershellpnpm add @esbuild/win32-x64@0.27.3 @rollup/rollup-win32-x64-msvc lightningcss-win32-x64-msvc @tailwindcss/oxide-win32-x64-msvc --ignore-scripts -w

▶️ Running the Project

You need two terminals running at the same time.

Terminal 1 — Backend (API Server)

powershell# Windows
cd artifacts/api-server
$env:NODE_ENV="development"
node ./build.mjs

$env:DATABASE_URL="your_postgresql_url_here"
$env:PORT="5000"
node --enable-source-maps ./dist/index.mjs

bash# Mac / Linux
cd artifacts/api-server
NODE_ENV=development node ./build.mjs
DATABASE_URL="your_postgresql_url_here" PORT=5000 node --enable-source-maps ./dist/index.mjs

Terminal 2 — Frontend (React App)

powershell# Windows
cd artifacts/shaadi-app
$env:PORT="3000"
$env:BASE_PATH="/"
npx vite --host 0.0.0.0

bash# Mac / Linux
cd artifacts/shaadi-app
PORT=3000 BASE_PATH="/" npx vite --host 0.0.0.0

Open in browser

http://localhost:3000

✅ Quality

This is the stable, production-ready build of Matrimony. All known issues from earlier QA testing cycles have been fixed and verified, including:


Filters returning accurate, correctly matched results
All buttons and navigation actions working as intended
Live data reflected across the app instead of hardcoded placeholders
Form fields validating input correctly before submission


🧪 Useful Commands

bash# Full typecheck across all packages
pnpm run typecheck

# Build all packages
pnpm run build

# Regenerate API hooks from OpenAPI spec
pnpm --filter @workspace/api-spec run codegen

# Push DB schema to PostgreSQL
pnpm --filter @workspace/db run push

🤝 Contributing

Fork the repository
Create your branch: git checkout -b your-name-dev
Make your changes
Commit: git commit -m "describe your change"
Push: git push -u origin your-name-dev
Open a Pull Request to main


📄 License

MIT License — free to use and modify.
