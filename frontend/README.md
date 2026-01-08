Cloudflare Pages (frontend) quick deploy

Option A — publish with Cloudflare Pages using the dashboard
- Push the `frontend/` folder to a GitHub repo and connect it to Pages via the Cloudflare dashboard. Set build command empty and publish directory `.` (or `main-pages` depending on your structure).

Option B — publish via Wrangler CLI (Pages command)

```bash
npm install -g wrangler
wrangler login
wrangler pages publish ./ --project-name=bowling-frontend
```

Notes:
- To have `/api/*` proxied to a Worker, configure a route in Cloudflare Dashboard (Workers → Add route) to point `https://yourdomain.com/api/*` to the backend Worker.
