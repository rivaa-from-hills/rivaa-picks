# Rivaa's Picks

A free link-in-bio page for Rivaa's Instagram. It shows each product's photo with a **Shop on Amazon** button, with category filters on the left (or across the top on phones).

You add products from your phone using a private admin page. No coding, no deploy step.

## What's in this folder

| File | What it is |
|---|---|
| `index.html` | The public page your bio links to |
| `admin.html` | Your private upload page (photo + link + Publish) |
| `products.json` | The product list. The admin page edits this for you |
| `images/` | Product photos. The admin page adds to this for you |
| `.nojekyll` | Tells GitHub Pages to serve the files as they are |

There is no build step and nothing to install.

## 1. Put it on GitHub (one time)

Pick **one** way.

**A. GitHub Desktop (no terminal, easiest)**
1. Install GitHub Desktop and sign in.
2. File → **Add local repository** → choose this `rivaa-picks` folder. When it says it isn't a repository yet, click **create a repository here**.
3. Click **Publish repository**. **Untick "Keep this code private"** (free GitHub Pages needs a public repo).

**B. VS Code**
1. File → **Open Folder** → this folder.
2. Left bar → **Source Control** → **Initialize Repository** → type a message → **Commit**.
3. Click **Publish Branch** → choose **Public repository**.

**C. Website only (no tools)**
1. On github.com click **New repository**, name it `rivaa-picks`, set it Public.
2. Click **uploading an existing file** and drag in everything *inside* this folder (not the zip itself).

## 2. Turn on the website (one time)

Repo → **Settings** → **Pages** → Source: **GitHub Actions**. The workflow in `.github/workflows/deploy.yml` then deploys the site on every push to `main` (including edits made by the admin page).

After a minute your page is at `https://YOUR-USERNAME.github.io/rivaa-picks/`. Put that in your Instagram bio.

## 3. Connect the admin page (one time)

1. Open the [GitHub token page](https://github.com/settings/personal-access-tokens/new).
2. Name: `Rivaa admin`. Repository access: **Only select repositories** → pick `rivaa-picks`.
3. Permissions → Repository permissions → **Contents: Read and write**.
4. Generate the token and copy it.
5. Open `https://YOUR-USERNAME.github.io/rivaa-picks/admin.html`, type `YOUR-USERNAME/rivaa-picks`, paste the token, tap **Save and connect**.
6. On your phone, use **Add to Home Screen** so it opens like an app.

The token stays in that browser only. Don't use the admin page on a shared computer. If a device is lost, delete the token on GitHub.

## 4. Every day

Open the admin page → choose the photo → paste the affiliate link (e.g. `link.amazon/…` or `amzn.to/…`) → pick the category → type a short name → **Publish**. It is live in about 1–2 minutes.

- Photos should be Rivaa's own styled pictures (portrait works best). They are shrunk automatically.
- Don't copy photos from Amazon's website. Amazon doesn't allow its product photos to be reused this way.
- **Change link** and **Remove** are at the bottom of the admin page.

## Amazon rules this page follows

- Shows "As an Amazon Associate I earn from qualifying purchases."
- Says Rivaa is an AI-generated character.
- Affiliate links are marked `sponsored`.
- No prices are shown (they change and Amazon limits showing them).
- Don't buy through your own links. Amazon treats that as a violation.

## Preview on your computer (optional)

In VS Code install **Live Server** (it will suggest it), right-click `index.html` → **Open with Live Server**. Opening the file by double-click will not load the product list, because browsers block that.

## Changing the look

The colours and layout are in the `<style>` section at the top of `index.html`. If you want a different look, ask Claude to change it, then upload the new `index.html`.
