# DVLA Recon

## Tools exposed
- GetCurrentUser - resolves the current user
- GetUserTransactions(user_id) - takes a user ID parameter

## ReAct loop observed
hi! -> GetCurrentUser -> GetUserTransactions : 1 -> Complete

## My baseline transactions (user 1)
| ID | Reference | Recipient | Amount |
|----|-----------|-----------|--------|
| 1 | DeLoreanParts | AutoShop | $1000 |
| 2 | SkateboardUpgrade | SportsStore | $150 |

## Thesis
The model chooses which tool to call and with what arguments from text
it can't fully separate from user input. That's the attack surface.

## Attack idea for Unit 3
GetUserTransactions takes a user_id — try to make the agent call it
with an ID that isn't mine. Cross-user data access.