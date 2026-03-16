# Test Plan
Objective

## Validate regulatory guardrails for Pix Automático managed subscriptions, ensuring:

- 48-hour processing lock enforced
- 7-day regulatory lock enforced
- Subscription changes blocked during lock
- API responses match expected verbiage
- UI states reflect backend enforcement
- All testing must use real time progression.

## Key Constraints

- ❌ Cannot simulate payment events
- ❌ Cannot override timestamps
- ❌ Cannot bypass 7-day window
- ❌ Cannot mock EBANX behavior
- ⏳ Must wait real 7–9 days between charge attempts
