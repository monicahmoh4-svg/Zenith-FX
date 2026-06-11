# ZenithFX — Trade The World 🚀

> Africa's premier online trading platform. Trade Synthetic Indices, Forex, Crypto, Commodities and more. Deposit via M-Pesa. Start with a free demo account.

---

## 🌐 Live Demo
Deployed at: [https://zenithfx.vercel.app](https://zenithfx.vercel.app)

---

## 📁 Project Structure

```
zenithfx/
├── index.html        # Landing page (marketing site)
├── app.html          # Full trading platform application
├── vercel.json       # Vercel deployment configuration
├── README.md         # This file
└── assets/           # (optional) images, icons
```

---

## ✨ Features

### Trading Platform
- 📈 **Live Price Charts** — Real-time streaming with EMA, SMA, Bollinger Bands, RSI
- 🎲 **Synthetic Indices** — V10, V25, V50, V75, V100, Boom 1000, Crash 1000, Step, Jump, Drift
- 💱 **Forex** — EUR/USD, GBP/USD, USD/KES, GBP/KES, EUR/KES, USD/NGN and more
- ₿ **Crypto** — BTC, ETH, SOL, BNB, XRP, ADA, DOT
- 🥇 **Commodities** — Gold, Silver, Crude Oil, Natural Gas, Platinum
- 📊 **Indices** — S&P 500, NASDAQ, DAX, FTSE, Nikkei, NSE 20

### Trading Tools
- Binary Options (Rise/Fall, Even/Odd, Match/Differ, Over/Under, Touch/No Touch)
- Multiplier & Accumulator contracts
- 8 timeframes (1s to 4h)
- Digit barrier selector with live probability bars
- DBot visual automation builder (no-code)
- Copy Trading with live trader stats
- Trade Journal with full history & CSV export
- Open Positions panel with real-time P&L

### Finance
- 📱 **M-Pesa deposits** via Lipana.dev (STK Push, instant)
- 💳 Card, Bank Transfer, Airtel Money, Crypto, Skrill
- Instant withdrawals back to M-Pesa
- KES ↔ USD conversion at live rates

### Account Features
- Demo account ($10,000 virtual, unlimited resets)
- Live account with real money trading
- KYC verification flow (6 steps)
- Affiliate program (up to 45% commission)
- Loyalty tiers (Bronze → Silver → Gold → Platinum)
- Trade Journal & performance analytics
- Market News & Economic Calendar
- Settings (theme, notifications, trading prefs, privacy)

---

## 🚀 Deploy to Vercel (Recommended)

### Option 1: Deploy via Vercel CLI

```bash
# Install Vercel CLI
npm install -g vercel

# Navigate to project folder
cd zenithfx

# Deploy (follow prompts)
vercel

# Deploy to production
vercel --prod
```

### Option 2: Deploy via GitHub + Vercel Dashboard

1. **Push to GitHub** (see below)
2. Go to [vercel.com](https://vercel.com) → New Project
3. Import your GitHub repository
4. Framework: **Other** (Static HTML)
5. Output directory: **.** (root)
6. Click **Deploy**

---

## 📤 Push to GitHub

```bash
# Initialize git repo
git init
git add .
git commit -m "feat: initial ZenithFX trading platform"

# Create repo on GitHub (via github.com or gh CLI)
gh repo create zenithfx --public --push

# OR manually:
git remote add origin https://github.com/YOUR_USERNAME/zenithfx.git
git branch -M main
git push -u origin main
```

---

## 🔧 Local Development

No build step required — pure HTML/CSS/JS.

```bash
# Option 1: Python simple server
python3 -m http.server 3000

# Option 2: Node http-server
npx http-server . -p 3000

# Option 3: VS Code Live Server extension
# Right-click index.html → Open with Live Server
```

Open [http://localhost:3000](http://localhost:3000)

---

## 🔌 M-Pesa Integration (Lipana.dev)

The platform is pre-wired for Lipana.dev M-Pesa integration.

To go fully live with real M-Pesa payments:

1. Sign up at [lipana.dev](https://lipana.dev)
2. Get your API key and callback URL
3. Create a backend endpoint (Node.js/Python/PHP) that:
   - Initiates STK Push via Lipana.dev API
   - Receives payment confirmation webhook
   - Updates user balance in your database
4. Replace the `procDeposit()` function in `app.html` with real API calls

**Lipana.dev STK Push example:**
```javascript
// POST https://api.lipana.dev/v1/stk-push
const response = await fetch('https://api.lipana.dev/v1/stk-push', {
  method: 'POST',
  headers: {
    'Authorization': 'Bearer YOUR_LIPANA_API_KEY',
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    phone: '254712345678',
    amount: 1000,
    reference: 'ZFX-DEP-001',
    description: 'ZenithFX Deposit'
  })
});
```

---

## 🔐 Production Checklist

Before going fully live:

- [ ] Connect real M-Pesa API via Lipana.dev
- [ ] Set up backend/database (Firebase, Supabase, or custom)
- [ ] Implement real user authentication (JWT/sessions)
- [ ] Connect real market data feed (WebSocket price stream)
- [ ] Set up KYC document upload (AWS S3 / Cloudinary)
- [ ] Implement real trade execution engine
- [ ] Add real withdrawal processing
- [ ] Set up email notifications (SendGrid/Mailgun)
- [ ] Configure SSL certificate (auto on Vercel)
- [ ] Set up monitoring (Vercel Analytics / Sentry)
- [ ] Add rate limiting and fraud detection
- [ ] Register with relevant financial regulators

---

## 📞 Support

- Email: support@zenithfx.io
- Twitter: @ZenithFX
- Telegram: t.me/ZenithFX

---

## ⚠️ Risk Disclaimer

Trading binary options, forex and CFDs involves significant risk. Past performance is not indicative of future results. Only trade with money you can afford to lose.

---

*Built with ❤️ for Africa's trading community*
