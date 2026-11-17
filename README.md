# Minecraft AI World — AI server

## Render settings
- Runtime: Node
- Build command: `npm install`
- Start command: `npm start`
- Add environment variable in Render Dashboard:
  - Key: `OPENAI_API_KEY`
  - Value: your secret OpenAI API key (never commit it to GitHub)

Optional:
- `OPENAI_MODEL` — model name enabled for your API project. If unset, the server uses `gpt-6`; change it to a model available in your API account if needed.

## Endpoints
- `GET /` — server status
- `GET /health` — health check
- `POST /api/chat` — JSON body: `{"message":"Построй дом","gameState":{}}`

The API returns a reply and a restricted list of game actions. The game client must implement those actions.
