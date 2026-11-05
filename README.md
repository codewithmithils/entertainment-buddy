# Entertainment Buddy

**An AI-powered personal entertainment recommendation assistant built with n8n, Groq, and Tavily.**

Entertainment Buddy helps users discover movies, web series, anime, documentaries, and entertainment events based on their mood, interests, preferred language, available time, and budget.

## Features

- Personalised recommendations based on mood and preferences
- Suggestions across Telugu, Hindi, English, Korean, and international content
- 3–5 recommendations with a short explanation for each
- Web search through Tavily for current releases, ratings, streaming availability, and upcoming events
- Careful handling of current information: avoids inventing dates, prices, ratings, or availability

## Workflow

`Chat Trigger → AI Agent`

The AI Agent uses:
- **Groq Chat Model** — `openai/gpt-oss-120b` for language generation
- **Tavily MCP** — web search tool for current entertainment information

## Tech Stack

- [n8n](https://n8n.io/) — workflow automation and agent orchestration
- [Groq](https://groq.com/) — language model inference
- [Tavily](https://tavily.com/) — web search

## Repository Structure

```text
entertainment-buddy/
├── README.md
└── workflow/
    └── entertainment-buddy.json
```

## Import and Set Up

1. Download `workflow/entertainment-buddy.json`.
2. In your n8n workspace, choose **Import from File** and select the downloaded JSON.
3. Open the **Groq Chat Model** node and connect your own Groq credentials.
4. Open the **Tavily MCP** node and configure your own Tavily connection/credentials.
5. Check that both nodes are connected to the AI Agent, then test the chat workflow.
6. Publish or activate the workflow according to your n8n setup.

You need your own n8n workspace and API access for Groq and Tavily. Credentials are intentionally not included in this repository.

## Example Prompts

- "Recommend three mind-bending thriller movies."
- "Suggest underrated Telugu movies for tonight."
- "I have two hours and want a feel-good movie. What should I watch?"
- "Find upcoming entertainment events in Hyderabad."

## Security

Never commit API keys, access tokens, passwords, or personal credentials. Configure credentials inside your own n8n workspace.

## Author

Created by [@codewithmithils](https://github.com/codewithmithils).
