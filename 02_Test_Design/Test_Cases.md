Subscription Change After Guardrail Period

## Objective
Validate that subscription changes are allowed after 9 days.

Day 0 -------- Day 9 -------- Day 18
Create        Change OK      Blocked

## Preconditions
- Pix Automatico subscription exists
- Subscription created successfully

## Steps

1. Wait 9 days after subscription creation
2. Attempt to upgrade the subscription
3. Submit the change

## Expected Result

- System allows the change
- Subscription upgrade is applied
- No guardrail error is triggered
