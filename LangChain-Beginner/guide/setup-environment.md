# Setup: Environment Variables

This project reads your OpenAI API key from a local `.env` file.

## Get your API key
1. Sign in to OpenAI and open the API keys page:
   https://platform.openai.com/api-keys
2. Create a new secret key and copy it.

## Create your .env
We keep a template you can copy from `guide/.env.example`.

1. Copy the template into the project root (same level as `pyproject.toml`):
   - From: `guide/.env.example`
   - To: `.env`
2. Open `.env` and add your key:

OPENAI_API_KEY=your_key_here

Notes:
- Keep this file private. It is already ignored by git in `.gitignore`.
- If you rotate your key, update `.env`.

That's it. The notebooks load this file with `python-dotenv` and read `OPENAI_API_KEY` with `os.getenv(...)`.
