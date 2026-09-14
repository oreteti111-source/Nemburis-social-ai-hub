# NEMBURIS SOCIAL AI HUB — FULL EDITION

A phone-first, self-hostable social-media growth and lead-management platform for NEMBURIS SAFARI TOURS.<link rel="stylesheet" href="style.css">

## Included
- Responsive PWA dashboard
- Content planner and calendar
- AI content generator with a no-training template engine
- Optional local AI through Ollama
- Image/video prompt studio
- PDF lead-magnet generator
- Public inquiry form
- Lead/CRM pipeline
- Follow-up tasks
- Analytics dashboard
- Content library
- Social account connection architecture
- Official-API connector configuration screen
- SQLite database
- FastAPI backend
- Docker deployment
- Export/import backup
- No paid AI API is required for the core application

## Important
This is a complete self-hostable application, but external social networks do not permit a generic application to publish to every network without registering an application and obtaining the required permissions/tokens. The included connector layer is designed for official APIs and does not fake successful publishing.

## Run
### Docker
1. Install Docker.
2. In this folder run:
   `docker compose up --build`
3. Open:
   `http://localhost:8000`

### Without Docker
1. Python 3.11+
2. `pip install -r requirements.txt`
3. `uvicorn backend.main:app --host 0.0.0.0 --port 8000`
4. Open `http://localhost:8000`

## Optional local AI
Install Ollama on a computer/server and set:
`OLLAMA_URL=http://localhost:11434`
`OLLAMA_MODEL=llama3.2`

The app falls back to its built-in generator if Ollama is unavailable.

## Phone
The interface is responsive and can be installed as a PWA from a supported browser once hosted over HTTPS.

## Production checklist
- Set a strong `SECRET_KEY`
- Put the app behind HTTPS
- Configure social API credentials
- Configure a production database if desired
- Configure WhatsApp Business Cloud API if automated messaging is needed
- Configure SMTP if email notifications are needed
