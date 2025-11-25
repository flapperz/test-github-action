# Backend (FastAPI)

A simple FastAPI backend application.

## Setup

```bash
pip install -r requirements-dev.txt
```

## Run

```bash
uvicorn app.main:app --reload
```

## Linting

```bash
# Format code
black app/

# Check formatting
black --check app/

# Lint
flake8 app/

# Type check
mypy app/
```
