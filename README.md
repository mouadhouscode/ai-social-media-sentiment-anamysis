# ai-social-media-sentiment-anamysis
An n8n AI automation workflow that collects social media posts, classifies sentiment using an LLM, and stores structured results in Google Sheets.
# AI-Powered Social Media Sentiment Analysis with n8n

## Overview

This project is an AI-powered automation workflow built with **n8n** that monitors social media posts related to a specific keyword, analyzes their sentiment using a Large Language Model (LLM), and organizes the results in Google Sheets.

The workflow automates the process of collecting and classifying online content, helping businesses monitor public opinions and understand how people feel about a particular topic, product, or brand.

## Workflow Architecture

The automation follows these steps:

1. **Scheduled Trigger:** Automatically starts the workflow at a configured time.
2. **Data Collection:** Uses an HTTP Request node to retrieve recent posts related to a specific keyword.
3. **Data Processing:** Splits the collected data into individual items and processes them iteratively.
4. **AI Sentiment Analysis:** Uses a Basic LLM Chain connected to an OpenRouter Chat Model to classify each post into one of three categories:
   - Positive
   - Negative
   - Neutral
5. **Conditional Routing:** Uses IF nodes to route each classified post to the appropriate category.
6. **Data Storage:** Saves the results in Google Sheets, organized by sentiment category.

For each post, the workflow is designed to store relevant information such as the post content, author name, post ID, and original link.

## Technologies Used

- **n8n** — Workflow automation and orchestration
- **HTTP Request** — Data retrieval from an external endpoint
- **OpenRouter** — Access to an LLM for sentiment classification
- **LLM Chain** — AI-powered text analysis
- **Google Sheets** — Structured storage and organization of results
- **IF Nodes** — Conditional routing based on sentiment
- **Loop Over Items** — Iterative processing of collected posts

## Key Features

- Automated, scheduled monitoring of keyword-related posts
- AI-based sentiment classification
- Automatic categorization of positive, negative, and neutral content
- Structured data storage in Google Sheets
- Reduced manual effort in reviewing social media discussions
- Modular workflow that can be adapted to different keywords and use cases

## Potential Use Cases

This workflow can be adapted for:

- Brand reputation monitoring
- Customer feedback analysis
- Product and service sentiment tracking
- Market research
- Monitoring public reactions to specific topics or campaigns

## Workflow Diagram

The repository includes a visual representation of the n8n workflow, showing the data collection, AI classification, conditional routing, and Google Sheets integration.

## Setup

To reproduce this workflow, you will need:

1. An n8n instance.
2. A configured HTTP endpoint or data source that provides relevant social media posts.
3. An OpenRouter API credential and a compatible chat model.
4. A Google account with access to Google Sheets.
5. A Google Sheets document configured to store the classified results.

Import the exported workflow JSON into n8n, configure your own credentials and data source, and update the spreadsheet references before running it.

**Security note:** API keys, access tokens, private credentials, and sensitive data must never be included in the public repository.

## Project Purpose

This project demonstrates the practical application of workflow automation, LLM integration, conditional logic, and structured data management to solve a real-world business problem.

It is part of my portfolio of AI automation projects focused on building practical solutions that reduce repetitive tasks and improve business workflows.

---

**Author:** Hadid Mouadh

**Tools:** n8n · OpenRouter · LLMs · Google Sheets · HTTP APIs
![Workflow Architecture](screenshots/workflow.png)

