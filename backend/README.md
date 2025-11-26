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
# Lint and check
ruff check app/

# Format code
ruff format app/

# Check formatting
ruff format --check app/

# Type check
mypy app/
```
