# college-whatsapp-notification-automation
An n8n-based automation to categorize college WhatsApp messages into Holidays, Jobs, Class Schedules, and General updates.

#📌 College WhatsApp Notification Automation using n8n

#🔍 Overview

College communication heavily relies on WhatsApp groups for announcements related to holidays, placements, class schedules, and general updates. However, due to the high volume of daily messages, students often miss critical information.

This project proposes an automation-based solution using n8n that reads incoming WhatsApp messages, categorizes them intelligently, and stores them in a structured format for easy access.



❗ Problem Statement

College WhatsApp groups generate hundreds of messages

Important announcements get buried under casual chat

Students must scroll endlessly to find relevant updates

No centralized, categorized view of information exists



💡 Proposed Solution

This project builds an automated message classification system that:

Receives WhatsApp messages via API

Extracts the message content

Categorizes messages into meaningful groups:

🏖️ Holidays

💼 Jobs / Internships

🏫 Class Schedule Updates

ℹ️ General Information


Stores the categorized messages in Google Sheets

Enables students to quickly view only relevant updates



---

⚙️ System Architecture

WhatsApp Business Cloud
        ↓
   n8n WhatsApp Trigger
        ↓
   Message Text Extraction
        ↓
   Conditional Logic (IF nodes)
        ↓
 ┌───────────┬───────────┬──────────────┬───────────┐
 │ Holidays  │ Jobs      │ Class        │ General   │
 │ Sheet     │ Sheet     │ Schedule     │ Sheet     │
 └───────────┴───────────┴──────────────┴───────────┘


---

🔄 Workflow Logic

WhatsApp Trigger
   ↓
Edit Fields (extract message_text)
   ↓
IF (message contains "holiday")
   → Google Sheet: Holidays
ELSE
   IF (message contains "job" OR "internship")
      → Google Sheet: Jobs
   ELSE
      IF (message contains "class" OR "schedule")
         → Google Sheet: Class Schedule
      ELSE
         → Google Sheet: General


---

🧠 Key Features

📩 Automatic message ingestion

🧩 Keyword-based classification logic

📊 Structured storage in Google Sheets

⏱️ Timestamped records

🔁 Easily extendable to AI/ML classification in the future

🔒 Secure (no credentials stored in repository)



---

🛠️ Technology Stack

n8n – Workflow automation platform

WhatsApp Business Cloud API – Message ingestion

Google Sheets – Lightweight database

Conditional Logic (IF nodes) – Classification



---

📊 Google Sheets Data Structure

Each sheet follows the same structure:

TimeStamp	Category	Message

2026-01-22 16:35	Holiday	Tomorrow is a holiday due to festival


Sheets used:

Holidays

Jobs

Class Schedule

General



---

📂 Repository Structure

college-whatsapp-notification-automation/
│
├── README.md
├── screenshots/
│   └── (workflow & output images – to be added)
├── workflow/
│   └── n8n-workflow.json (placeholder)


---

🚧 Current Status

✅ Workflow logic completed

✅ Message categorization implemented

✅ Google Sheets integration working

⚠️ WhatsApp Business Cloud reconnection pending due to Meta security cooldown (temporary)


> No sensitive credentials or phone numbers are included in this repository.




---

🚀 Future Enhancements

🤖 AI-based text classification (NLP)

📱 Student dashboard / web portal

🔔 Automated notifications to students

📈 Analytics on announcement trends

🗂️ Admin moderation panel



---

🎓 Academic Relevance

This project demonstrates:

Practical use of automation tools

Real-world problem solving

Integration of APIs

Data organization and processing

Scalable system design



---

👩‍💻 Author

Rabiya Tahseen
B.Tech – Computer Science & Engineering


---

📜 Disclaimer

This project is developed for educational purposes only.
WhatsApp Business Cloud access is subject to Meta platform policies.
Google Sheets
Conditional Logic (IF nodes)

# 👩‍💻 Author
Rabiya Tahseen
B.Tech CSE Student
