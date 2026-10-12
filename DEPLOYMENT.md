# Deployment Guide

## 🚀 Quick Deployment Options

### 1. Vercel (Recommended - Easiest)

**Pros:**
- Free tier includes 100GB bandwidth
- Automatic deployments from git
- Instant SSL
- Great performance for India traffic
- Easy domain setup

**Steps:**
```bash
# Install Vercel CLI
npm install -g vercel

# Deploy from project directory
cd /Users/iambabu/resume-builder-mnc
vercel

# For production
vercel --prod
```

**Custom Domain:**
1. Go to Vercel dashboard
2. Add your domain
3. Update DNS records (Vercel provides)
4. SSL auto-provisioned

### 2. Netlify

**Pros:**
- Free tier includes bandwidth and storage
- Git integration
- Form handling built-in
- Edge functions for serverless

**Steps:**
```bash
# Build locally first
npm run build

# Deploy
npm install -g netlify-cli
netlify deploy --prod --dir=dist
```

### 3. GitHub Pages (Free)

**Pros:**
- Completely free
- Built-in git backup
- Easy to manage

**Steps:**
```bash
# Build
npm run build

# Push dist folder to gh-pages
git add dist/
git commit -m "Deploy to GitHub Pages"
git subtree push --prefix dist origin gh-pages
```

**Note:** Your site will be at `username.github.io/resume-builder-mnc`

### 4. AWS S3 + CloudFront

**Pros:**
- Very scalable
- Good for high traffic
- Can handle high concurrent users

**Steps:**
1. Create S3 bucket
2. Enable static website hosting
3. Upload dist/ contents
4. Create CloudFront distribution
5. Route domain via Route53

**Cost:** ~$1-5/month for typical traffic

## 📋 Pre-Deployment Checklist

### Content & Branding
- [ ] Update all branding and colors
- [ ] Replace favicon
- [ ] Update social media links
- [ ] Set up email address

### SEO & Analytics
- [ ] Add Google Analytics 4 tracking
- [ ] Set up Google Search Console
- [ ] Add sitemap.xml
- [ ] Create robots.txt
- [ ] Add schema markup

### Monetization
- [ ] Add Google AdSense code (or other ad network)
- [ ] Set up Google Analytics events for conversions
- [ ] Create privacy policy page
- [ ] Create terms of service page

### Technical
- [ ] Test on mobile devices
- [ ] Test form functionality
- [ ] Test PDF download
- [ ] Check all links work
- [ ] Verify no console errors

### Performance
- [ ] Minify and optimize assets
- [ ] Enable gzip compression
- [ ] Set cache headers
- [ ] Test page speed (target: < 2s)

## 🔧 Configuration Files

### Create sitemap.xml
```xml
<?xml version="1.0" encoding="UTF-8"?>
<urlset xmlns="http://www.sitemaps.org/schemas/sitemap/0.9">
  <url>
    <loc>https://resumebuilder.com/</loc>
    <lastmod>2024-10-12</lastmod>
    <priority>1.0</priority>
  </url>
  <url>
    <loc>https://resumebuilder.com/tips</loc>
    <lastmod>2024-10-12</lastmod>
    <priority>0.8</priority>
  </url>
  <url>
    <loc>https://resumebuilder.com/about</loc>
    <lastmod>2024-10-12</lastmod>
    <priority>0.7</priority>
  </url>
</urlset>
```

Place in `public/sitemap.xml`

### Create robots.txt
```text
User-agent: *
Allow: /
Disallow: /admin

Sitemap: https://resumebuilder.com/sitemap.xml
```

Place in `public/robots.txt`

## 🌐 Domain Setup

### Recommended Domain Registrars
- Namecheap (cheap, good service)
- GoDaddy (popular, expensive)
- Google Domains (integrated with Google)
- Route53 (if using AWS)

### Domain Ideas
- resumebuildermnc.com
- mnc-resume-builder.in
- freeresumenow.in
- resumeaidx.com
- resumeforge.in

### DNS Configuration (for Vercel)
After registering domain:
1. Go to domain registrar
2. Find DNS settings
3. Add Vercel nameservers:
   - ns1.vercel-dns.com
   - ns2.vercel-dns.com
   - ns3.vercel-dns.com

## 📊 Post-Launch Setup

### Google Search Console
1. Go to search.google.com/search-console
2. Add property (your domain)
3. Verify ownership
4. Submit sitemap
5. Monitor search performance

### Google Analytics 4
1. Create GA4 property
2. Add tracking ID to site
3. Set up conversion events
4. Create custom dashboards
5. Monitor traffic sources

### Monitoring & Alerts
- Set up uptime monitoring (UptimeRobot free)
- Monitor error rates
- Track revenue (AdSense dashboard)
- Monitor traffic (Analytics)

## 💰 Cost Breakdown

### Monthly Costs
| Service | Cost | Notes |
|---------|------|-------|
| Domain | $10-15 | Annual, varies by registrar |
| Hosting (Vercel) | $0 | Free tier |
| CDN | $0 | Included in Vercel |
| Email | $0-5 | Use Gmail free, or Zoho mail |
| SSL Certificate | $0 | Free with Vercel |
| **Total** | **$0-1.25** | Per month (domain amortized) |

### Optional Services
- Email marketing (Mailchimp): $0-20/month
- Advanced analytics (Mixpanel): $0-25/month
- Ad optimization (Ezoic): 10-20% of earnings

## 🔐 Security Checklist

- [ ] HTTPS enabled (automatic with Vercel)
- [ ] Security headers configured
- [ ] No sensitive data in code
- [ ] Environment variables for secrets
- [ ] Regular backups of database (if used)
- [ ] Privacy policy page
- [ ] GDPR compliance (if EU users)
- [ ] Cookie consent banner (recommended)

## 📈 Post-Launch Optimization

### Week 1
- Monitor uptime and errors
- Check analytics setup
- Verify AdSense installation
- Test on different devices
- Get first 100 users

### Month 1
- Analyze user behavior
- Optimize form based on drop-off
- Fix any bugs reported
- Publish 3-5 blog posts
- Start organic promotion

### Month 3
- Scale content marketing
- Optimize for keywords
- Analyze revenue sources
- Plan phase 2 features
- Consider paid ads

## 🚨 Troubleshooting

### Build Errors
```bash
# Clear cache and reinstall
rm -rf node_modules package-lock.json
npm install
npm run build
```

### Deployment Issues
```bash
# Check build logs
npm run build --verbose

# Verify dist/ folder has files
ls -la dist/

# Test locally first
npm run preview
```

### Performance Issues
- Use Lighthouse (Chrome DevTools)
- Check Time to First Byte (TTFB)
- Optimize images
- Enable gzip compression
- Consider CDN (Cloudflare free tier)

### AdSense Not Loading
- Verify ad code is correct
- Check browser console for errors
- Wait 24-48 hours after code addition
- Ensure domain is verified
- Check AdSense policies

## 📞 Support Resources

- **Astro Docs:** https://docs.astro.build
- **Vercel Docs:** https://vercel.com/docs
- **Google AdSense Help:** https://support.google.com/adsense
- **SEO Guide:** https://developers.google.com/search/docs

---

**Ready to deploy?** Choose your hosting provider above and follow the steps!
