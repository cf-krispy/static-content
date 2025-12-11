# Static Content Site

A simple static site for serving maintenance and error pages on Cloudflare Workers.

## Deploy to Cloudflare

[![Deploy to Cloudflare Workers](https://deploy.workers.cloudflare.com/button)](https://deploy.workers.cloudflare.com/?url=https://github.com/cf-krispy/static-content)

## Manual Deployment

```bash
npx wrangler deploy
```

## Workers Route Configuration

After deployment, configure your Workers route in the Cloudflare dashboard:

1. Go to **Workers & Pages** → `static-content`
2. Navigate to **Settings** → **Triggers**
3. Add or edit your route with the pattern: `*.yourdomain.com/*`

**Important:** The `/*` at the end is required to serve all assets (HTML, images, CSS, etc.). Without it, only the root path will work and images/assets will return 404 errors.

## Files

- `static/index.html` - Maintenance page
- `static/error.html` - Error page (503)
- `static/small-image.png` - Site logo
