# 📧 Cold Mail Generator

An AI-powered Streamlit application that scrapes job postings from a given URL, extracts job descriptions using LLaMA3 (via Groq), and generates personalized cold emails for outreach. It also matches job requirements with a portfolio of project links to include in the email.
## 🚀 Features

- 🌐 Scrapes job data from any career page using `WebBaseLoader`
- 🧠 Uses **LLaMA3-70B** model (via Groq) for:
  - Extracting job roles, skills, and descriptions
  - Writing personalized cold emails
- 📁 Matches job-required skills with a portfolio (CSV file)
- 📬 Outputs clean, professional cold emails using your project links


## 🧩 Tech Stack

- **Frontend**: [Streamlit](https://streamlit.io)
- **LLM**: LLaMA3 (via [Groq API](https://console.groq.com/))
- **NLP Framework**: [LangChain](https://www.langchain.com/)
- **Data Storage**: [ChromaDB](https://docs.trychroma.com/)
- **Environment Handling**: `dotenv`
- **Vector Search**: Chroma with UUID-based indexing
## 📦 Requirements

Install using [Poetry](https://python-poetry.org/):

```bash
poetry install

⚙️ Setup
1. Create .env file:

GROQ_API_KEY=your_groq_api_key_here

▶️ Run the App

poetry run streamlit run app/main.py

🧠 How It Works
You enter a job URL

The app scrapes and cleans the page content

LLaMA3 (via Groq) extracts:

Job Role

Skills

Experience

Description

It matches the skills with your portfolio

It generates a cold email using that info and your links

```
##🧪 Example Output

Subject: Helping Nike Automate Talent Acquisition Using AI

Hi [Hiring Manager],

I'm Mohan, BDE at AtliQ – an AI consulting firm. I noticed your need for a Machine Learning Engineer experienced in NLP and deployment...

Here are some of our projects that match your vision:
- https://yourportfolio.com/chatbot
- https://yourportfolio.com/eda

Looking forward to discussing how we can collaborate.

Warm regards,  
Mohan  
BDE, AtliQ

## Screenshots

![App Screenshot][def]

![App Screenshot][def2]

[def]: ./assets/mail1.png

[def2]: ./assets/mail2.png