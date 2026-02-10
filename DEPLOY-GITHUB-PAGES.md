# Deploy Your Portfolio to GitHub Pages

Follow these steps to get your site live at **www.sainikhil.com** (or yourusername.github.io/portfolio until DNS is set).

---

## Step 1: Create a GitHub account (if you don’t have one)

1. Go to [github.com](https://github.com) and click **Sign up**.
2. Complete sign-up and verify your email.

---

## Step 2: Create a new repository

1. Click the **+** in the top-right → **New repository**.
2. **Repository name:** `portfolio` (or any name you like).
3. Choose **Public**.
4. **Do not** check “Add a README” (you already have files).
5. Click **Create repository**.

---

## Step 3: Push your project from your computer

Open Terminal and run these commands **one at a time** (replace `YOUR_USERNAME` with your GitHub username):

```bash
cd /Users/nikhilkunapareddy/Documents/portfolio
```

```bash
git init
```

```bash
git add .
```

```bash
git commit -m "Initial portfolio"
```

```bash
git branch -M main
```

```bash
git remote add origin https://github.com/YOUR_USERNAME/portfolio.git
```
*(Use the repo URL GitHub shows on the new-repo page if the name isn’t “portfolio”.)*

```bash
git push -u origin main
```

When prompted, sign in with your GitHub account (browser or personal access token if you use 2FA).

---

## Step 4: Turn on GitHub Pages

1. On GitHub, open your **portfolio** repository.
2. Click **Settings** (top menu).
3. In the left sidebar, click **Pages** (under “Code and automation”).
4. Under **Build and deployment**:
   - **Source:** select **Deploy from a branch**.
   - **Branch:** choose **main** and **/ (root)**.
   - Click **Save**.

---

## Step 5: Add your custom domain (www.sainikhil.com)

1. Still in **Settings → Pages**.
2. Under **Custom domain**, type: `www.sainikhil.com`
3. Click **Save**.
4. If GitHub offers **Enforce HTTPS**, enable it after the domain is working.

Your site will be live at **https://YOUR_USERNAME.github.io/portfolio/** in a couple of minutes. The custom domain will work after Step 6.

---

## Step 6: Point your domain’s DNS to GitHub

Where you bought **sainikhil.com** (e.g. Namecheap, GoDaddy, Google Domains, Cloudflare):

1. Open the **DNS** or **Manage DNS** section for **sainikhil.com**.
2. Add a **CNAME** record:

   | Type  | Name/Host | Value/Points to        |
   |-------|-----------|------------------------|
   | CNAME | www       | YOUR_USERNAME.github.io |

   - **Name:** `www` (or `www.sainikhil.com` if it asks for full name).
   - **Value:** your GitHub username followed by `.github.io` (no `https://`).

3. Save. Remove any old **A** or **CNAME** record for **www** if it conflicts.

DNS can take **5 minutes to 48 hours** to update. After that, **https://www.sainikhil.com** will show your portfolio.

---

## Updating your site later

After you change files in your portfolio folder:

```bash
cd /Users/nikhilkunapareddy/Documents/portfolio
git add .
git commit -m "Update portfolio"
git push
```

GitHub Pages will redeploy automatically; changes appear in 1–2 minutes.
