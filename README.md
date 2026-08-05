# Aly Maklad Portfolio

An interactive AI-style portfolio for Aly Maklad. The site includes a static single-page frontend and a Vercel serverless API route that answers visitor questions using OpenRouter's OpenAI-compatible chat completions API.

## Features

- Minimal responsive portfolio landing page
- Quick-answer cards for profile, projects, skills, contact, location, and resume
- Free-text question box with fallback AI answers grounded in Aly's resume/context
- Downloadable resume PDF
- Serverless `/api/ask` endpoint for Vercel deployments

## Project Structure

```text
.
├── api/
│   └── ask.js                 # Vercel serverless function
├── Aly_Maklad_CV.pdf          # Resume PDF
├── avatar-transparent.png     # Portfolio avatar image
├── index.html                 # Main portfolio page
└── README.md
```

## Local Development

This is mostly a static site, so you can open `index.html` directly in a browser for the frontend.

To test the serverless API locally, use Vercel:

```bash
npm install -g vercel
vercel dev
```

Then visit:

```text
http://localhost:3000
```

## Environment Variables

The AI fallback route requires:

```text
OPENROUTER_API_KEY=your_openrouter_api_key
```

Set this in your Vercel project under:

```text
Project Settings -> Environment Variables
```

The frontend still works without the API key, but free-text AI fallback answers will show a friendly fallback message.

## Deployment

Deploy with Vercel:

```bash
vercel
vercel --prod
```

The API route is available at:

```text
/api/ask
```

## Tech

- HTML, CSS, and vanilla JavaScript
- Vercel Serverless Functions
- OpenRouter chat completions API

