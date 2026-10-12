# Resume Builder for MNC Jobs

A free, mobile-friendly resume builder tailored for Indian MNC job placements. Built with Astro + CSS for optimal performance and SEO.

## 🎯 Features

- **Smart Resume Builder** - Form-based interface with real-time preview
- **ATS-Friendly Templates** - Designed to pass automated screening systems
- **Mobile Responsive** - Build resumes on any device
- **Instant PDF Download** - Generate professional PDFs in seconds
- **Interview & Tips Section** - Resume writing, interview prep, salary negotiation guides
- **Completely Free** - No sign-ups, no premium features

## 🚀 Quick Start

### Prerequisites
- Node.js 22.12.0 or higher
- npm or yarn

### Installation

```bash
# Install dependencies
npm install

# Start development server
npm run dev

# Build for production
npm run build

# Preview production build
npm run preview
```

The app will be available at `http://localhost:3000`

## 📁 Project Structure

```
resume-builder-mnc/
├── src/
│   ├── pages/
│   │   ├── index.astro          # Main resume builder
│   │   ├── tips.astro           # Tips & interview prep
│   │   └── about.astro          # About page
│   ├── layouts/
│   │   └── Layout.astro         # Base layout with AdSense setup
│   ├── components/
│   │   └── Navigation.astro     # Top navigation
├── public/                       # Static assets
├── dist/                         # Build output
├── package.json
├── astro.config.mjs
└── README.md
```

## 💰 Monetization Strategy

### 1. Google AdSense (Primary Revenue)
- **Top Banner Ad** - Above the main builder section
- **Middle Ad** - Between features and tips section
- **Bottom Ad** - After tips section

**Estimated Revenue:** $500-$2000/month with 10K-50K monthly users (CPM: $5-15 for Indian traffic)

### 2. Affiliate Marketing (Secondary Revenue)
- Resume writing courses (Udemy, Coursera)
- Interview preparation platforms
- Career counseling services
- Job portals and placement drives

### 3. Growth Strategy to Hit $10K/Month

**Traffic Targets:**
- 50K+ monthly unique visitors
- 100K+ page views
- 5000+ resume downloads

**SEO Target Keywords:**
- "Free resume builder India"
- "MNC resume template"
- "Resume builder for freshers"
- "ATS friendly resume"
- "Campus placement resume"

**Content Strategy:**
- Blog posts on resume writing (SEO)
- Interview question collections
- Company-specific guides (TCS, Infosys, etc.)
- Placement tips by engineering branch

**Promotional Channels:**
- Reddit (r/India, r/cscareerquestions)
- LinkedIn (career tips)
- Twitter threads
- College WhatsApp groups
- Career forums

## 🔧 Configuration

### Set Up Google AdSense

1. Replace `ca-pub-xxxxxxxxxxxxxxxx` in `src/layouts/Layout.astro` with your AdSense Publisher ID
2. Ensure site is approved by Google AdSense
3. Add proper content policy and privacy pages

### Set Up Analytics

Update `src/layouts/Layout.astro` with your Google Analytics ID

### Customize Branding

- `public/favicon.svg` - Site icon
- Site title and metadata in page frontmatter

## 📱 Mobile Optimization

- Responsive grid layout (adapts to all screen sizes)
- Touch-friendly form inputs
- Fast load times for slow connections
- Print-optimized for PDF generation

## 📊 Performance Metrics

- **Build time:** ~393ms
- **Page size:** Optimized for mobile (< 100KB per page)
- **SEO:** Mobile-friendly, semantic HTML, meta tags
- **Accessibility:** WCAG compliant

## 📋 Content Included

### Resume Builder
- Personal information form
- Education details
- Work experience section
- Technical skills input
- Projects section
- Real-time preview
- PDF download functionality

### Tips & Preparation
- **Resume Writing Guide** (action verbs, quantifying, formatting)
- **Interview Preparation** (STAR method, technical tips)
- **Salary Negotiation** (market research, compensation)

### About Page
- Mission and features
- How to get started
- Contact information

## 🚀 Deployment

### Deploy to Vercel (Recommended)
```bash
npm install -g vercel
vercel
```

### Deploy to Netlify
```bash
npm install -g netlify-cli
netlify deploy --prod --dir=dist
```

### Deploy to GitHub Pages
```bash
npm run build
# Push dist/ to gh-pages branch
```

## 📈 Revenue Projections

| Month | Users | Views | Revenue |
|-------|-------|-------|---------|
| 1     | 1K    | 5K    | $35     |
| 3     | 5K    | 20K   | $150    |
| 6     | 20K   | 100K  | $700    |
| 12    | 50K   | 250K  | $1700   |

*To reach $10K/month, consider:*
- Premium resume templates
- Career coaching service
- Job listing partnerships
- Corporate bulk licenses

## ⚠️ Important Notes

1. **AdSense Approval**: Minimum traffic and original content required
2. **Content Quality**: Regular updates increase SEO ranking and revenue
3. **User Experience**: Balance monetization with UX
4. **Privacy**: Clear privacy policy and terms of service required
5. **Legal**: Compliance with Indian data protection laws

## 📝 License

MIT License

## 🤝 Contributing

Contributions welcome! Areas for improvement:
- Additional resume templates
- Dark mode
- Multiple language support
- Job application tracker
- LinkedIn integration

---

Built with ❤️ for Indian job aspirants | Made with Astro
