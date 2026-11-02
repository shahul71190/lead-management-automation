# Lead Management Automation System

An end-to-end lead management automation system built using **n8n, Lovable, Google Sheets, and Gmail**.

The project automates website inquiry collection, lead storage, personalized email communication, and email delivery status tracking.

## 🌐 Live Demo

**Website:** https://leadflow-inquiry-orchestrator.lovable.app

## 🎯 Problem Statement

Businesses often receive customer inquiries through website forms but manage them manually.

This can result in:
- Delayed responses to potential customers.
- Repetitive manual data entry.
- Lost or unorganized lead information.
- Difficulty tracking email delivery status.
- Additional administrative workload.

## 💡 Solution

This workflow automatically captures website inquiries, stores lead information in Google Sheets, sends personalized confirmation emails, and tracks email delivery status.

## ⚙️ Workflow Architecture

Website Form (Lovable)  
→ n8n Webhook  
→ Google Sheets (Append Lead)  
→ Gmail (Send Email)  
→ Google Sheets (Update Status)

**Email failure handling:**

Gmail Error Output  
→ Google Sheets (Update Status to Failed)

## 🔧 Technologies Used

- n8n — Workflow automation
- Lovable — Website and inquiry form
- Google Sheets — Lead database
- Gmail — Automated email communication
- Webhooks — Application integration
- JSON — Data exchange

## ✨ Key Features

- Website inquiry form integration.
- Automatic lead capture through webhook.
- Lead storage in Google Sheets.
- Automatic submission timestamp.
- Personalized confirmation emails.
- Email status tracking (`Pending`, `Sent`, `Failed`).
- Email sent timestamp.
- Error handling for failed email delivery.

## 📊 Lead Tracking Fields

| Field | Description |
|---|---|
| Lead ID | Unique lead reference |
| Name | Customer name |
| Email | Customer email |
| Company Name | Customer's company |
| Interested Service | Requested service |
| Message | Inquiry details |
| Submission Date | Lead submission timestamp |
| Email Status | Pending / Sent / Failed |
| Email Sent Time | Email sent timestamp |

## 🧪 Testing

The workflow was tested for:
- Successful webhook data reception.
- Google Sheets row insertion.
- Successful Gmail delivery.
- Successful `Sent` status update.
- Failed email handling and `Failed` status update.
- Production webhook submission.

## 👨‍💻 About This Project

Built as a practical business automation project to demonstrate how no-code workflow automation can reduce repetitive administrative work and improve lead response processes.

**Interested in implementing a similar automation for your business?**

Connect with me on LinkedIn and let's discuss your workflow automation requirements.
