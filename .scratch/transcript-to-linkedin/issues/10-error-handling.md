# Error handling for failed generations and publishes

Type: grilling
Status: resolved

## Question

What should happen when the app encounters errors at key points in the flow (angle extraction, post generation, LinkedIn publish)?

## Answer

- **Angle extraction fails:** Show error message to user with option to retry.
- **Post generation fails (for a specific angle):** Show error next to that post with immediate retry option.
- **LinkedIn publish fails:** Show error with immediate retry option. If retry fails, auto-save the draft back to history so user can retry from the history view later.
