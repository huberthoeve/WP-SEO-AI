# Auth mechanism

Type: grilling
Status: resolved

## Question

Since the app already needs a LinkedIn connection to publish, should "Sign in with LinkedIn" be the only login method?

## Answer

Yes — LinkedIn OAuth only. One connection serves as both login and the publishing permission: no separate auth provider needed, which also fits the free-tier hosting constraint. (See the LinkedIn API/OAuth research ticket for whether the scopes needed for this are realistically obtainable.)
