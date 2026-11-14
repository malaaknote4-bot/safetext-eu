# SafeText EU: AI Scam Message Detector

**Veritas AI Hackathon 2026, finance track**

Paste a suspicious text message and find out in seconds if it's a scam, and why.

## The problem

One in four people in the EU have been tricked by messages or emails into sending money, paying for something or giving away personal data (EU Agency for Fundamental Rights, 2026). Text-message phishing rose tenfold in one year (BioCatch, 2025).

## What it does

1. The user pastes any message: SMS, WhatsApp, email, in any EU language.
2. An AI model analyses it for scam signals: look-alike links, urgency and threats, money or code requests, brand or family impersonation.
3. The user gets:
   - a **risk score** (0–100) and a verdict: *Scam*, *Suspicious* or *Looks safe*
   - the **red flags** found, pointing to the exact part of the message
   - **what to do next**, including where to report it

## How it works

- `index.html` is the whole app: one self-contained web page (HTML, CSS, JavaScript).
- **AI analysis:** the page sends the message to a large language model (Claude) with a fraud-analyst prompt focused on European scam patterns. The model returns structured JSON (score, verdict, scam type, impersonated brand, language, red flags, advice), which the page displays.
- **Fallback:** if the AI is unavailable, a rule-based checker scans for links, urgency words, payment requests, verification requests and "Hi Mum" patterns, so the app always gives an answer.
- Six built-in example messages for testing: five European scams (parcel fee, bank alert, "Hi Mum", French tax refund, German bank TAN) and one genuine message.

## Live demo

https://claude.ai/artifact/BzSxc236GUfTzFCPir4zLG

## Next steps

- WhatsApp checker: forward a message, get the verdict back in the chat
- Pilot inside a European bank's app
- Alerts on new scam waves for banks and users

## Sources

- FRA, *Online fraud: people's experiences across the EU*, 2026
- BioCatch, *Global Scams Report*, October 2025
- MEF consumer survey on SMS fraud, 2025
- UK Finance, *Annual Fraud Report 2026*
