# Website

Single-page static site. No build step, no dependencies — just `index.html`.

## Deploy: GitHub → Vercel

### 1. Push to GitHub

Open a terminal in this folder and run:

```bash
git init
git add .
git commit -m "Initial commit"
```

Then go to https://github.com/new, create a new repository (don't initialize it with a README), and copy the remote URL it gives you. Then:

```bash
git remote add origin YOUR_GITHUB_REPO_URL
git branch -M main
git push -u origin main
```

### 2. Deploy on Vercel

1. Go to https://vercel.com and sign in with your GitHub account.
2. Click **Add New → Project**.
3. Select the GitHub repo you just pushed.
4. Vercel will auto-detect it as a static site — no build command or output directory needed. Leave the defaults.
5. Click **Deploy**.

That's it — Vercel gives you a live URL immediately, and every future `git push` to `main` will auto-deploy.

### 3. Custom domain (optional)

In the Vercel project → **Settings → Domains**, add your domain and follow the DNS instructions it gives you (usually just adding a CNAME or A record at your domain registrar).
