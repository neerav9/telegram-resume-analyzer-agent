AI-Powered Resume–Job Matcher Bot (n8n + Gemini + Telegram)

This is an AI agent built using n8n, Gemini 2.5 Flash, and Telegram Bot API to help jobseekers instantly compare their resume with a job description and get personalized feedback.

It returns:

Match percentages for Skills, Experience, and Education

Reasoning behind the score

Actionable suggestions to improve the resume

One weak bullet rewritten using power verbs and metrics

Demo Screenshot:

User sends resume + job description PDF
Bot replies with detailed match + suggestions

<img width="945" height="910" alt="image" src="https://github.com/user-attachments/assets/0bfb260b-b445-4f16-8ed1-f30c2f7d926c" />


What’s New in v2.0:

Added section-wise scoring (Skills, Experience, Education)

Added overall reasoning logic

Added resume improvement suggestions

Integrated bullet point rewriting using LLM

Formatted response in clean markdown, perfect for Telegram & UI

View Prompt Used in Gemini: ./prompt-v2.md
See Sample Output: ./example-output.md

Tech Stack:

Tool	Purpose
n8n	Workflow automation
Gemini 2.5 Flash API	LLM for resume analysis
Telegram Bot API	User interaction
Markdown	Formatted output

How It Works:

User sends their resume and a job description as text or PDFs via Telegram.

n8n extracts the content and sends both to Gemini API with a custom prompt.

Gemini responds with:

Section-wise scores

Reasoning

Suggestions to improve

Rewritten bullet point

Bot replies back to the user with the entire report in markdown.

Files:

resume-agent-v2.json — Exported n8n workflow

prompt-v2.md — The optimized Gemini prompt

example-output.md — Sample result output

README.md — This file

To Use This:

Clone this Repo

bash
Copy
Edit
git clone https://github.com/your-username/resume-matching-bot.git
Import Workflow in n8n

Go to your n8n instance → Import → Select resume-agent-v2.json

Set Environment Variables

You’ll need:

Gemini API Key → Get from Google AI Studio

Telegram Bot Token → Create a bot via BotFather on Telegram

Run Your Workflow

Send a JD and Resume to your Telegram bot
Let the agent respond

Future Plans:

Add vector-based matching using ChromaDB or FAISS

Build a public UI with Streamlit or Gradio

Add multi-agent logic for keyword rewriting and tone coaching

Author:

Neerav Krishna Uppu
Building AI agents, automating workflows, and simplifying hiring.
Connect with me on LinkedIn: https://www.linkedin.com/in/neeravkrishna-uppu/
DM me if you'd like to deploy a similar bot for your company/team!

Tags:
n8n, Gemini, TelegramBot, ResumeMatching, AIProjects, LLMEngineering
