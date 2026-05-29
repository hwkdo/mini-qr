# HWKDO Docker build configuration

`hwkdo.env` contains build-time variables baked into the static app:

- `VITE_QR_CODE_PRESETS` — QR style + optional embedded `frame` (used when loading config from file)
- `VITE_FRAME_PRESETS` + `VITE_FRAME_PRESET` — frame dropdown and default frame (required for correct frame on first load)

- **GitHub Actions** loads this file when building `ghcr.io/hwkdo/mini-qr`.
- **Local:** `cp deploy/hwkdo.env .env` then `docker compose up -d --build`.

After changing presets, commit `hwkdo.env` and push to `main` to publish a new image
