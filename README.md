# Fixology V3 - Enterprise AI Platform for Device Repair

## 🚀 Quick Start

### Deploy to Vercel (Recommended)

1. **Push to GitHub**
   ```bash
   git init
   git add .
   git commit -m "Fixology v3"
   git remote add origin https://github.com/YOUR_USERNAME/fixology.git
   git push -u origin main
   ```

2. **Connect to Vercel**
   - Go to [vercel.com](https://vercel.com)
   - Click "New Project" → Import your GitHub repo
   - Framework preset: "Other"
   - Root directory: `public`
   - Deploy!

3. **Add Environment Variables** (for chat API)
   - In Vercel dashboard → Settings → Environment Variables
   - Add: `OPENAI_API_KEY` = your OpenAI API key

4. **Connect Domain**
   - Settings → Domains → Add `fixologyai.com`
   - Update DNS records as instructed

---

## 📁 File Structure

```
fixology-v3/
├── public/
│   ├── index.html          # Homepage
│   ├── diagnose.html       # AI diagnosis page
│   ├── for-shops.html      # Shop SaaS landing
│   ├── devices.html        # Device support list
│   ├── pricing.html        # Pricing page
│   ├── styles/
│   │   ├── main.css        # Core design system
│   │   └── chat-widget.css # Chat widget styles
│   ├── js/
│   │   ├── main.js         # Core JavaScript
│   │   └── chat-widget.js  # AI chat widget
│   ├── api/
│   │   └── chat.js         # Backend API (Vercel function)
│   └── vercel.json         # Deployment config
└── README.md
```

---

## 🎨 Design System

### Colors
- **Lavender Gradient**: `#B48FFF → #8E75FF → #6B59FF`
- **Neon Cyan**: `#6DF7FF`
- **Background**: `#07070A` (near-black)
- **Cards**: `#16161D`

### Typography
- Font: Inter (Google Fonts)
- Weights: 300-800

### Components
- Buttons: `.btn`, `.btn-primary`, `.btn-secondary`, `.btn-cyan`
- Cards: `.card`, `.card-featured`, `.card-glow`
- Badges: `.badge`, `.badge-cyan`, `.badge-success`

---

## 🤖 Chat Widget Integration

### Option 1: Link to GPT (Current - No Backend Required)
The widget currently opens your Fixology GPT in a new tab. This works immediately.

### Option 2: Full Backend Integration
To enable in-site chat:

1. Deploy the `/api/chat.js` function
2. Add your `OPENAI_API_KEY` to Vercel
3. Update `chat-widget.js`:
   ```javascript
   const CONFIG = {
       apiEndpoint: 'https://fixologyai.com/api/chat',
       useBackendApi: true,  // Change to true
       // ...
   };
   ```

### Embedding the Widget
The widget auto-loads on every page via `chat-widget.js`. To disable on specific pages, remove the script tag.

---

## 📊 Metrics & Trust Signals

Current positioning uses these metrics:
- 100,000+ repair cases analyzed
- 500+ symptoms mapped
- 250+ causes identified
- 150+ diagnostic tests
- 50+ device models
- 93% accuracy (lab-verified)
- 10,000+ technicians

---

## 🔗 Important Links

- **Fixology GPT**: https://chatgpt.com/g/g-692e842d0dc48191989c1f877d00165d-fixology-repair-assistant
- **Domain**: fixologyai.com

---

## 📱 Pages Overview

| Page | URL | Description |
|------|-----|-------------|
| Homepage | `/` | Main landing with all trust signals |
| Diagnose | `/diagnose` | AI diagnosis + device tests |
| For Shops | `/for-shops` | SaaS platform landing |
| Devices | `/devices` | Supported devices list |
| Pricing | `/pricing` | Customer & shop pricing |

---

## 🛠️ Development

### Local Testing
```bash
cd public
npx serve
# Opens at http://localhost:3000
```

### Adding New Pages
1. Create `newpage.html` in `/public`
2. Add rewrite in `vercel.json`
3. Link from navigation

---

## 🔒 Security

- All pages include security headers
- No sensitive data stored client-side
- API keys only in server environment
- SOC 2 compliant messaging (aspirational)

---

## 📈 Analytics Setup

Add to each page before `</body>`:
```html
<!-- Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=G-XXXXXXXXXX"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'G-XXXXXXXXXX');
</script>
```

---

## 🎯 Next Steps

1. [ ] Deploy to Vercel
2. [ ] Connect fixologyai.com domain
3. [ ] Add OPENAI_API_KEY for chat backend
4. [ ] Set up Google Analytics
5. [ ] Create remaining pages (docs, blog, etc.)
6. [ ] Build actual Notion API integration

---

Built with 💜 by the Fixology team
