# HWKDO Docker build configuration

`hwkdo.env` contains build-time variables (including `VITE_QR_CODE_PRESETS`) baked into the static app.

- **GitHub Actions** loads this file when building `ghcr.io/hwkdo/mini-qr`.
- **Local:** `cp deploy/hwkdo.env .env` then `docker compose up -d --build`.

After changing presets, commit `hwkdo.env` and push to `main` to publish a new image.
