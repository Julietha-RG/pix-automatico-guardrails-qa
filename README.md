# pix-automatico-guardrails-qa
Pix Automatic guardrails QA
This project demonstrates the design and validation of regulatory guardrails for Pix Automático managed subscriptions. The feature required enforcing 48-hour processing locks and 7-day rolling regulatory restrictions while operating under real-time constraints without simulation capabilities.

Business Problem

The payment provider does not natively support managed subscriptions.
To comply with banking regulations, the system simulates a weekly auto-renew subscription model while allowing manual seller-triggered charges.

Regulatory requirements:

Only one payment attempt every 7 days

No subscription modification during the regulatory window

No concurrent charge attempts during processing

This created a hybrid behavioral model requiring strict backend guardrails.
