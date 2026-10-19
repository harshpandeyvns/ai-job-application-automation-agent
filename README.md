# AI-Powered Job Application Automation Agent

An n8n workflow that automates job discovery, resume customization, and job application tracking.

## Features

- **Job scraping:** Uses Apify to retrieve LinkedIn job postings from a user-provided search URL.
- **AI relevance screening:** Uses Google Gemini to assess whether each job matches the candidate's profile.
- **Resume customization:** Generates an ATS-friendly resume tailored to each relevant job description while instructing the LLM not to fabricate qualifications.
- **Google Docs integration:** Creates and updates a tailored resume document for each relevant job.
- **Google Sheets integration:** Records job titles, company names, experience levels, posting dates, salary information, job descriptions, resume links, and application links.

## Workflow

Manual Trigger → Job Search URL → Apify Job Scraper → Loop Through Jobs → Retrieve Resume → Gemini Relevance Screening → Filter → Gemini Resume Customization → Google Docs → Google Sheets

## Technologies

- n8n
- Apify
- Google Gemini
- Google Docs
- Google Sheets
- JSON and workflow automation

## Setup

1. Run n8n and import the workflow JSON.
2. Configure your Apify, Google Docs, Google Sheets, and Gemini credentials in n8n.
3. Replace the placeholder resume and spreadsheet IDs with your own resources.
4. Configure the job-search URL and required scraper inputs.
5. Test the workflow with a small number of job postings.

## Security

The published workflow uses dummy LinkedIn cookie values and redacted resource identifiers. Configure authentication securely before running it. Never commit session cookies, API keys, OAuth tokens, or private resume data.

## Deployment

Developed and tested as a locally running n8n workflow using Docker. It is not presented as a publicly hosted service.
