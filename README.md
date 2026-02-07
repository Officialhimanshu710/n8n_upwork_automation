# Upwork Automation Workflow (n8n)

This repository contains an enhanced n8n workflow that scrapes Upwork job listings, scores them using AI (Llama3-70b via Groq), and saves high-value leads to Airtable.

## 🚀 Features
- **Automated Scheduling:** Runs every 8 hours.
- **AI Scoring:** Analyzes jobs for "Automation" skills (n8n, Python, Docker) vs. "Manual" work.
- **Smart Filtering:** Automatically blocks low-value "Data Entry" jobs before AI processing.
- **Error Handling:** Includes auto-retry logic for API rate limits.

## 🛠️ Setup Instructions

### 1. Prerequisites
- [Docker](https://www.docker.com/) installed.
- n8n installed via Docker:
  ```bash
  docker run -it --rm --name n8n -p 5678:5678 -v ~/.n8n:/home/node/.n8n n8nio/n8n
  ```

### 2. Import Workflow

1. Open n8n (http://localhost:5678).

2. Go to Workflows > Import.

3. Upload the Upwork-Automation.json file from this repository.

### 3. Configure Credentials
You must set up the following credentials in n8n:

- Groq API: For the Llama3 model.

- Airtable Personal Access Token: For database access.

### 📂 Project Structure
- Upwork-Automation.json: The main workflow file.

- REPORT.md: Details on issues fixed and enhancements.

  ---

