# Newsletter Intelligence Pipeline

Automated marketing intelligence pipeline built with n8n, Gmail, Google Sheets and OpenAI.

## Overview

The workflow processes newsletter emails and transforms them into structured marketing intelligence.

It extracts the newsletter content and images, analyzes both text and visual elements with AI, and combines the results into a structured marketing analysis stored in Google Sheets.

The purpose is to turn historical newsletter data into a reusable dataset for competitive marketing analysis, content research and identification of recurring marketing patterns.

## Workflow

Gmail
↓
Newsletter filtering
↓
Duplicate check
↓
Email extraction
↓
Text analysis ─────────┐
                       ├→ Combined analysis → Google Sheets
Image extraction       │
↓                      │
Image analysis ────────┘

### What it does

- Retrieves newsletters from Gmail
- Checks whether a newsletter has already been analyzed
- Processes one newsletter at a time
- Extracts newsletter text and metadata
- Extracts images from the email
- Downloads and filters relevant images
- Analyzes newsletter copy with OpenAI
- Analyzes newsletter images with OpenAI
- Combines text and visual analysis
- Produces structured marketing intelligence
- Stores the final analysis in Google Sheets

## Marketing Analysis

The workflow analyzes areas such as:

- Newsletter type
- Primary marketing goal
- Target audience
- Main product or service
- Main offer
- Value proposition
- Key marketing messages
- Calls to action
- Persuasion techniques
- Urgency and scarcity
- Tone of voice
- Copywriting style
- Content structure
- Promotional strategy
- Brand positioning
- Customer motivation
- Marketing patterns
- Visual strategy
- Visual style
- Image usage
- Text/image balance

The analysis is designed to identify both explicit marketing messages and recurring patterns that can be useful for broader campaign and competitor analysis.

## Tools

- **n8n** — workflow automation and orchestration
- **Gmail** — newsletter source
- **OpenAI** — text and image analysis
- **Google Sheets** — structured analysis database
- **JavaScript** — email processing, image extraction and data transformation

## Workflow File

The sanitized n8n workflow is available here:

[`workflow/newsletter-intelligence-pipeline.json`](./workflow/newsletter-intelligence-pipeline.json)

The workflow is provided for demonstration and portfolio purposes.

## Data Structure

Each analyzed newsletter is stored as a structured record containing the newsletter metadata and AI-generated marketing analysis.

The image analysis is also linked to the individual newsletter, allowing text and visual insights to be analyzed together.

## Security

This repository contains a sanitized version of the workflow.

Credentials, API keys and private configuration have been removed or replaced with placeholders.

The workflow is provided for demonstration and portfolio purposes. Before using it, configure your own Gmail, OpenAI and Google Sheets credentials.
