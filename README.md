Anika-AI

AI-Powered Expense Management, OCR Bill Splitting & Financial
Intelligence Platform

Anika-AI is a full-stack AI-powered expense management platform that
helps users scan bills, extract expense information using OCR and NLP,
split expenses among participants, calculate settlements, track
spending, and generate financial insights.

The project is designed as a production-style application using a
React + TypeScript frontend, Flask/Python AI backend, Node.js/Express
services, SQLite database, and machine-learning components.

🚀 Key Features

🧾 AI Bill OCR & Understanding

Upload bills as images or PDFs

OCR-based text extraction

Automatic merchant detection

Automatic amount and item extraction

Tax/GST detection

Multi-bill processing

Structured JSON output from OCR

OCR error handling and retry/fallback flow

👥 Smart Expense Splitting

Add multiple participants

Select the person who paid

Equal split

Percentage-based split

Custom amount split

Itemized split

Automatic validation of split amounts

Automatic settlement calculation

Clear "who owes whom" results

🤖 AI & Machine Learning

NLP-based entity extraction

Expense category prediction

TF-IDF based text features

Machine-learning classification

Synthetic training-data generation

Model evaluation using:

Accuracy

Precision

Recall

F1-score

Confusion matrix

spaCy and regex-based entity recognition

AI-generated financial insights

📊 Financial Dashboard

Total expenses

Monthly spending

Category-wise spending

Spending trends

Budget tracking

Pending settlements

Recent activity

Expense analytics

Interactive charts

💬 AI Financial Assistant

Natural-language expense queries

Expense-related explanations

Financial insights

Budget-related suggestions

Conversational expense workflows

🛒 Smart Buy

Product recommendation workflow

Budget-aware recommendations

AI-assisted purchase analysis

📤 Export

PDF reports

CSV data

Text reports

Expense summaries

🔐 Authentication & Security

User registration/login

Session-based authentication

Protected API routes

Password hashing

Environment-variable based secrets

CORS configuration

Secure database access

🛠️ Tech Stack

Frontend

React

TypeScript

Vite

Tailwind CSS

Lucide React

Recharts

Zustand

React Markdown

jsPDF

Backend

Python

Flask

Flask-CORS

Flask-Login

Flask-SQLAlchemy

REST APIs

Server/API Layer

Node.js

Express

TypeScript

TSX

CORS

Helmet

dotenv

AI / Machine Learning

Google Gemini API

OpenAI API integration

scikit-learn

spaCy

pandas

NumPy

TF-IDF

Logistic Regression / LinearSVC

Regex-based NLP

Database

SQLite

SQLAlchemy

better-sqlite3

Development Tools

Git

GitHub

VS Code

Antigravity

Python virtual environment

npm

🏗️ System Architecture

                        ┌──────────────────────┐
                        │      React UI        │
                        │ React + TypeScript   │
                        │ Tailwind + Vite      │
                        └──────────┬───────────┘
                                   │
                                   ▼
                        ┌──────────────────────┐
                        │ Node.js / Express    │
                        │ API & Server Layer   │
                        └──────────┬───────────┘
                                   │
                     ┌─────────────┴─────────────┐
                     │                           │
                     ▼                           ▼
          ┌──────────────────┐        ┌──────────────────┐
          │   Flask Backend  │        │ SQLite Database  │
          │ Python + AI/ML   │        │ User/Expense     │
          └────────┬─────────┘        │ Data/Settlements │
                   │                  └──────────────────┘
          ┌────────┴────────────┐
          │                     │
          ▼                     ▼
   ┌──────────────┐     ┌────────────────┐
   │ OCR Pipeline │     │ ML/NLP Engine  │
   │ Gemini/OCR   │     │ spaCy/sklearn  │
   └──────────────┘     └────────────────┘

📁 Project Structure

anika-ai/
│
├── src/
│   ├── components/
│   ├── pages/
│   ├── hooks/
│   ├── services/
│   ├── store/
│   ├── types/
│   ├── utils/
│   └── App.tsx
│
├── backend/
│   ├── models/
│   ├── services/
│   ├── utils/
│   ├── config.py
│   ├── extensions.py
│   ├── nlp_entity_model.py
│   ├── ocr_bill_understanding.py
│   ├── smart_buy_recommendation.py
│   └── train_category_model.py
│
├── server/
│   ├── routes/
│   ├── services/
│   ├── db.ts
│   ├── index.ts
│   └── utils.ts
│
├── uploads/
│
├── tests/
│
├── .env.example
├── .gitignore
├── package.json
├── requirements.txt
├── tsconfig.json
├── vite.config.ts
├── README.md
└── LICENSE

