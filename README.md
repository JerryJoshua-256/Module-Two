# Module 2 Urban Design Quiz — Vercel deployment

Responsive 20-question quiz with one-question-at-a-time navigation, immediate feedback, final score, review and retry. The Vercel serverless function emails completed results to olaniyijerry20@gmail.com.

## Enable score emails
1. Create accounts at https://vercel.com and https://resend.com.
2. Push this project to GitHub and import it into Vercel. Deploy.
3. Create a Resend API key. For public use, verify a sending domain in Resend.
4. In Vercel → Project → Settings → Environment Variables, set `RESEND_API_KEY` and `QUIZ_FROM_EMAIL` (e.g. `Urban Design Quiz <quiz@your-verified-domain.com>`).
5. Redeploy.

Each completion sends participant name (optional), score, percentage, timestamp and answer breakdown. The API key is server-side, not exposed in the browser. The fallback sender `onboarding@resend.dev` is for development only and may be restricted to your Resend account. Live email delivery has not yet been tested; valid Resend credentials and a verified sender are required. Add rate limiting/bot protection before wide public distribution.

Open `index.html` for a frontend preview; sending email requires Vercel deployment and configuration.
