# DepEd Aringay District LRs - Web Deployment

This repository connects the **DepEd Aringay District Learning Resources (LRs) Repository** to a clean, custom URL on **Vercel** using **Method 2 (Gateway Wrapper)**.

---

## ⚡ How It Works (Method 2)
1. **Google Apps Script** handles all backend logic, Google Sheets read/write, and live data.
2. The root `index.html` file on GitHub/Vercel acts as a full-bleed, seamless responsive wrapper pointing to your Apps Script Web App:
   `https://script.google.com/macros/s/AKfycbwFmFTs1C53mTM4nk56nBOM1bnCjszvn96padGs1Frrh7_EcR4de321hDbOaaNIBh8SzA/exec`
3. **No manual GitHub updates needed**: Whenever you edit `Code.gs` or `Index.html` in Apps Script, just click **Deploy ➔ New Version**. Your Vercel website will immediately reflect all updates!

---

## 🚀 Quick Setup (3 Minutes)

### Step 1: Upload to GitHub
1. In your GitHub repository (e.g. `aringay-dlrs`), upload the files:
   - `index.html` (the root wrapper)
   - `vercel.json`
   - (Optional) `/gas` folder containing the backups of your Apps Script files.
2. Commit and push.

### Step 2: Deploy to Vercel
1. Go to [vercel.com](https://vercel.com) and import your repository.
2. Click **Deploy**.
3. Under **Project Settings ➔ Domains**, customize your domain (e.g., `aringaydlrs.vercel.app`).
