# Acceptance Criteria

## Subscription Creation

Given a customer purchases a Pix Automatico subscription  
When the checkout is completed successfully  
Then the subscription must be created in the system  
And the next renewal should be scheduled according to the simulated weekly cycle.

---

## Subscription Change Allowed

Given a subscription is active  
When 9 days have passed since the last charge  
Then the seller should be able to perform changes such as upgrade or downgrade.

---

## Guardrail Blocking Period

Given a subscription has passed the modification window  
When the guardrail period begins  
Then subscription changes and charges should be blocked.

---

## Guardrail Enforcement

If a seller attempts to change a subscription during the blocking period  
Then the system should reject the change request.

---

## Renewal Behavior

Given the backend simulates a weekly renewal cycle  
Then the system should correctly notify Ebanx as if the subscription were weekly auto-renew.
