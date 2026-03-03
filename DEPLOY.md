# Hosting Album Ratings on GitHub Pages

Your site is a single `index.html` file. GitHub Pages will serve it directly — no build step, no server config needed.

---

## What you need

- A free [GitHub account](https://github.com)
- The `index.html` file (downloaded from this chat)

---

## Step-by-step

### 1. Create a new repository

1. Go to [github.com/new](https://github.com/new)
2. Give it a name — e.g. `album-ratings`
3. Set it to **Public** (required for free GitHub Pages)
4. Check **"Add a README file"**
5. Click **Create repository**

---

### 2. Upload your file

1. On your new repo's main page, click **Add file → Upload files**
2. Drag in your `index.html` file
3. Scroll down, leave the commit message as-is, and click **Commit changes**

---

### 3. Enable GitHub Pages

1. Go to your repo's **Settings** tab (top nav)
2. In the left sidebar, click **Pages**
3. Under **Source**, select **Deploy from a branch**
4. Set the branch to **main** and the folder to **/ (root)**
5. Click **Save**

---

### 4. Visit your site

After about 60 seconds, GitHub will show a green banner:

> **Your site is live at** `https://YOUR-USERNAME.github.io/album-ratings/`

That URL is your permanent public link. Share it with anyone.

---

## Updating the site in the future

When you get an updated `index.html` from this chat:

1. Go to your repo on GitHub
2. Click on `index.html` in the file list
3. Click the **pencil icon** (Edit) — or click **...** → **Upload new version** and drag in the new file
4. Commit the change

GitHub Pages will re-deploy automatically within about 60 seconds.

---

## Important notes

### Your data stays local
Everything you add — new album entries, uploaded art, score edits — is stored in your **browser's localStorage**, not on GitHub. This means:

- The GitHub repo only holds the app code, not your ratings data
- Your data is tied to the browser you use the site in
- If you clear browser data or use a different browser, your added entries won't be there

### Backing up your data
To avoid losing entries, periodically open your browser's DevTools (F12), go to **Application → Local Storage**, find the keys starting with `albums2025_`, and copy their values somewhere safe.

### The site works offline too
Once loaded, the main list and all seed album detail pages work without internet. You only need a connection to:
- Add a new album (iTunes API lookup)
- Load album art for the first time (auto-fetched in background)

---

## Optional: use a custom domain

If you own a domain (e.g. `ratings.yourdomain.com`), you can point it at GitHub Pages:

1. In repo **Settings → Pages**, enter your domain in the **Custom domain** field
2. Add a CNAME record at your DNS provider pointing to `YOUR-USERNAME.github.io`
3. GitHub will provision HTTPS automatically within a few minutes
