# pix-automatico-guardrails-qa
Pix Automatic guardrails QA
This project demonstrates the design and validation of regulatory guardrails for Pix Automático managed subscriptions. The feature required enforcing 48-hour processing locks and 7-day rolling regulatory restrictions while operating under real-time constraints without simulation capabilities.

pix-regulatory-guardrails-qa/
│
├── README.md
│
├── 01_Test_Strategy/
│     ├── Test_Plan.md
│     ├── Risk_Assessment.md
│
├── 02_Test_Design/
│     ├── Acceptance_Criteria.md
│     ├── Test_Cases.md
│     ├── Timeline_Model.md
│
├── 03_Test_Execution/
│     ├── Execution_Log_Template.xlsx
│
└── 04_Artifacts/
      ├── Sample_API_Response.json
      ├── Timeline_Diagram.png

# Business Problem
The payment provider does not natively support managed subscriptions.
To comply with banking regulations, the system simulates a weekly auto-renew subscription model while allowing manual seller-triggered charges.

Regulatory requirements:
Only one payment attempt every 7 days
No subscription modification during the regulatory window
No concurrent charge attempts during processing
This created a hybrid behavioral model requiring strict backend guardrails.

# QA Challenges
- No time manipulation in lower environments
- No charge simulation capability
- 7-day real-time validation cycles
- Rolling time-window enforcement
- Backend workaround behavior (non-native subscription model)
- Multi-channel restriction enforcement

# Testing Strategy 
To address constraints, the following strategy was designed: 
- Parallel subscription testing to stagger validation windows
- Precise UTC timestamp logging
- Boundary validation at exactly 168 hours
- Channel consistency verification (UI, API, admin tools)
- Negative testing for guardrail enforcement
- Cycle reset validation after new charge initiation

# Deliverables
This repository includes:
Test Plan
Acceptance Criteria
Detailed Test Cases
Risk Assessment
Timeline Model
Execution Strategy
API validation examples

# Skills Demonstrated 
- Regulatory compliance testing
- Time-based logic validation
- Rolling window testing
- Boundary testing
- Cross-channel validation
- Risk-based test design
- Requirement traceability
- API negative testing
- QA strategy under constraints

# Tools & Practices
Test management methodology compatible with Xray (Jira)
REST API validation
Structured documentation approach
Evidence-based validation
Risk-first planning

# Lessons Learned
Time-based features require environment flexibility for efficient regression.
Rolling windows must always be tested at exact boundary timestamps.
Regulatory logic must be enforced at backend level, not only UI.
When simulation is unavailable, test execution strategy becomes as important as test design.
