# Deploy — Second Story Trades

Static site. Nothing to build.

## Vercel
1. In your Contractor Envy Vercel account: New Project → import this folder (or drag-drop) → Deploy. No build command needed (it's static).
2. Add domain: Project → Settings → Domains → add **secondstorytrades.org**, then point the domain's DNS to Vercel (A record or Vercel nameservers).

## Wire the form to your existing connections
- In GoHighLevel, create an **Inbound Webhook** trigger (or use an existing CE endpoint).
- Open `index.html`, find `FORM_ENDPOINT`, and paste that webhook URL.
- Build a GHL workflow off that webhook: create/Update Contact → send you an SMS (Blooio) + email → auto-reply the requester.
- The form posts JSON with: requester_type, contact_name, org_name, phone, email, city, state, scope, description, consent, source, submitted_at.

## Fill in before launch
- `[GOFUNDME LINK]` (index.html — Support button)
- `[Your phone]`, `[Your email]` (footer)
- `FORM_ENDPOINT` (index.html script)
