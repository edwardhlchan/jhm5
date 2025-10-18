# Cloudflare Workers Deployment Setup

This portfolio has been configured to deploy as a **Cloudflare Worker** instead of Cloudflare Pages.

## Changes Made

### 1. Updated `wrangler.jsonc`
- Changed from Cloudflare Pages configuration to Workers configuration
- Added `"$schema"` for IDE support
- Replaced `pages_build_output_dir` with `assets.directory`
- Added `observability` settings
- Kept KV namespace bindings for the TOD app

### 2. Updated `package.json` Scripts
- **deploy**: Changed from `wrangler pages deploy` to `wrangler deploy`
- **preview**: Changed from `serve public` to `wrangler dev`
- **dev**: Changed to use `wrangler dev` for local development

## Deployment Commands

### Local Development
```bash
# Generate portfolio and run local dev server
npm run preview

# Or just run dev server (if public folder already built)
npm run dev
```

### Deploy to Production
```bash
# Generate portfolio and deploy to Cloudflare Workers
npm run deploy
```

### First-Time Setup
```bash
# Install dependencies
npm install

# Login to Cloudflare (if not already logged in)
npx wrangler login

# Generate the portfolio
npm run generate

# Deploy
npm run deploy
```

## How It Works

- **Static Assets**: The `public` folder is served as static assets using Workers' built-in assets support
- **KV Storage**: The TOD app's KV namespace is bound and available in the worker
- **Auto-generation**: The portfolio index is automatically generated before each deployment
- **Configuration**: All settings are in the root `wrangler.jsonc` file

## Differences from Pages

| Feature | Cloudflare Pages | Cloudflare Workers |
|---------|------------------|-------------------|
| Deployment | `wrangler pages deploy` | `wrangler deploy` |
| Static Assets | Automatic | Via `assets` config |
| Custom Logic | Pages Functions | Full Worker script |
| Local Dev | External server | `wrangler dev` |
| Build Output | `pages_build_output_dir` | `assets.directory` |

## Benefits of Workers

1. **More Control**: Full Worker API available for custom logic
2. **Single Configuration**: One `wrangler.jsonc` for everything
3. **Integrated Dev Experience**: Built-in dev server with hot reload
4. **Better Observability**: Native observability support
5. **Flexible Routing**: Can add custom request handling if needed

## Notes

- The `./worker` directory contains a separate worker template that can be used as reference
- Your main deployment is now from the root directory
- All projects in `src/` are built into `public/` during generation
- KV bindings work the same way in Workers as they did in Pages
