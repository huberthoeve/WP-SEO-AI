# LinkedIn API/OAuth requirements for posting on behalf of users

Type: research
Status: open

## Question

What does it actually take for this app to publish LinkedIn posts on a user's behalf via the LinkedIn API? Specifically:

- Which OAuth scopes are required (e.g. `w_member_social`, OpenID Connect `Sign In with LinkedIn`)?
- Does LinkedIn require a developer program tier or app review/approval before those scopes are grantable, and how long does that take?
- Are there rate limits or usage caps on posting that would affect a small app?
- Any cost associated with API access itself (separate from hosting/LLM costs)?
- Does this reasonably support "sign in with LinkedIn" doubling as both auth and the publishing grant in one OAuth connection?

This blocks the tech-stack ticket (token storage requirements depend on the answer) and is a scope risk: if direct publish isn't realistically obtainable, the destination may need to fall back to a copy/paste flow.
