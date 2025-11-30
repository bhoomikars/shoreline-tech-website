# Shoreline Tech Website - Deployment Guide

## Domain Options

Since `shorelinetech.com` is already registered, here are alternative domain options:

### Available Domain Alternatives:
1. **shorelinetech.io** - Tech-focused TLD (recommended)
2. **shorelinetech.dev** - Developer-focused
3. **shorelinetech.co** - Business alternative
4. **getshorelinetech.com**
5. **shorelinetechconsulting.com**
6. **shoreline-tech.com** (with hyphen)

### Check Domain Availability:
- [Namecheap](https://www.namecheap.com/)
- [Google Domains](https://domains.google/)
- [GoDaddy](https://www.godaddy.com/)

**Cost**: $10-15/year typically

---

## Deployment Options

### Option 1: Netlify (Recommended - FREE & Easy)

**Pros**: Free hosting, automatic SSL, custom domain, continuous deployment
**Time**: 5 minutes

#### Steps:
1. **Create Netlify account**: Go to [netlify.com](https://www.netlify.com/)
2. **Deploy via drag & drop**:
   ```bash
   # Create a zip file of your project
   cd /Users/bhoomikars
   zip -r shoreline-tech-website.zip shoreline-tech-website -x "*.git*" "*.DS_Store"
   ```
3. Drag `shoreline-tech-website.zip` to Netlify dashboard
4. Your site will be live at `https://random-name-12345.netlify.app`
5. **Add custom domain**:
   - Go to Site settings > Domain management
   - Add your custom domain (e.g., shorelinetech.io)
   - Follow DNS configuration steps
   - SSL certificate is automatic!

**Cost**: FREE

---

### Option 2: Vercel (FREE & Developer-Friendly)

**Pros**: Free, fast, automatic HTTPS, great performance
**Time**: 5 minutes

#### Steps:
1. **Create Vercel account**: Go to [vercel.com](https://vercel.com/)
2. **Deploy via CLI**:
   ```bash
   # Install Vercel CLI
   npm install -g vercel

   # Deploy
   cd /Users/bhoomikars/shoreline-tech-website
   vercel
   ```
3. Follow prompts (press Enter for defaults)
4. Your site is live at `https://shoreline-tech-website.vercel.app`
5. **Add custom domain** in Vercel dashboard

**Cost**: FREE

---

### Option 3: GitHub Pages (FREE)

**Pros**: Free, simple, good for static sites
**Time**: 10 minutes

#### Steps:
1. **Create GitHub repository**:
   ```bash
   cd /Users/bhoomikars/shoreline-tech-website
   git init
   git add .
   git commit -m "Initial commit - Shoreline Tech website"
   ```

2. **Create repo on GitHub**:
   - Go to [github.com/new](https://github.com/new)
   - Name: `shoreline-tech-website`
   - Make it public
   - Don't initialize with README

3. **Push to GitHub**:
   ```bash
   git remote add origin https://github.com/YOUR-USERNAME/shoreline-tech-website.git
   git branch -M main
   git push -u origin main
   ```

4. **Enable GitHub Pages**:
   - Go to repo Settings > Pages
   - Source: Deploy from branch `main`
   - Folder: `/ (root)`
   - Save

5. Site will be live at: `https://YOUR-USERNAME.github.io/shoreline-tech-website/`

6. **Add custom domain**:
   - Add a file named `CNAME` with your domain:
     ```bash
     echo "shorelinetech.io" > CNAME
     git add CNAME
     git commit -m "Add custom domain"
     git push
     ```
   - Configure DNS at your domain registrar (see DNS section below)

**Cost**: FREE

---

### Option 4: AWS S3 + CloudFront (Professional)

**Pros**: Highly scalable, professional, fast global CDN
**Cons**: Requires AWS knowledge
**Time**: 30 minutes

#### Steps:
1. Create S3 bucket
2. Enable static website hosting
3. Upload files
4. Configure CloudFront distribution
5. Add custom domain with SSL certificate (AWS Certificate Manager)

**Cost**: ~$1-5/month (low traffic)

---

### Option 5: DigitalOcean App Platform

**Pros**: Simple, scalable, good developer experience
**Time**: 10 minutes

#### Steps:
1. Create DigitalOcean account
2. Create new Static Site app
3. Connect GitHub repo or upload files
4. Deploy
5. Add custom domain

**Cost**: $0-5/month

---

## DNS Configuration (For Custom Domain)

Once you've purchased a domain, configure DNS:

### For Netlify:
Add these DNS records at your domain registrar:
```
Type: A
Name: @
Value: 75.2.60.5

Type: CNAME
Name: www
Value: YOUR-SITE-NAME.netlify.app
```

### For Vercel:
```
Type: A
Name: @
Value: 76.76.21.21

Type: CNAME
Name: www
Value: cname.vercel-dns.com
```

### For GitHub Pages:
```
Type: A
Name: @
Value: 185.199.108.153
Value: 185.199.109.153
Value: 185.199.110.153
Value: 185.199.111.153

Type: CNAME
Name: www
Value: YOUR-USERNAME.github.io
```

---

## Recommended Deployment Path

### Step 1: Quick Deploy (Today)
Use **Netlify** for instant free hosting:
```bash
# Option A: Drag & drop to netlify.com
# Option B: Use Netlify CLI
npx netlify-cli deploy --prod --dir=/Users/bhoomikars/shoreline-tech-website
```

Your site will be live at: `https://random-name.netlify.app`

### Step 2: Get Custom Domain (This Week)
1. Buy domain from Namecheap/Google Domains
   - Recommended: **shorelinetech.io** or **shorelinetech.dev**
2. Connect to Netlify (automatic SSL)
3. Update contact form email if needed

### Step 3: Optional Enhancements
- Add Google Analytics
- Set up email forwarding (e.g., hello@shorelinetech.io)
- Add contact@shorelinetech.io for professional email

---

## Quick Commands Reference

### Test Locally:
```bash
cd /Users/bhoomikars/shoreline-tech-website
python3 -m http.server 8000
# Visit: http://localhost:8000
```

### Deploy to Netlify (CLI):
```bash
npm install -g netlify-cli
cd /Users/bhoomikars/shoreline-tech-website
netlify deploy --prod
```

### Deploy to Vercel:
```bash
npm install -g vercel
cd /Users/bhoomikars/shoreline-tech-website
vercel --prod
```

### Create GitHub Repo:
```bash
cd /Users/bhoomikars/shoreline-tech-website
git init
git add .
git commit -m "Initial commit"
gh repo create shoreline-tech-website --public --source=. --push
```

---

## Email Setup (Professional Touch)

### Option 1: Google Workspace
- **Cost**: $6/user/month
- Get: hello@shorelinetech.io, bhoomika@shorelinetech.io, sagar@shorelinetech.io
- Setup: 15 minutes

### Option 2: Zoho Mail (Free)
- **Cost**: FREE (up to 5 users)
- Professional email hosting
- Setup: 20 minutes

### Option 3: Email Forwarding (Simple)
- **Cost**: FREE
- Forward hello@shorelinetech.io → bhoomikars28@gmail.com
- Available through domain registrar

---

## Performance Optimizations (After Launch)

1. **Image Optimization**:
   - Convert bhoomika.jpg and sagar.jpg to WebP format
   - Reduce file sizes

2. **CDN**: Already included with Netlify/Vercel

3. **Analytics**:
   ```html
   <!-- Add to <head> in index.html -->
   <!-- Google Analytics -->
   <script async src="https://www.googletagmanager.com/gtag/js?id=G-XXXXXXXXXX"></script>
   ```

---

## Support & Monitoring

### Free Tools:
- **Uptime Monitoring**: [UptimeRobot](https://uptimerobot.com/) (free)
- **Analytics**: Google Analytics (free)
- **Error Tracking**: [Sentry](https://sentry.io/) (free tier)

---

## Next Steps

1. ✅ **Deploy to Netlify** (5 min) - Get live URL
2. ⏳ **Purchase domain** (shorelinetech.io recommended)
3. ⏳ **Connect domain to Netlify** (5 min)
4. ⏳ **Set up professional email** (optional)
5. ⏳ **Add Google Analytics** (optional)
6. ⏳ **Share with clients!** 🚀

---

## Need Help?

- **Netlify Docs**: https://docs.netlify.com/
- **Vercel Docs**: https://vercel.com/docs
- **GitHub Pages**: https://pages.github.com/

## Contact
- Bhoomika RS: bhoomikars28@gmail.com
- Website will be live at: https://shorelinetech.io (once domain is purchased)
