# Tech stack selection (framework, DB, LinkedIn token storage)

Type: grilling
Status: open
Blocked by: 01

## Question

Given the constraints — free hosting (Vercel-style), free tiers everywhere except the paid LLM API, and LinkedIn OAuth as the sole auth mechanism — what's the concrete stack for this app?

Needs to cover:
- Web framework (a Vercel-friendly choice, e.g. Next.js, is the default assumption but hasn't been confirmed)
- Database for storing accounts, transcripts, generated posts, and history (must have a workable free tier)
- Where/how LinkedIn OAuth tokens (and refresh tokens) get stored and refreshed

Blocked on the LinkedIn API/OAuth research ticket: the token storage and refresh requirements depend on what that scope/flow actually looks like.
