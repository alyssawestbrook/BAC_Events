# BAC_Events
A Python-based web application that scrapes campus calender event data and uses an API for integration. Includes Docker, GitHub Actions, and deployment through Google Cloud Run.

## Project Status
- MVP complete: scraper + DB + Dockerization
- CI: GitHub Actions
- Deployed: Google Cloud Run (URL: TBA)

## Setup (local)
1. Clone repo:
git clone https://github.com/yourusername/your-project-name.git
cd your-project-name

2. Install dependencies:
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate
pip install -r requirements.txt

3. Run app:
python app/main.py

## Docker
docker build -t your-project-name .
docker run -p 8080:8080 your-project-name

## Google Cloud Deployment
gcloud auth login
gcloud config set project YOUR_PROJECT_ID
gcloud builds submit --tag gcr.io/YOUR_PROJECT_ID/your-project-name
gcloud run deploy your-project-name --image gcr.io/YOUR_PROJECT_ID/your-project-name --platform managed --region us-central1 --allow-unauthenticated

## AI usage log
- ChatGPT: regex design
- GitHub Copilot: function suggestions