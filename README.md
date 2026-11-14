# SafeText EU

**Got a weird text? Check it before you click.**
An AI scam message checker for people in Europe. Veritas AI Hackathon 2026, finance track.

## Why

One in four people in the EU have been tricked by messages or emails into sending money, paying for something or giving away personal data (EU Agency for Fundamental Rights, 2026). Text-message phishing rose tenfold in one year (BioCatch, 2025). Most victims never report it, so the same tricks keep working.

## What it does

Paste any SMS, WhatsApp or email message, in any EU language, and SafeText gives you:

- **A risk score (0–100)** and a clear verdict: scam, suspicious or safe
- **Highlighted red flags** shown directly inside the original message, with a short reason for each
- **What to do now**, including the right reporting route in Europe
- **A ready-to-send warning** to copy and share with family
- **Explanations in your language**: English, Swedish, German, French, Spanish, Italian, Dutch, Polish or Arabic

## How it works

`index.html` is the whole app: one self-contained web page (HTML, CSS, JavaScript), so it runs on any phone with no install.

1. The message and the chosen explanation language go into a prompt for a large language model (Claude). The prompt describes common European scam patterns: impersonation of banks, delivery firms, tax offices and family members; urgency; requests for money, codes or logins; look-alike links; too-good-to-be-true offers.
2. The model returns structured JSON: score, verdict, scam type, who it imitates, red flags with exact quotes from the message, next steps and a family warning.
3. The page draws a score gauge, highlights each quoted red flag inside the original message and lists the next steps.
4. **Fallback:** if the AI can't be reached, a rule-based quick check scans for suspicious links, time pressure, payment requests, detail requests, "Hi Mum" and job-scam patterns, so the user always gets an answer.

Six test messages are built in: German delivery fee, fintech card freeze, Swedish "Hi Mum", Italian parking fine, job/task scam, and a genuine one-time code.

## Live demo

https://claude.ai/artifact/UVuCwu86dwYbarhuGLpkHM

## Next steps

- A WhatsApp number you can forward suspicious messages to
- A pilot inside a European bank's app
- Alerts when a new scam wave starts spreading

## Sources

- FRA, *Online fraud: people's experiences across the EU*, 2026
- BioCatch, *Global Scams Report*, October 2025
