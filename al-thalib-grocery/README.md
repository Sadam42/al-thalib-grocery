# 🛒 Al Thalib Grocery Management System
**Ihala Kotramulla, Sri Lanka**

> Complete grocery store management — inventory, orders, billing, WhatsApp receipts, monthly & annual reports, user login.

---

## 📁 Folder Structure (Important — Do NOT change)

```
al-thalib-grocery/          ← Root folder (upload this to GitHub)
├── public/
│   └── index.html          ← The entire app lives here
├── wasmer.toml             ← Wasmer package config
├── app.yaml                ← Wasmer Edge app config
├── .gitignore
└── README.md
```

> ⚠️ The `index.html` MUST be inside the `public/` folder. Wasmer serves files from there.

---

## 🔑 Default Login

| Username | Password | Role |
|----------|----------|------|
| `admin` | `admin123` | Admin (full access) |

---

## 🚀 DEPLOYMENT GUIDE

### METHOD A — GitHub + Wasmer Import (Recommended)

---

#### STEP 1 — Create a GitHub Account & Repository

1. Go to **https://github.com** → Sign up (free)
2. After login, click the **"+"** button (top right) → **"New repository"**
3. Fill in:
   - **Repository name:** `al-thalib-grocery`
   - **Visibility:** ✅ Public
   - Leave everything else as default
4. Click **"Create repository"**

---

#### STEP 2 — Upload Files to GitHub

On your new empty repository page, click **"uploading an existing file"** link.

Drag and drop ALL these files/folders:
```
al-thalib-grocery/
  ├── public/
  │   └── index.html
  ├── wasmer.toml
  ├── app.yaml
  ├── .gitignore
  └── README.md
```

> 💡 **Tip:** GitHub web upload doesn't support folders directly.
> Upload files one by one, OR use the zip method below.

**Easiest way — upload via zip extract:**
1. Download the `al-thalib-grocery.zip` provided
2. Unzip it on your computer
3. On GitHub, drag ALL the files (including the `public` folder) into the upload area

After uploading, scroll down and click **"Commit changes"** (green button).

---

#### STEP 3 — Create a Wasmer Account

1. Go to **https://wasmer.io** → Click **"Sign Up"** (free)
2. Verify your email
3. You're now in the Wasmer dashboard

---

#### STEP 4 — Import from GitHub to Wasmer

1. In Wasmer dashboard, click **"Deploy"** or **"New Project"**
2. Choose **"Import an existing GitHub repository"**
3. Connect your GitHub account when prompted
4. Select your `al-thalib-grocery` repository
5. Wasmer will auto-detect the `wasmer.toml` and `app.yaml`
6. Click **"Deploy"**

Your live URL will be:
```
https://al-thalib-grocery-YOURUSERNAME.wasmer.app
```

🎉 **Done! Your grocery system is live on the internet!**

---

### METHOD B — Wasmer CLI (Advanced)

#### Install Wasmer CLI

**Windows (PowerShell — run as Administrator):**
```powershell
iwr https://win.wasmer.io -useb | iex
```

**Mac:**
```bash
curl https://get.wasmer.io -sSfL | sh
source $HOME/.wasmer/wasmer.sh
```

**Linux:**
```bash
curl https://get.wasmer.io -sSfL | sh
source $HOME/.wasmer/wasmer.sh
```

Verify:
```bash
wasmer --version
```

#### Login & Deploy

```bash
# Login (opens browser)
wasmer login

# Go into the project folder
cd al-thalib-grocery

# Deploy!
wasmer deploy
```

Answer the prompts:
- **Who should own this app?** → your Wasmer username
- **App name:** `al-thalib-grocery`
- **Publish now?** → yes

---

### METHOD C — GitHub Pages (Simplest — No CLI at all)

> ⚠️ For GitHub Pages, the `index.html` must be in the ROOT (not in `public/`).
> Use the special `github-pages/index.html` version if deploying this way.

1. Upload only `index.html` to root of GitHub repo
2. Go to repo **Settings** → **Pages**
3. Source: **Deploy from branch** → `main` → **/ (root)**
4. Save → wait 2 min
5. URL: `https://YOURUSERNAME.github.io/al-thalib-grocery/`

---

## 🔄 Updating Your App Later

**Via GitHub (easiest):**
1. Open your repository on GitHub
2. Click on `public/index.html`
3. Click the pencil ✏️ edit icon
4. Make changes
5. Click **"Commit changes"**
6. Wasmer will auto-redeploy in 1-2 minutes

**Via CLI:**
```bash
wasmer deploy
```

---

## 💾 How Data is Stored

- **Cloud (online):** JSONBin.io — data syncs across all devices automatically
- **Offline:** Falls back to browser localStorage
- The sidebar shows a green dot ● when cloud is connected

---

## ✨ Features

| Feature | Details |
|---------|---------|
| 🔐 Login | Admin & Staff roles, permanent passwords |
| 📦 Products | Add / Edit / Delete, low stock alerts |
| 🛒 New Order | Cart system, customer name & phone |
| 🧾 Bill Delivery | Print, Save PDF, Send WhatsApp |
| 📋 All Orders | View / Edit / Delete any order |
| 📊 Monthly Report | Revenue, profit, daily breakdown |
| 📈 Annual Report | Monthly trends, bar chart |
| 👥 Users | Add/Edit/Delete staff accounts |
| ☁️ Cloud Sync | JSONBin.io real-time storage |
