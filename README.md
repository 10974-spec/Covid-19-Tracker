🌍 COVID-19 Global Data Tracker (Django)
A real-time dashboard tracking COVID-19 cases worldwide using Django, Python, and public APIs.

Demo Screenshot

📌 Features
✔ Live Data Fetching – Pulls data from disease.sh API
✔ Interactive Charts – Visualizes cases, deaths, recoveries
✔ Country Filtering – Search and filter by country
✔ Auto-Update – Scheduled data refreshes (Celery/cron)
✔ Responsive UI – Works on desktop & mobile

⚙️ Tech Stack
Backend: Django (Python)




APIs: disease.sh

🚀 Installation
1. Clone the Repository

<code>git clone https://github.com/10974-spec/Covid-19-Tracker.git
cd covid19-tracker</code>
2. Set Up Virtual Environment

<code>python -m venv venv
source venv/bin/activate  # Linux/Mac
venv\Scripts\activate     # Windows</code>
3. Install Dependencies

<code>pip install -r requirements.txt</code>
4. Run Migrations

<code>python manage.py migrate</code>
5. Fetch Initial Data
bash
python manage.py fetch_covid_data  # Custom command (if available)
6. Start the Server

<code>python manage.py runserver</code>
Visit → http://127.0.0.1:8000

📂 Project Structure
covid19-tracker/
├── tracker/               # Django app
│   ├── models.py          # Country, CovidData models
│   ├── views.py           # Dashboard & API views
│   ├── management/        # Custom commands (data fetching)
│   └── templates/         # HTML + Chart.js
├── covid_tracker/         # Django project settings
└── requirements.txt       # Dependencies
🔧 Custom Commands
To update data manually:


<code>python manage.py fetch_covid_data</code>
(Set up a Celery task or cron job for auto-updates.)

📊 Data Sources
disease.sh – Free COVID-19 API

