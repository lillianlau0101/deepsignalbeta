# 🚀 Stock Monitoring Agent

> [!TIP]
> This agent follows a **Fetch → Filter → Synthesize → Deliver** pipeline.

### 📂 Directory Structure
```text
stock-agent-backend/
├── src/
│   ├── agents/
│   │   └── researchAgent.js    <-- Gemini 3.1 Pro Logic
│   ├── services/
│   │   ├── newsService.js      <-- API calls to News/Earnings
│   │   └── mailService.js      <-- Sending the newsletter
│   ├── routes/
│   │   └── subscription.js     <-- Stripe $1/$5 logic
│   ├── templates/
│   │   └── newsletter.html     <-- The UI/UX for the email
│   └── app.js                  <-- Entry point
├── .env                        <-- API Keys (Gemini, Stripe, etc.)
├── package.json
└── README.md


Logic Breakdown (Visual View)
Diff
+ GREEN: Successful Data Fetching (Polygon.io / NewsAPI)
- RED: High-Risk Market Signals (Analyzed by Gemini)
! ORANGE: Upcoming Earnings Catalysts
@@ PURPLE: Personalized Delivery (Resend API) @@
