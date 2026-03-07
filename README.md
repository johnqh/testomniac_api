# testomniac_api

Backend API server for the Testomniac AI-powered automated UI testing platform. Built with Hono on Bun with PostgreSQL and Firebase auth.

## Setup

```bash
bun install
cp .env.example .env   # Configure DATABASE_URL, Firebase credentials
```

## Routes

| Method | Path | Auth | Description |
|--------|------|------|-------------|
| GET | `/api/v1/users/:userId/histories` | Required | List user histories |
| POST | `/api/v1/users/:userId/histories` | Required | Create history |
| PUT | `/api/v1/users/:userId/histories/:id` | Required | Update history |
| DELETE | `/api/v1/users/:userId/histories/:id` | Required | Delete history |
| GET | `/api/v1/histories/total` | Public | Global total |
| GET | `/health` | Public | Health check |

## Development

```bash
bun run dev          # Watch mode (port 8022)
bun run build        # Build for production
bun run start        # Run built output
bun test             # Run tests
bun run verify       # All checks + build
```

## Environment Variables

| Variable | Default | Description |
|----------|---------|-------------|
| `PORT` | 8022 | Server port |
| `DATABASE_URL` | -- | PostgreSQL connection string |
| `FIREBASE_PROJECT_ID` | -- | Firebase project ID |
| `FIREBASE_CLIENT_EMAIL` | -- | Firebase service account email |
| `FIREBASE_PRIVATE_KEY` | -- | Firebase private key |

## Related Packages

- `testomniac_types` -- Shared type definitions
- `testomniac_client` -- API client SDK
- `testomniac_lib` -- Business logic library
- `testomniac_app` -- Web frontend
- `testomniac_app_rn` -- React Native frontend
- `testomniac_extension` -- Chrome extension

## License

BUSL-1.1
