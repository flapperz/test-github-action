# test-github-action

A testing repository for various GitHub Actions in a simple monorepo structure.

## Project Structure

```
.
├── backend/          # FastAPI backend application
│   ├── app/         # Application code
│   ├── requirements.txt
│   └── requirements-dev.txt
├── frontend/        # Vite React frontend application
│   ├── src/
│   ├── package.json
│   └── vite.config.js
└── .github/
    └── workflows/   # GitHub Actions workflows
```

## Backend (FastAPI)

The backend is a simple FastAPI application with:
- CORS middleware configured
- Health check endpoint
- Sample API endpoints

### Setup and Run

```bash
cd backend
pip install -r requirements-dev.txt
uvicorn app.main:app --reload
```

### Linting

```bash
cd backend
ruff check app/         # Lint
ruff format app/        # Format code
mypy app/               # Type check
```

## Frontend (Vite + React + TypeScript)

The frontend is a Vite React TypeScript application with:
- TypeScript for type safety
- ESLint for linting
- Prettier for code formatting
- Modern React setup

### Setup and Run

```bash
cd frontend
npm install
npm run dev
```

### Linting

```bash
cd frontend
npm run type-check     # Run TypeScript type check
npm run lint           # Run ESLint
npm run format:check   # Check formatting
npm run format         # Format code
```

## GitHub Actions Workflows

### 1. Backend Linting (`backend-lint.yml`)
- Runs on push/PR to main/develop branches
- Only triggers when backend files change
- Checks: Ruff linting and formatting, MyPy type checking

### 2. Frontend Linting (`frontend-lint.yml`)
- Runs on push/PR to main/develop branches
- Only triggers when frontend files change
- Checks: TypeScript type check, ESLint, Prettier formatting

### 3. GitHub Actions Quirk Tests (`quirk-tests.yml`)
Tests fundamental GitHub Actions features:
- **Matrix builds**: Tests across multiple OS and Node versions
- **Conditional execution**: Tests if conditions and event filtering
- **Artifacts**: Upload and download test
- **Caching**: Dependency caching test
- **Environment variables**: ENV vars and GitHub context
- **Job dependencies**: Output sharing between jobs

### 4. Webdev Essential CI/CD (`webdev-cicd.yml`)
Complete CI/CD pipeline:
- **Backend CI**: Linting, testing, artifact creation
- **Frontend CI**: Linting, building, artifact creation
- **Security Scan**: Trivy vulnerability scanning with SARIF upload
- **Integration Test**: Combines backend and frontend artifacts
- **Deploy**: Conditional deployment to production (main branch only)

## Development

1. Make changes to backend or frontend
2. Run local linting before committing
3. Push to a feature branch
4. Create a PR to trigger all workflows
5. Merge to main to trigger deployment workflow

## License

MIT