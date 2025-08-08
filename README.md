Web-App Link - https://hershield-2-yagl.onrender.com
HerShield - Women's Safety Application
A comprehensive web application designed to enhance women's safety through technology, providing emergency alerts, AI-powered assistance, and community support.

🌟 Features
🚨 Emergency SOS System
3-Click Activation: Prevents accidental activation
Automatic SMS: Sends emergency alerts to contacts
Location Tracking: Real-time location sharing
Audio Alerts: Siren sound during emergencies
🤖 AI Chatbot Assistant
Dynamic Q&A: Answers any question about safety, health, relationships
Context-Aware: Specialized in women's safety and empowerment
24/7 Support: Always available for assistance
📞 Emergency Contacts Management
Smart Validation: Phone number and data validation
Priority System: High, Medium, Low priority contacts
Edit/Delete: Full CRUD operations for contacts
Duplicate Prevention: Prevents duplicate entries
🛡️ Safety Features
Self-Defense Tutorials: Video tutorials and tips
Health & Wellness: Comprehensive health guidance
Community Support: Share experiences and connect
Latest Articles: Stay informed with safety news
🚀 Quick Start
Prerequisites
Python 3.11 or higher
pip (Python package installer)
Installation
Clone the repository

git clone <repository-url>
cd HerShield_Project1
Install dependencies

pip install -r requirements.txt
Run deployment script

python deploy.py
Set up environment variables

cp env_example.txt .env
# Edit .env file with your API keys
Run the application

python app.py
Access the application

Open your browser and go to http://localhost:5000
Register a new account
Add emergency contacts
Start using HerShield!
🔧 Configuration
Environment Variables
Create a .env file in the project root with the following variables:

# Flask Configuration
SECRET_KEY=your-secret-key-here
FLASK_ENV=production
FLASK_DEBUG=False

# Gemini AI Configuration
GEMINI_API_KEY=your-gemini-api-key-here

# Twilio Configuration (for SMS)
TWILIO_ACCOUNT_SID=your-twilio-account-sid
TWILIO_AUTH_TOKEN=your-twilio-auth-token
TWILIO_PHONE_NUMBER=your-twilio-phone-number

# Weather API Configuration
WEATHER_API_KEY=your-openweathermap-api-key
API Keys Setup
Gemini AI API

Visit Google AI Studio
Create a new API key
Add to GEMINI_API_KEY in .env
Twilio API (for SMS functionality)

Sign up at Twilio
Get Account SID and Auth Token
Get a Twilio phone number
Add to .env file
OpenWeatherMap API (for weather updates)

Sign up at OpenWeatherMap
Get API key
Add to WEATHER_API_KEY in .env
🌐 Deployment
Heroku Deployment
Install Heroku CLI

# Download from https://devcenter.heroku.com/articles/heroku-cli
Login to Heroku

heroku login
Create Heroku app

heroku create your-app-name
Set environment variables

heroku config:set SECRET_KEY=your-secret-key
heroku config:set GEMINI_API_KEY=your-gemini-key
heroku config:set TWILIO_ACCOUNT_SID=your-twilio-sid
heroku config:set TWILIO_AUTH_TOKEN=your-twilio-token
heroku config:set TWILIO_PHONE_NUMBER=your-twilio-number
heroku config:set WEATHER_API_KEY=your-weather-key
Deploy to Heroku

git add .
git commit -m "Deploy HerShield application"
git push heroku main
Railway Deployment
Connect to Railway

Visit Railway
Connect your GitHub repository
Set environment variables

Add all required environment variables in Railway dashboard
Deploy

Railway will automatically deploy your application
Vercel Deployment
Install Vercel CLI

npm i -g vercel
Deploy

vercel
📱 Usage Guide
For Users
Registration

Visit the application
Click "Get Started" or "Sign Up"
Fill in your details and create an account
Adding Emergency Contacts

Go to "Emergency Contacts" section
Add trusted contacts with their phone numbers
Set priority levels (High, Medium, Low)
Using SOS Feature

Click the SOS button 3 times quickly
System will automatically send SMS to all emergency contacts
Your location will be shared with them
AI Chatbot

Click the chatbot icon (🤖) on any page
Ask any question about safety, health, relationships, etc.
Get comprehensive, supportive answers
For Administrators
Monitor Alerts

Access /admin route to view all emergency alerts
Track user activity and emergency situations
Database Management

SQLite databases are stored in database/ folder
users.db contains user data and contacts
alerts.db contains emergency alerts
🛠️ Development
Project Structure
HerShield_Project1/
├── app.py                 # Main Flask application
├── deploy.py             # Deployment script
├── requirements.txt      # Python dependencies
├── Procfile             # Heroku deployment config
├── runtime.txt          # Python version specification
├── wsgi.py              # WSGI entry point
├── database/            # SQLite databases
│   ├── users.db
│   └── alerts.db
├── static/              # Static files
│   ├── css/
│   ├── images/
│   └── sounds/
├── templates/           # HTML templates
│   ├── dashboard.html
│   ├── chatbot.html
│   ├── emergency_contacts.html
│   └── ...
└── logs/               # Application logs
Running in Development Mode
export FLASK_ENV=development
export FLASK_DEBUG=True
python app.py
Running in Production Mode
gunicorn app:app --worker-class gevent --workers 4 --bind 0.0.0.0:8000
🔒 Security Features
Password Hashing: All passwords are securely hashed
Session Management: Secure session handling
Input Validation: Comprehensive input validation
SQL Injection Protection: Parameterized queries
XSS Protection: Template escaping
📊 Database Schema
Users Table
id: Primary key
name: User's full name
email: Unique email address
phone: Phone number
password: Hashed password
Emergency Contacts Table
id: Primary key
user_id: Foreign key to users
name: Contact name
phone: Contact phone number
relationship: Relationship type
priority: Priority level (1-3)
Alerts Table
id: Primary key
user_id: Foreign key to users
name: User name
location: GPS coordinates
timestamp: Alert timestamp
status: Alert status
priority: Alert priority
🤝 Contributing
Fork the repository
Create a feature branch
Make your changes
Test thoroughly
Submit a pull request
📄 License
This project is licensed under the MIT License - see the LICENSE file for details.

🆘 Support
For support and questions:

Create an issue in the repository
Contact the development team
Check the documentation
🙏 Acknowledgments
Google Gemini AI for intelligent chatbot responses
Twilio for SMS functionality
OpenWeatherMap for weather data
Bootstrap for UI components
Font Awesome for icons
Made with ❤️ for women's safety and empowerment
