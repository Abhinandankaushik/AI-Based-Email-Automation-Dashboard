# ✉️ AI-Based Email Automation Dashboard

A full-stack web application designed for automating and personalizing email communication at scale. This platform enables staff or organizations to upload recipient data, generate AI-powered emails, schedule or send them instantly, and track engagement with real-time analytics.

---

## 🚀 Features

- 📥 Upload recipient data via CSV
- 🤖 Generate personalized emails using AI (Gemini API)
- ✍️ Preview, edit, and manage email templates
- 📊 Track email engagement (opens, clicks, RSVPs) via analytics dashboard
- 🕒 Schedule follow-up emails using cron jobs
- 📬 Send emails using SendGrid with delivery tracking

---

## 🏗️ System Architecture

**Frontend**  
- Built with **React.js** and **Tailwind CSS**
- Handles CSV upload (via PapaParse), template editing, email previews, and analytics display
- Uses `react-router-dom` for routing

**Backend**  
- Built with **Node.js** and **Express.js**
- Handles AI email generation, data management, scheduling, and API communication
- Integrates **Gemini API** using `p-limit` for rate-limited parallel requests

**Database**  
- **MongoDB Atlas** used for data storage
- Key collections:
  - `emailTemplates`: Editable and reusable templates
  - `recipients`: CSV-uploaded data with AI-generated emails
  - `emailLogs`: Tracks delivery and analytics data

**Email Service**  
- **SendGrid** integration for email delivery and tracking

**Scheduler**  
- **node-cron** used to automate follow-up and reminder emails

---

## 🧠 AI Integration

- Leverages **Gemini API** to generate dynamic, context-aware emails
- Personalization based on recipient data and selected templates
- Fallback logic in case of missing or invalid templates

---

## 📊 Analytics

- Real-time dashboard displaying:
  - Open rates
  - Click-through rates
  - RSVP responses
- Metrics fetched from SendGrid API and stored in MongoDB

---


## 🔮 Planned Enhancements

- Authentication and access control for admin users
- Retry logic for failed emails
- Regional language support for email content
- AI feedback loop to improve personalization quality
### 🔹 Dashboard View
![Dashboard Screenshot](./Dashboard%20Images/0.pdf)

### 🔹 Email Template Editor
![Template Editor](./Dashboard%20Images/1.pdf)

### 🔹 Analytics Dashboard
![Analytics View](./Dashboard%20Images/2.pdf)

