# Artist Manager Bot

A Telegram bot designed to help artists manage their career, social media presence, and streaming profiles.

## Setup

1. Clone the repository:
```bash
git clone https://github.com/yourusername/artistmanager00.git
cd artistmanager00
```

2. Create and activate a virtual environment:
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. Install dependencies:
```bash
pip install -r requirements.txt
```

4. Create a `.env` file with your credentials:
```
TELEGRAM_BOT_TOKEN=your_bot_token
OPENAI_API_KEY=your_openai_api_key
```

5. Run the bot:
```bash
python -m artist_manager_agent
```

## Features

- Personalized onboarding process
- Career stage assessment and guidance
- Social media profile management
- Streaming platform integration
- Goal setting and tracking

## Development

To install in development mode:
```bash
pip install -e .
```

## Vercel Deployment

1. Install the Vercel CLI:
```bash
npm i -g vercel
```

2. Login to Vercel:
```bash
vercel login
```

3. Deploy to Vercel:
```bash
vercel
```

4. Set up environment variables in Vercel:
- Go to your project settings
- Add the following environment variables:
  - `TELEGRAM_BOT_TOKEN`
  - `OPENAI_API_KEY`
  - `OPENAI_MODEL`
  - `DATABASE_URL`
  - `LOG_LEVEL`

5. Set up the Telegram webhook:
```bash
curl "https://api.telegram.org/bot$TELEGRAM_BOT_TOKEN/setWebhook?url=https://your-vercel-url.vercel.app/api/vercel"
```

## Project Structure

- `artist_manager_agent/` - Main bot code
  - `bot.py` - Bot initialization and core logic
  - `onboarding.py` - Onboarding wizard
  - `models.py` - Data models
  - `agent.py` - AI agent logic
  - `blockchain.py` - Blockchain integration
  - `log.py` - Logging utilities
- `api/` - Vercel serverless functions
- `tests/` - Test suite
- `deploy.py` - Local deployment script
- `deploy_prod.py` - Production deployment script

## Contributing

1. Fork the repository
2. Create a feature branch
3. Commit your changes
4. Push to the branch
5. Create a Pull Request

## License

MIT License - see LICENSE file for details
