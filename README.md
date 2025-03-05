# SharedArrayBuffer Issue in Nuxt Dev Mode

This repository demonstrates an issue where `SharedArrayBuffer` is not available in development mode (`npm run dev`), but works in production mode (`npm run build && node .output/server/index.mjs`).

It is related to issue: https://github.com/Baroshem/nuxt-security/issues/608

## Issue Description

After updating to the latest versions of Nuxt and `nuxt-security`, `SharedArrayBuffer` is no longer accessible in development mode. Previously, with:

- **Nuxt:** `3.12.3`
- **nuxt-security:** `2.0.0-beta.0`

`SharedArrayBuffer` was available when using `nuxt-security`. However, in the latest version, it is missing in dev mode while still working in production.

## Steps to Reproduce

1. Clone this repository:
   ```sh
   git clone https://github.com/your-username/your-repo.git
   cd your-repo
   ```
2. Install dependencies:
   ```sh
   npm install
   ```
3. Run in development mode:
   ```sh
   npm run dev
   ```
   - Open the console and check for `SharedArrayBuffer`.
   - Notice the error.

4. Build and run in production mode:
   ```sh
   npm run build
   node .output/server/index.mjs
   ```
   - Check the console again.
   - No error this time.

## Expected Behavior

`SharedArrayBuffer` should be available in development mode, just like in production, when using `nuxt-security`.

## Actual Behavior

- `SharedArrayBuffer` is **undefined** in development mode.
- `SharedArrayBuffer` is **available** in production mode.
