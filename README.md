# Anjali Love Nudge (Vercel + Resend)

A single-screen web app that greets **Anjali Tiwari** daily and lets you send a cute email nudge.

## Deploy (quick)
1. Create a new Git repo with these files.
2. Import into **Vercel** (Framework preset: Other).
3. In Vercel → Project → Settings → Environment Variables, add:
   - `RESEND_API_KEY` = your Resend API key
   - `FROM_EMAIL` = verified sender, e.g., `Love <noreply@yourdomain.com>`
   - `TO_EMAIL` = her email address, e.g., `anjali.tiwari@example.com`
   - `PASSCODE` = a secret to authorize email sends
4. Deploy. Open your site and test the **Send Nudge** button with the passcode.

## Optional
- Schedule a daily email using **Vercel Cron** to hit `/api/nudge` with your header (add a secret param or keep it manual).
- Add more lines (duplicate in `index.html` and `api/nudge.ts` to keep UI and email in sync).
