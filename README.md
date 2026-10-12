*Intuz — Your automation partner, one workflow at a time.*

<p align="center">
  <picture>
    <img alt="Banner Image" src="https://github.com/user-attachments/assets/210f97fc-0fce-404a-b647-7dfe1302cd37" />
  </picture>
</p>

[Intuz](https://www.intuz.com) helps organizations orchestrate AI, automation, and enterprise systems through scalable workflows. Our repository showcases proven implementations across healthcare, operations, customer support, document processing, sales, and back-office functions, enabling teams to accelerate automation initiatives without starting from scratch.

[N8N Creator](https://n8n.io/creators/intuz/) · [Workflow Automation](https://www.intuz.com/workflow-automation-services/) · [Custom AI Development](https://www.intuz.com/ai/) · [For Custom Workflow Automation](https://www.intuz.com/get-started/)

# Automate lead generation from Google Search & Maps to Google Sheets

This n8n template from Intuz provides a complete solution to automate on-demand lead generation.

It acts as a powerful scraping agent that takes a simple chat query, scours both Google Search and Google Maps for relevant businesses, scrapes their websites for contact details, and compiles an enriched lead list directly in Google Sheets.

## Who’s this workflow for?

- Sales Development Representatives (SDRs)
- Local Marketing Agencies
- Business Development Teams
- Freelancers & Consultants
- Market Researchers

## How it works

1. **Start with a Chat Query:** The user initiates the workflow by typing a search query (e.g., “dentists in New York”) into a chat interface.

2. **Multi-Source Search:** The workflow queries both the Google Custom Search API (for web results across multiple pages) and scrapes Google Maps (for local businesses) to gather a broad list of potential leads.

3. **Deep Dive Website Scraping:** For each unique business website found, the workflow visits the URL to scrape the raw HTML content of the page.

4. **Intelligent Contact Extraction:** Using custom code, it then parses the scraped website content to find and extract valuable contact information like email addresses, phone numbers, and social media links.

5. **Deduplicate and Log to Sheets:** Before saving, the workflow checks your Google Sheet to ensure the lead doesn’t already exist. All unique, newly enriched leads are then appended as clean rows to your sheet, along with the original search query for tracking.

## Key Requirements to Use This Template

### 1. n8n Instance & Required Nodes

- An active n8n account (Cloud or self-hosted).
- This workflow uses the official n8n LangChain integration (`@n8n/n8n-nodes-langchain`) for the chat trigger. If you are using a self-hosted version of n8n, please ensure this package is installed.

### 2. Google Custom Search API

- A Google Cloud Project with the Custom Search API enabled.
- You will need an API Key for this service.
- You must also create a Programmable Search Engine and get its Search engine ID (`cx`). This tells Google what to search (e.g., the whole web).

### 3. Google Sheets Account

- A Google account and a pre-made Google Sheet with columns for Business Name, Primary Email, Contact Number, URL, Description, Socials, and Search Query.

## Setup Instructions

### 1. Configure the Chat Trigger

- In the **When chat message received** node, you can find the Direct URL or Embed code to use the chat interface.

### 2. Set Up Google Custom Search API (Crucial Step)

- Go to the **Custom Google Search API** (HTTP Request) node.
- Under **Query Parameters**, replace the placeholder values for `key` (with your API Key) and `cx` (with your Search Engine ID). These values are unique to each Google Cloud project.

### 3. Configure Google Sheets

- In all Google Sheets nodes (**Append row in sheet**, **Get row(s) in sheet**, etc.), connect your Google Sheets credentials.
- Select your target spreadsheet (Document ID) and the specific sheet (Sheet Name) where you want to store the leads.

### 4. Activate the Workflow

- Save the workflow and toggle the **Active** switch to ON.
- Open the chat URL and enter a search query to start generating leads.

## FAQ

**Is this template free to use?**
Yes. It's an open-source n8n workflow published by Intuz — copy the workflow JSON from this repo and import it into your own n8n instance at no cost.

**Do I need a paid n8n plan to run this?**
No. It runs on n8n's free self-hosted Community Edition or on n8n Cloud. You'll need your own Google Custom Search API and Google Sheets credentials, not a specific n8n pricing tier.

**Does it create duplicate leads if I search the same query again?**
No. Before appending a row, the workflow checks the Google Sheet and only adds unique, newly enriched leads.

## Related n8n templates from Intuz

- [Personalized sales outreach from LinkedIn job signals with Apify & Google Gemini](https://github.com/Intuz-production/LinkedIn-Lead-Generation)
- [Automate scraping Y Combinator startups with Apify & Google Sheets](https://github.com/Intuz-production/Y-Combinator-Startup-Scraper)
- [Automate lead gen & email outreach with Apify, Apollo.io, GPT-4 & Google Sheets](https://github.com/Intuz-production/AI-Lead-Generation-Automation)

[See all of Intuz's free n8n templates](https://www.intuz.com/n8n-workflow-automation-templates/)

## Connect with us

Intuz is a USA-based AI & workflow automation company with 16+ years of experience building custom AI-enabled workflow automations for SMBs and Enterprises, specializing in agentic AI, LLM integrations, and CRM/ERP sync across Healthcare, FinTech, eCommerce, Manufacturing, and Real Estate.

* **Website:** [https://www.intuz.com](https://www.intuz.com)
* **Email:** [getstarted@intuz.com](mailto:getstarted@intuz.com)
* **LinkedIn:** https://www.linkedin.com/company/intuz/
* **Get Started:** https://n8n.partnerlinks.io/intuz

## For Custom Workflow Automation

[Click here - Get Started](https://www.intuz.com/get-started/)
