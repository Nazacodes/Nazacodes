# 🚀 How to publish your profile README

Your GitHub profile README lives in a **special repository named exactly after your username**.
For you that means a repo called **`nazacodes/nazacodes`**.

## Step 1 — Create the repo on GitHub
1. Go to https://github.com/new
2. **Repository name:** `nazacodes` (must match your username exactly)
3. Set it to **Public**
4. Do **not** initialize with a README (you already have one here)
5. Click **Create repository**

> When the repo name matches your username, GitHub shows a note:
> *"You found a secret! nazacodes/nazacodes is a special repository..."* — that's the one.

## Step 2 — Push this folder
Run these from inside this folder (`/Users/naza/githubpf`):

```bash
git init
git add .
git commit -m "✨ Add animated profile README"
git branch -M main
git remote add origin https://github.com/nazacodes/nazacodes.git
git push -u origin main
```

## Step 3 — Turn on the auto-generated visuals 🧊📊
Two images are produced by GitHub Actions and won't appear until each workflow
runs at least once. After pushing, open your repo → **Actions** tab, click
**"I understand my workflows, enable them"** if prompted, then run each:

1. **Generate 3D Contribution Calendar** — commits `profile-3d-contrib/*.svg`
   (the isometric 3D skyline near the top). No secret required. ~1 min.
2. **Generate Metrics** — commits `metrics.svg`, the **main GitHub Stats card**
   (commits/stars/followers header + language breakdown + isometric calendar).
   **This one needs the `METRICS_TOKEN` secret — see Step 3b.** Until it runs,
   the GitHub Stats card shows a broken image, so set the token before relying
   on your profile.

Both re-run automatically on a schedule (and the 3D calendar on every push).

> ℹ️ Why metrics instead of the usual `github-readme-stats` cards? Those are
> served live by a shared public instance that frequently rate-limits (HTTP 503)
> — which is exactly why the stats section looked broken. `metrics.svg` is
> generated once and **committed to your repo**, so it always renders.

## Step 3b — METRICS_TOKEN (required for the stats card)
The metrics workflow needs a Personal Access Token:

1. Create a **classic** token at https://github.com/settings/tokens with scopes
   `repo`, `read:org`, `read:user`.
2. In your repo: **Settings → Secrets and variables → Actions → New repository
   secret**. Name it exactly **`METRICS_TOKEN`**, paste the token.
3. Run the **Generate Metrics** workflow.

If you'd rather not use it at all, delete `.github/workflows/metrics.yml` and
remove the `metrics.svg` image line in the **GitHub Stats** section of
`README.md`.

## Step 4 — Personalize ✏️
Open `README.md` and update the clearly-marked spots:
- The `whoami` code block (pronouns, location, fun fact)
- The **Connect with me** links — replace `your-handle` / `your-website.com`
- Add/remove tech badges to match your real stack
- Header subtitle, quote, etc.

Find all real GitHub badge slugs at https://shields.io and logos at https://simpleicons.org

## Notes
- All the stats widgets (`github-readme-stats`, streak, trophies, activity graph)
  read your **public** contribution data automatically once the repo is live.
- To include **private** contribution counts in the stats card, you can self-host
  the stats widget — see https://github.com/anuraghazra/github-readme-stats#deploy-on-your-own-vercel-instance
- Preview markdown locally anytime, but the dynamic images only render on github.com.

Enjoy your new profile! ⭐️
