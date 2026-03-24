# Mental Health Check-in Bot

## Solution Summary
Production-ready domain application.

This Phase-2 implementation is a domain-ready, deployable web application for **Education** workflows.

## Core Capabilities
- Responsive dashboard with KPI cards and recent activity table
- Domain record lifecycle with full CRUD (web + API)
- Dynamic schema fields tailored to this use case
- Status pipeline: `planned, in-session, assessment, mastered`
- Docker + Gunicorn deployment assets, CI checks, and Pytest tests

## Domain Model
- Primary entity: **Mental Health Learning Unit**
- Collection: **Mental Health Learning Units**
- Dynamic fields:
- Learner Group (`learner_group` / text)
- Difficulty (1-5) (`difficulty` / number)
- Material Notes (`material_notes` / textarea)

## Operational Workflow
1. Plan curriculum
2. Run learning activity
3. Assess outcomes
4. Track mastery

## API
- `GET /api/health`
- `GET /api/schema`
- `GET /api/records`
- `POST /api/records`
- `GET /api/metrics`

## Run Locally
```bash
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
python app.py
```

## Docker Run
```bash
docker compose up --build
```

## Proof of Concept
- [proof-of-concept.md](proof-of-concept.md)
- [proof/demo-output.txt](proof/demo-output.txt)
- [proof/ui-preview.svg](proof/ui-preview.svg)
