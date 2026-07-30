# Verify LinkedIn Developer Portal access path for w_member_social

Type: task
Status: resolved

## Question

LinkedIn's own documentation is internally inconsistent about whether the `w_member_social` posting scope (needed to publish on a member's behalf) is still plain self-serve/instant, or now effectively requires "Community Management App Review" — which is scoped to registered legal organizations doing commercial integrations. This couldn't be resolved from documentation alone (see the research findings linked from the LinkedIn API/OAuth research ticket).

This is a hands-on verification task, not something answerable by more reading:

1. Create a test app in the LinkedIn Developer Portal (requires a LinkedIn account and a company Page — any individual can create one for free).
2. Attempt to add both the "Sign In with LinkedIn using OpenID Connect" and "Share on LinkedIn" products to the test app.
3. Observe and record: does adding "Share on LinkedIn" grant `w_member_social` instantly, or does it trigger an application/review flow? If a review is triggered, record what it asks for (organization details, business legitimacy, etc.).

This is a HITL task — it requires a real LinkedIn account and company Page, which the agent cannot create or act through on your behalf. Record the outcome as the answer here when done; it determines whether the destination's "direct publish" feature is buildable as scoped, or needs to fall back to a copy/paste flow for v1.

## Answer

Verified directly in the LinkedIn Developer Portal: adding "Share on LinkedIn" alongside "Sign In with LinkedIn using OpenID Connect" granted `w_member_social` **instantly, self-serve, no review** — resolving the ambiguity from the research ticket in favor of the self-serve path. LinkedIn API credentials are now in hand. The destination's direct-publish feature is confirmed buildable as scoped; no fallback to copy/paste needed. This unblocks the tech-stack ticket.
