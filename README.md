# Ghostfolio (LazyCat LPK)

Portfolio tracker for stocks, ETFs and crypto.

- Upstream: https://github.com/ghostfolio/ghostfolio
- Image: `ghostfolio/ghostfolio:3.96.0` (Docker Hub, mirror mode, digest-matched)
- License: AGPL-3.0 (full text in `content/licenses/LICENSE`)
- Containers: Ghostfolio + PostgreSQL 16 + Redis 7

## Notes

- Env contract comes from upstream `.env.example`: `DATABASE_URL`, `REDIS_HOST/PORT/PASSWORD`,
  `ACCESS_TOKEN_SALT`, `JWT_SECRET_KEY`. All secrets come from platform stable secrets.
- Redis requires a password (`--requirepass`) matching `REDIS_PASSWORD`.
- Port 3333 (image-declared); the app listens on `HOST=0.0.0.0` + `PORT=3333`.
- No seeded account upstream — the first user is self-registered.
- Market quotes require outbound internet access from the container.
- No mail service configured.
- Not yet verified on a real device.
