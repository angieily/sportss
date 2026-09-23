# Sports Research Lab v26 — Shared Free Web App

This version is built so another person can use the app from a normal web link.

## What visitors do
Nothing to install.
They open the Streamlit URL in a browser and use the dashboard.
They do not enter Tavily or Groq keys.

## What the app owner sets up once
1. Put the project in GitHub.
2. Deploy it on Streamlit Community Cloud.
3. Create a Tavily free API key.
4. Create a Groq Free API key.
5. Add both keys privately in Streamlit Community Cloud > App settings > Secrets.

Use:
TAVILY_API_KEY = "tvly-..."
GROQ_API_KEY = "gsk_..."
GROQ_MODEL = "openai/gpt-oss-20b"

## Free-only design
- Streamlit Community Cloud hosts the app.
- Tavily provides the live public-web search layer.
- Groq Free provides the hosted AI summary layer.
- Existing ESPN / official league / nflverse / Open-Meteo / Kalshi sources remain.
- If a free limit is reached, the app reports the limit/failure and does not upgrade itself to a paid plan.

## Deploy
Go to https://share.streamlit.io/
Create an app from the GitHub repository.
Use app.py as the main file.
Add the secrets above in the Secrets settings.
Deploy, then share the resulting *.streamlit.app link.

No OpenAI paid API is used.
No Ollama installation is required.
