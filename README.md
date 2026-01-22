# college-whatsapp-notification-automation
An n8n-based automation to categorize college WhatsApp messages into Holidays, Jobs, Class Schedules, and General updates.

#College WhatsApp Notification Automation (n8n)
#🧠 Problem Statement
College WhatsApp groups generate a high volume of messages daily. Important updates related to holidays, placements, and class schedule changes often get missed.

#💡 Solution
This project uses n8n workflow automation to automatically read incoming WhatsApp messages, analyze their content, categorize them, and store them in Google Sheets for easy access.

🔄 Workflow Logic

WhatsApp Trigger
   ↓
Edit Fields
   ↓
IF (contains "holiday")
   → Google Sheet: Holidays
ELSE
   IF (contains "job")
      → Google Sheet: Jobs
   ELSE
      IF (contains "class")
         → Google Sheet: Class Schedule
      ELSE
         → Google Sheet: General
         
🛠️ Tools & Technologies
n8n (Workflow Automation)

WhatsApp Business Cloud API
Google Sheets
Conditional Logic (IF nodes)

👩‍💻 Author
Rabiya Tahseen
B.Tech CSE Student
