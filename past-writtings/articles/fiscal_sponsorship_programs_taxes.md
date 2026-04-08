# Fiscal Sponsorship Programs and Tax Handling (for Farms & Community Projects)

> **Scope:** This document explains fiscal sponsorship as a *tax + governance* arrangement and the operational implications for payment processing, bookkeeping, and compliance.
>
> **Not legal or tax advice.** It is a technical/operational overview meant to help you structure policies, data capture, and reporting.

---

## 1) What fiscal sponsorship is (and what it is not)

**Fiscal sponsorship** is an arrangement where an established **501(c)(3)** nonprofit (the **sponsor**) accepts charitable donations and manages funds on behalf of a mission-aligned project (the **project**) that is not itself a standalone charity. The sponsor provides fiduciary oversight and remains responsible for compliance. citeturn0search0turn0search1

Key implication: **donations are legally made to the sponsor**, under the sponsor’s EIN and financial systems. The sponsor must retain **final discretion and control** over funds to avoid “conduit”/earmarking problems that can jeopardize deductibility. citeturn0search12turn0search2

### Common confusion
- **Not “renting an EIN.”** A reputable fiscal sponsorship program is a governance and controls framework, not a payment pass-through.
- **Not donor-controlled escrow.** Donors can express intent/designation, but the sponsor must retain authority. citeturn0search12turn0search2

---

## 2) Why it matters in agriculture and local food projects

Many farms and community initiatives have public-benefit goals (education, conservation, access programs, infrastructure) but lack:
- tax-exempt status for deductible fundraising,
- administrative capacity for compliance,
- and repeatable reporting that funders trust.

Fiscal sponsorship can unlock compliant fundraising while keeping governance centralized in a sponsor and operations distributed across projects.

---

## 3) Two dominant operating models (practical framing)

Fiscal sponsorship is implemented in multiple forms; two common ones are:

### A) “Comprehensive” sponsorship (often called Model A)
- The project is treated as a program of the sponsor.
- Sponsor typically runs payroll/contracting, owns the project’s assets, and provides oversight.

### B) “Pre-approved grant relationship” (often called Model C)
- Sponsor receives donations and makes grants to the project entity subject to grant controls.
- Used when the project is a separate legal entity but needs deductible fundraising.

The right model affects: liability, HR, contracting, procurement, and how “project accounts” are represented in bookkeeping and dashboards. citeturn0search9turn0search5

> **Implementation note:** For your website/payment architecture, both models benefit from identical *data capture* (designation, restrictions, conditions, documentation), even if disbursement differs.

---

## 4) Donation types and what your system must track

Your platform should treat donation intake as **sponsor-centric**, with project metadata layered on top.

### 4.1 Unrestricted donations
Donations for the sponsor’s general mission.
- No project designation required.
- Used for general operations and broad programs.

### 4.2 Restricted / designated donations (donor intent)
Donor expresses intent (e.g., “Farm Infrastructure Fund”).
- **You must capture and retain the designation intent** (for reporting and internal controls).
- Sponsor publishes policy language on how designations are handled and retains discretion. citeturn0search12turn0search5

### 4.3 Conditional donations
Donations contingent on events or milestones (match requirements, construction milestones, etc.).
- Funds may need to be held and recognized according to conditions.
- Requires explicit documentation and a release workflow.

**Minimum donation metadata fields (recommended):**
- sponsor_id
- project_id (or designation_id)
- donation_type: unrestricted | restricted | conditional
- restriction_text / designation_label (as shown to donor)
- condition_text (if any)
- donor_contact fields (for receipts and audit)
- payment_processor_txn_id
- acknowledgement_status + timestamp
- refund_void_chargeback flags

---

## 5) Payment processing architecture aligned with fiscal sponsorship

### 5.1 Payment Processing Overview (from the provided page structure)
Goal: a simple, reliable payment foundation for **community-driven enterprises**, where the sponsor can unify:
- online donations,
- designated giving,
- and in-person POS transactions,
under one sponsor-controlled account (EIN-aligned).

