# AI Invoice & Document Processing Agent

An n8n automation that receives invoice emails, extracts invoice data from PDF attachments using Google Gemini, stores the results in Google Sheets, validates invoice totals, and sends an email notification.

## Workflow

Gmail Trigger → Analyze Document (Google Gemini) → Google Sheets → IF Validation → Success/Review Email

## Features

- Detects invoice emails with attachments.
- Extracts Invoice ID, Vendor, Invoice Date, Amount, Currency, and Line Items.
- Stores extracted data in Google Sheets.
- Checks that line-item amounts add up to the invoice total.
- Checks quantity × unit price for each line item.
- Sends a success email for valid invoices.
- Sends a review email for failed validation.

## Technologies

- n8n
- Gmail
- Google Gemini
- Google Sheets

## Setup

1. Import `ai-invoice-processing-agent.json` into n8n.
2. Re-select your Gmail, Gemini, and Google Sheets credentials.
3. Set your Google Sheet ID and sheet name.
4. Replace `YOUR_EMAIL@example.com` with your notification recipient.
5. Test with an invoice PDF.
6. Publish/activate the workflow.

> The GitHub version is sanitized. Credentials, personal email addresses, private spreadsheet identifiers, and instance-specific metadata are not included.

## Security

Never commit API keys, OAuth tokens, passwords, private webhook URLs, or other credentials to GitHub.
