Frontend (Vercel)

1. If your frontend is static HTML/JS, point Vercel to this `frontend` folder as the Project Root when importing the repo.
2. Add an Environment Variable named `API_BASE_URL` with the value `https://YOUR_BACKEND_ON_RENDER.onrender.com` (replace with your Render service URL).
3. `vercel.json` contains a rewrite to proxy `/api/*` to the backend. Update the placeholder `YOUR_BACKEND_ON_RENDER` before deploying or use Vercel environment variables and runtime rewrites.

Notes:
- If your frontend code currently hardcodes API endpoints, change them to use `process.env.API_BASE_URL` (for frameworks) or set a runtime `API_BASE_URL` via Vercel (for static sites replace at build time).
- Do not commit production secrets into the repo.