### 5.2 Trusted payment processing (why a default like PayPal is practical)
A “default” processor can reduce friction while you standardize workflows and data capture:
- fast onboarding + donor familiarity,
- exportable transaction reporting,
- reusable payment experiences across multiple project pages.

### 5.3 Designed for fiscal sponsorship (designation intent vs legal control)
In fiscal sponsorship, donations are to the sponsor. Your system can still capture donor designation intent **without implying donor control**:
- receipts show sponsor as recipient,
- designation field is clearly labeled as “intent/designation,”
- sponsor policies govern how restricted funds are administered. citeturn0search12turn0search5

### 5.4 POS and in-person transactions (keeping sales vs donations distinct)
For markets and farms that do both:
- **Retail sales** (potentially taxable, inventory-linked)
- **Charitable donations** (receipt/acknowledgment, restriction handling)

Your reporting should support:
- unified dashboards (total activity),
- separate ledgers/tags (sales vs donations),
- reconciled exports for bookkeeping.

### 5.5 Donation box module (data capture + repeatability)
A “donation box” widget is useful if it:
- routes payments through the sponsor’s processor,
- captures designation + donor metadata consistently,
- triggers receipt workflows,
- supports sponsor-level aggregated reporting while preserving per-project breakdowns.

### 5.6 Contingencies & alternatives (no hard lock-in)
A core design principle: **separation of concerns**
- Payments are handled by the processor.
- Program/project data lives in the sponsor’s (or your client’s) system.

That makes it feasible to swap processors or add methods (ACH, recurring, event payment flows) without rebuilding fundraising logic.

---

## 6) Sponsor obligations (what must exist for compliance)

A sponsor is responsible for financial/legal oversight and adequate systems to manage risk and reporting; best-practice guidelines emphasize governance, financial controls, and transparency. citeturn0search5turn0search0

Minimum sponsor-side controls to reflect in your tooling:
- written fiscal sponsorship agreement (per project),
- restricted funds policy (what “designation” means, how changes/refunds are handled),
- approval workflow for expenses/disbursements,
- documentation requirements (invoices, receipts, grant reports),
- audit-ready transaction trails.

---

## 7) Practical workflows your software should support

### Workflow A: Intake → Designation → Receipt
1. donor pays sponsor via donation widget
2. system records donor intent + restriction category
3. receipt/ack issued by sponsor (or sponsor-approved template)
4. transaction reconciled to bookkeeping tags/classes/funds

### Workflow B: Spending/disbursement for a designated project
1. project submits expense request with documentation
2. sponsor approves/denies (policy-based)
3. sponsor pays vendor OR reimburses OR regrants (model-dependent)
4. expense is tagged to the same designation/fund for reporting

### Workflow C: Multi-project sponsor dashboard
- per-project totals (in/out)
- restriction status (restricted vs unrestricted vs conditional)
- budget vs actual
- time-based reporting (month/quarter/year)
- export packets for auditors/funders

---

## 8) Checklist for implementation (site + operations)

### Sponsor program setup
- define eligible project types and prohibited uses
- publish public language: “donations are to sponsor; designations are intent”
- define restricted funds handling rules

### Payment setup
- sponsor-controlled payment account(s)
- standardized donation page language
- consistent designation picklists (project list) + freeform notes as secondary

### Bookkeeping + reporting
- chart-of-accounts mapping
- fund/class/tag strategy (per project and per restriction category)
- export format + cadence
- exception handling: refunds, chargebacks, mis-designations

---

## Appendix: Useful references
- Council of Nonprofits — fiscal sponsorship overview citeturn0search0
- National Network of Fiscal Sponsors (NNFS) + guidelines PDF citeturn0search1turn0search5
- IRS-related framing on donor control / conduit risk citeturn0search2turn0search12
