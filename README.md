# N8N-News-Automation

📰 AI-Powered Daily WhatsApp News Automation
An automated workflow built using n8n that fetches the latest Hindi news, translates/summarizes them into English using Groq AI (Llama 3.1), and delivers a clean, formatted update directly to your WhatsApp.

🚀 Features
Real-time Fetching: Uses Google News RSS to get the latest headlines.

AI Summarization: Leverages the llama-3.1-8b-instant model on Groq for concise, 2-line English summaries.

Automated Scheduling: Set to trigger every day at a specific time (e.g., 04:40 PM).

WhatsApp Delivery: Sends formatted messages using the Meta WhatsApp Business Cloud API.

🛠️ Tech Stack
n8n: Workflow automation platform.

Groq Cloud AI: High-speed LLM inference for news processing.

Meta Cloud API: Official WhatsApp integration.

RSS: Google News Feed.

📦 How to Setup
Import Workflow: Download the Automation 2.json file and import it into your n8n instance.

Configure Credentials:

Add your Groq API Key in the Groq Chat Model node.

Set up your Meta WhatsApp Cloud API credentials (Phone Number ID and Access Token).

Verification:

Verify your recipient phone number in the Meta Developer Dashboard.

Crucial: Send a "Hi" message to your Test Number from your WhatsApp to open the 24-hour communication window.

Activate: Toggle the workflow to Published mode in n8n.

📋 News Format
The output delivered to WhatsApp follows this professional structure:

🔴 [English Headline]

📝 Summary: [2-line easy English summary]

💡 Pro-Tip
Since this uses a Meta Temporary Access Token, remember to refresh the token every 24 hours in n8n to keep the automation running smoothly!


Key Technical Achievements
Format Consistency: Successfully forces the AI to output data using specific emojis (🔴 and 📝) and 100% English text.

Error Handling: Configured to manage API rate limits by switching to optimized models like llama-3.1-8b-instant.

Privacy-First: The workflow is designed to work with secure credentials while maintaining a seamless delivery window via the 24-hour "Hi" message protocol.