⚙️ Installation

1. Clone the Repository

git clone https://github.com/GUTHACHAITANYA/anika-ai.git
cd anika-ai

2. Install Frontend / Node Dependencies

npm install

3. Create Python Virtual Environment

Windows

python -m venv .venv
.venv\Scripts\activate

macOS / Linux

python3 -m venv .venv
source .venv/bin/activate

4. Install Python Dependencies

pip install -r requirements.txt

If requirements.txt is not available, install the core dependencies:

pip install flask flask-cors flask-login flask-sqlalchemy python-dotenv pandas numpy scikit-learn spacy pillow requests

🔑 Environment Variables

Create a .env file in the project root.

Example:

FLASK_SECRET_KEY=your_secret_key

GEMINI_API_KEY=your_gemini_api_key

OPENAI_API_KEY=your_openai_api_key

DATABASE_URL=sqlite:///anika.db

FLASK_ENV=development

Never commit .env or API keys to GitHub.

Add the following to .gitignore:

.env
.venv/
__pycache__/
*.pyc
*.db
uploads/*
node_modules/
dist/

▶️ Running the Project

Start the Node/React Application

npm run dev

The Vite development server normally runs on a local URL such as:

http://localhost:5173

Start the Flask AI Backend

Activate the virtual environment first:

.venv\Scripts\activate

Then run the Flask application according to the backend entry point
configured in the project.

Example:

python app.py

The Flask API normally runs on:

http://127.0.0.1:5000

Make sure you run commands from the correct project root. The
directory containing package.json should be used for npm commands,
and the directory containing the Flask entry point should be used for
Python commands.

🧠 Machine Learning Pipeline

Anika-AI uses machine learning to classify and understand expense
descriptions.

Raw Expense Data
       │
       ▼
Data Cleaning
       │
       ▼
Text Preprocessing
       │
       ▼
TF-IDF Vectorization
       │
       ▼
Train/Test Split
       │
       ▼
ML Classifier
       │
       ▼
Model Evaluation
       │
       ▼
Saved Model + Vectorizer
       │
       ▼
Real-Time Expense Category Prediction

Example Categories

Food
Travel
Shopping
Entertainment
Bills
Utilities
Healthcare
Education
Fuel
Other

📚 NLP Pipeline

Expense text is processed using a combination of:

Regex

spaCy

Tokenization

Entity extraction

Pattern matching

Text classification

Example input:

Mohan paid 450 for dinner

Possible structured output:

{
  "person": "Mohan",
  "amount": 450,
  "category": "Food",
  "description": "dinner"
}

🧾 OCR Processing Flow

Upload Image / PDF
        │
        ▼
File Validation
        │
        ▼
OCR Processing
        │
        ▼
Raw Text Extraction
        │
        ▼
Merchant / Item / Amount Detection
        │
        ▼
Tax / GST Detection
        │
        ▼
Structured Expense JSON
        │
        ▼
User Review
        │
        ▼
Expense Splitting

The application should validate OCR output before saving it to the
database.

👥 Expense Splitting

Anika-AI supports multiple splitting strategies.

Equal Split

Example:

Total = ₹1200
People = 4

Each person = ₹300

Percentage Split

Person A = 50%
Person B = 30%
Person C = 20%

The percentages must total:

100%

Custom Split

Users can directly specify how much each participant owes.

Itemized Split

Individual items are assigned to participants.

Example:

Pizza → Chaitanya
Burger → Anika
Drinks → Chaitanya + Anika

The settlement engine validates that the final participant amounts match
the total expense.

💰 Settlement Engine

Settlement calculations are handled deterministically by the application
rather than relying on an LLM for arithmetic.

Example:

Total Expense: ₹1000

Chaitanya paid: ₹1000
Anika owes: ₹500
Rahul owes: ₹500

Result:

Anika → Chaitanya ₹500
Rahul → Chaitanya ₹500

For financial calculations, integer cents/paise or decimal-safe
arithmetic should be used to avoid floating-point rounding problems.

📊 Dashboard

The dashboard provides:

Total spending

Monthly expenses

Category distribution

Spending trends

Budget utilization

Pending settlements

Recent transactions

OCR history

Financial insights

Charts are implemented using:

Recharts

💬 AI Financial Assistant

The conversational assistant can help users understand their expenses.

Example:

User:
How much did I spend on food this month?

Possible response:

You spent ₹4,850 on food this month.

Other supported workflows can include:

Show my largest expense
How much do people owe me?
Analyze my spending
Which category is increasing?
Create a budget
Explain this expense

🛒 Smart Buy

Smart Buy analyzes a user's purchase requirement and budget.

Example:

Find a phone under ₹25,000

The system can use:

Budget

User requirement

Product attributes

Recommendation logic

AI-assisted analysis

to produce relevant purchase recommendations.

🗄️ Database

SQLite is used for local development and persistence.

Typical entities include:

User
Expense
ExpenseItem
Participant
Split
Settlement
Budget
Category
OCRHistory
ActivityLog

The database should maintain relationships between users, expenses,
participants, and settlements.

🔌 API Overview

Example API groups:

Authentication

POST /api/auth/register
POST /api/auth/login
POST /api/auth/logout
GET  /api/auth/me

Expenses

POST /api/expenses
GET  /api/expenses
GET  /api/expenses/:id
DELETE /api/expenses/:id

OCR

POST /api/ocr/analyze
POST /api/ocr/multi-bill
GET  /api/ocr/history

Participants

POST /api/expenses/:id/participants
GET  /api/expenses/:id/participants

Splitting

POST /api/split/equal
POST /api/split/percentage
POST /api/split/custom
POST /api/split/itemized

Dashboard

GET /api/dashboard/summary
GET /api/dashboard/categories
GET /api/dashboard/trends

Keep the actual route names synchronized with the implementation.

🧪 Testing

The project should include tests covering:

Authentication

OCR validation

Expense creation

Participant management

Equal splitting

Percentage splitting

Custom splitting

Itemized splitting

Settlement calculations

ML prediction

API validation

Database operations

Error handling

Run frontend type checking:

npm run lint

Run Python tests if configured:

pytest

🔒 Security

Important security practices:

Never expose API keys in frontend code

Store secrets in .env

Hash user passwords

Validate uploaded files

Restrict allowed file types

Limit upload sizes

Validate API inputs

Protect authenticated routes

Use CORS carefully

Avoid returning raw server tracebacks

Sanitize user-generated content

Keep sensitive configuration outside Git

🐛 Error Handling

Anika-AI should provide user-friendly errors for:

Invalid file
Unsupported file type
OCR failure
AI service unavailable
Invalid split
Participant missing
Authentication failure
Database error
API timeout
Invalid API response

Instead of exposing:

Traceback ...
SERVER_ERROR_STATUS_500

the frontend should display a meaningful message such as:

We couldn't analyze this bill right now.
Please try again or upload a clearer image.

Detailed errors should be logged on the server side.

🎯 Project Workflow

Login
  │
  ▼
Dashboard
  │
  ├── Upload Bill
  │       │
  │       ▼
  │      OCR
  │       │
  │       ▼
  │   Review Expense
  │       │
  │       ▼
  │  Add Participants
  │       │
  │       ▼
  │ Select Split Strategy
  │       │
  │       ▼
  │ Calculate Settlement
  │       │
  │       ▼
  │ Final Review
  │       │
  │       ▼
  │ Save Expense
  │       │
  │       ▼
  └── Dashboard Analytics

📈 Future Enhancements

Planned improvements include:

Voice-based expense logging

UPI payment integration

Real-time collaborative expenses

Cloud synchronization

AI fraud detection

Predictive budgeting

Expense forecasting

Mobile application

Firebase authentication

Advanced ML personalization

Improved OCR accuracy

Multi-language expense recognition

🏆 Project Goals

Anika-AI aims to demonstrate practical experience in:

Full-stack development

Python backend development

REST API development

Machine Learning

NLP

OCR

Data Analytics

Database design

AI integration

Financial data processing

Dashboard development

Software testing

Production-oriented application architecture

👨‍💻 Author

GUTHA CHAITANYA

B.Tech --- Computer Science & Engineering

GitHub:

https://github.com/GUTHACHAITANYA

📄 License

This project is intended for educational, portfolio, and demonstration
purposes.

Add an appropriate open-source license such as MIT if you decide to
distribute the project publicly.

⭐ Support

If you find this project useful, consider giving the repository a ⭐ on
GitHub.
