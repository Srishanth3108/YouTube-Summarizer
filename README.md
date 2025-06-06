Gemini-Powered YouTube Summarizer
Project Documentation

Overview
This project is a Gemini-powered web application that generates concise summaries from YouTube videos.

In a world where video content can be long and time-consuming to watch, this tool helps users extract key insights quickly and efficiently by summarizing YouTube videos through the Gemini API.

Key Features
Summarizes any YouTube video via URL input

Utilizes Gemini API through Google Vertex AI

Simple and intuitive web interface

Backend built with Python (Flask)

Deployed serverlessly on Google Cloud Run

Responsive and fast

Project Structure
pgsql
Copy
Edit
amazing-gemini-app/
├── templates/
│   └── index.html       --> Frontend UI
├── app.py               --> Backend Flask app and Gemini integration
├── requirements.txt     --> Python dependencies
├── README.md            --> Project documentation (this document)
└── venv/                --> Virtual environment (local, optional)
Prerequisites
Before starting, ensure you have the following:

✅ Google Cloud Project with billing enabled
✅ Enabled APIs:

Vertex AI API

Cloud Run Admin API

Cloud Build API

Cloud Resource Manager API

✅ Python 3.8 or higher
✅ Basic knowledge of:

Python & Flask

HTML & CSS

Gemini API and Google Gen AI SDK
✅ Google Cloud CLI (gcloud) installed and configured

Technologies Used
Component	Technology
Frontend	HTML, CSS
Backend	Python, Flask
AI Service	Gemini API via Google Gen AI SDK
Deployment	Google Cloud Run

Installation & Setup
1️⃣ Clone the Repository
bash
Copy
Edit
git clone https://github.com/yourusername/amazing-gemini-app.git
cd amazing-gemini-app
2️⃣ Setup Virtual Environment
bash
Copy
Edit
python -m venv venv
source venv/bin/activate
3️⃣ Install Dependencies
bash
Copy
Edit
pip install -r requirements.txt
4️⃣ Configure Project ID
In app.py, replace:

python
Copy
Edit
PROJECT_ID = "REPLACE_WITH_YOUR_PROJECT_ID"
with your actual Google Cloud Project ID.

Running Locally
To run the application locally:

bash
Copy
Edit
python app.py
Access the app via http://localhost:8080 in your browser.

Deploying to Google Cloud Run
1️⃣ Configure Project
bash
Copy
Edit
gcloud config set project [PROJECT_ID]
2️⃣ Deploy Application
bash
Copy
Edit
gcloud run deploy --source .
During deployment:

Service name: youtube-summarizer or any name

Region: us-central1

Allow unauthenticated access: Yes

After successful deployment, you'll receive a URL like:

arduino
Copy
Edit
https://youtube-summarizer-xxxxx.a.run.app
You can now share this link — the app is live and publicly accessible.

How to Use
Open the deployed app in a browser.

Enter a YouTube video URL.

(Optional) Select model type and enter an additional prompt.

Click Summarize.

The summary will be generated and displayed.

Challenge Ideas
Implement a feature to upload local video files and summarize them.

Add authentication (Google OAuth, Firebase Auth) for secure access.

Improve UI with better CSS or add JS animations.

Support multiple Gemini models and allow model selection dynamically.

Optimize the response with caching to avoid repeated API calls for the same video.

Clean Up
To avoid extra costs:

Go to the Google Cloud Console → Cloud Run → Delete your deployed service.
Or

Delete your Google Cloud Project entirely if no longer needed.

Acknowledgements
This project is based on the Google Codelab:
"Build a Gemini-Powered YouTube Summarizer"
Authors: Thu Ya Kyaw and Alvin Prayuda Juniarta Dwiyantoro

License
Content: Creative Commons Attribution 4.0 License

Code Samples: Apache 2.0 License
