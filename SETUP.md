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

## Step 3 — Turn on the snake animation 🐍
The contribution-snake images (`...output/...snake.svg`) won't appear until the
GitHub Action runs once and creates the `output` branch.

1. After pushing, open your repo → **Actions** tab
2. If prompted, click **"I understand my workflows, enable them"**
3. Open **"Generate Contribution Snake"** → **Run workflow**
4. Wait ~30s. It creates an `output` branch with the SVGs. The snake will then render.

(After that it auto-updates every 12 hours and on every push.)

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
