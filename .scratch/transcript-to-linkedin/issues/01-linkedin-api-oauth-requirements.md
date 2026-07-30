# LinkedIn API/OAuth requirements for posting on behalf of users

Type: research
Status: resolved

## Question

What does it actually take for this app to publish LinkedIn posts on a user's behalf via the LinkedIn API? Specifically:

- Which OAuth scopes are required (e.g. `w_member_social`, OpenID Connect `Sign In with LinkedIn`)?
- Does LinkedIn require a developer program tier or app review/approval before those scopes are grantable, and how long does that take?
- Are there rate limits or usage caps on posting that would affect a small app?
- Any cost associated with API access itself (separate from hosting/LLM costs)?
- Does this reasonably support "sign in with LinkedIn" doubling as both auth and the publishing grant in one OAuth connection?

This blocks the tech-stack ticket (token storage requirements depend on the answer) and is a scope risk: if direct publish isn't realistically obtainable, the destination may need to fall back to a copy/paste flow.

## Answer

Technically feasible for a solo/indie project, no hard blockers confirmed — but one real ambiguity remains that needs a hands-on check, not just more reading.

Confirmed from LinkedIn's own docs:
- Posting needs the `w_member_social` scope (a separate "Share on LinkedIn" product); sign-in is a different product/scope set (`openid`/`profile`/`email`). Both can be requested together in one OAuth consent screen.
- No monetary fee for API access today.
- No follower-count or Marketing-Partner gate for this scope.
- Every app must be tied to a verified LinkedIn company Page (super-admin approval) — real friction, but free and surmountable for an indie dev.
- Rate limits are app/endpoint-specific and only visible in the Developer Portal — no published fixed number to design around yet.

Unresolved: LinkedIn's docs are internally inconsistent about whether `w_member_social` is still plain self-serve/instant, or whether it now routes through "Community Management App Review" — which is explicitly scoped to registered legal organizations doing commercial integrations (business details + screen-recorded OAuth demo required). This couldn't be resolved from documentation alone.

Full findings with citations: branch `research/linkedin-api-oauth`, file `.scratch/transcript-to-linkedin/research/linkedin-api-oauth-findings.md`.

**Follow-up spawned:** a live Developer Portal test is needed to resolve the self-serve-vs-review ambiguity before the tech stack (token storage) ticket can be answered with confidence — see the new task ticket.
