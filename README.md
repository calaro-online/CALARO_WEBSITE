# Standalone Webpage Deployment & Free Hosting Guide

This directory contains your standalone, fully interactive landing page for **CALARO**. It is completely separate from the core React/FastAPI codebase. You can host this static webpage **100% for free** and map it to your custom domain using any of the methods below.

---

## Option 1: Vercel (Recommended)
Vercel has an extremely fast global CDN, automated SSL certificates, and zero-configuration custom domain mapping.

### Steps to Deploy:
1. **Sign Up:** Go to [vercel.com](https://vercel.com) and sign up for a free Hobby account.
2. **Install Vercel CLI (Alternative A):**
   - Open your terminal and run: `npm install -g vercel`
   - Navigate to this folder: `cd standalone_website`
   - Run command: `vercel`
   - Log in, follow the defaults, and your site is live!
3. **Import GitHub Repository (Alternative B - Preferred):**
   - Push this folder to a new private or public GitHub repository.
   - On the Vercel dashboard, click **"Add New"** > **"Project"**.
   - Import your GitHub repo, keep default settings, and click **"Deploy"**.

### Mapping Your Custom Domain:
1. In your Vercel Project dashboard, go to **Settings** > **Domains**.
2. Type your domain (e.g., `yourdomain.com`) and click **Add**.
3. Vercel will show DNS records to configure. Go to your domain registrar (GoDaddy, Namecheap, Google Domains, etc.) and add:
   - **Type A Record:** Name: `@` | Value: `76.76.21.21`
   - **Type CNAME Record:** Name: `www` | Value: `cname.vercel-dns.com.`

---

## Option 2: Netlify
Netlify is perfect for drag-and-drop static hosting. You can deploy it in seconds without using the terminal or git.

### Steps to Deploy:
1. **Sign Up:** Create a free account at [netlify.com](https://www.netlify.com/).
2. **Drag & Drop Deployment:**
   - Go to [app.netlify.com/drop](https://app.netlify.com/drop).
   - Drag and drop this **`standalone_website`** folder onto the screen.
   - Your site is deployed immediately!

### Mapping Your Custom Domain:
1. In your Netlify Site dashboard, go to **Site settings** > **Domain management** > **Domains**.
2. Click **Add custom domain**, enter your domain, and click verify.
3. Configure your registrar DNS with Netlify's values:
   - **Type A Record:** Name: `@` | Value: `75.101.145.8`
   - **Type CNAME Record:** Name: `www` | Value: `your-site-name.netlify.app.`

---

## Option 3: GitHub Pages
If your codebase is on GitHub, GitHub Pages is fully integrated and free.

### Steps to Deploy:
1. Push this folder to a GitHub repository.
2. Go to **Settings** > **Pages** in your repository.
3. Under **"Build and deployment"**, select **"Deploy from a branch"**.
4. Choose your branch (e.g., `main`), set directory to `/root`, and click **Save**.

### Mapping Your Custom Domain:
1. Under **Settings** > **Pages**, scroll down to **Custom domain**.
2. Enter your domain name and click **Save**.
3. In your registrar DNS panel, configure these A records:
   - `185.199.108.153`
   - `185.199.109.153`
   - `185.199.110.153`
   - `185.199.111.153`
4. Add a CNAME record for `www` pointing to `yourusername.github.io.`.
