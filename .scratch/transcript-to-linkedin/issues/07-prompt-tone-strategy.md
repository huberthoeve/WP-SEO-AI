# Prompt/tone strategy for post variations

Type: grilling
Status: resolved

## Question

How should the app generate multiple LinkedIn post variations from a transcript — how many variations, what tones/angles should they cover, and how much should be derived automatically from the transcript vs. fixed presets?

## Answer

Two-stage generation flow, not a single-shot "3 variations":

1. **Angle extraction**: from the pasted/uploaded transcript, Claude extracts a flexible number of distinct angles/ideas (not a fixed count — however many the transcript actually supports). Each angle is a short pitch, not a full post.
2. **Post drafting**: the user browses the extracted angles and can turn any of them into a full LinkedIn post draft, one at a time, in any order — no restriction to picking just one angle per transcript. Generating a post from one angle doesn't discard the others.
3. The resulting draft is editable before publish (per the earlier "generate text, editable before publish" framing), then published immediately via the LinkedIn API — **no scheduling** (see Out of scope: scheduled/future-dated publishing is deferred past v1).

This changes the original destination wording from "several post variations" to this angle-then-post two-stage flow — updated on the map.
