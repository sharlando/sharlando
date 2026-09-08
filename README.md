# Sharlando Forbes

**IT program and controls work — the analysis between auditors, engineers, and management.**

I build tools for the parts of IT governance that are evidence-heavy and usually done by
hand: compliance assessment, financial controls testing, and cloud cost accountability.
Eight-plus years across military IT operations, financial operations, and consumer goods
manufacturing, currently based in Rochester, NY.

M.S. Information Technology Management · PMP · Security+ · Network+ · Active Secret Clearance ·
U.S. Army Veteran

---

## Projects

### [poam-forge](https://github.com/sharlando/poam-forge) — NIST SP 800-171 assessment

Reconciles what an organization claims about its security controls against what its
scanners actually report, then generates the SPRS score, POA&M, and assessment report a
DoD contractor has to produce. A control marked *implemented* while an open high-severity
finding maps to it scores as *not implemented*, and the report explains every
disagreement.

Remediation is ranked by SPRS points recovered, so the plan leads with the work that moves
the score most. All 110 controls ship as a swappable JSON catalog.

`Python` · `NIST 800-171` · `CMMC` · `SPRS` · `zero dependencies`

### [sod-sentinel](https://github.com/sharlando/sod-sentinel) — Segregation of duties analysis

Reads user, role, and entitlement extracts and reports who can complete a fraud scheme
without a second party — create a vendor and pay it, apply cash and issue the credit memo
that hides it, add an employee and run payroll.

20 rules across procure-to-pay, order-to-cash, payroll, financial reporting, and IT general
controls, each carrying the scheme it prevents and the compensating controls for when
duties genuinely cannot be split. Also finds terminated staff with live access, dormant
credentials, and entitlement outliers surfaced by comparing people against their
departmental peers.

`Python` · `SOX` · `ITGC` · `access reviews` · `zero dependencies`

### [cloud-steward](https://github.com/sharlando/cloud-steward) — AWS cost allocation and tag governance

Turns a Cost and Usage Report into a chargeback ledger that reconciles to the invoice, a
tag compliance scorecard measured in dollars rather than resource counts, and a ranked list
of savings opportunities.

Untagged spend is reported as its own line rather than swept into shared costs — the
shortcut that balances the ledger while destroying the only metric that drives tagging, and
that quietly makes disciplined teams subsidize the rest.

`Python` · `FinOps` · `AWS` · `chargeback` · `zero dependencies`

---

## How these are built

All three are standard library only. No `pip install`, no lockfile, no supply chain.
That is not minimalism for its own sake — these are tools for locked-down environments
where installing a package requires a change request, and often where the host cannot
reach a package index at all.

Each one is fully tested (246 tests across the three), runs in CI against Python 3.9
through 3.12, and ships with synthetic sample data so the whole pipeline can be run in one
command after cloning. The rules, catalogs, and policies are JSON data files rather than
hardcoded logic, so a controller or assessor can tune them without touching Python.

Where a number depends on an authority I cannot verify — the exact DoD control weights, real
AWS pricing — the documentation says so plainly and the tool reports its own provenance
rather than implying precision it does not have.

---

## Background

| | |
| --- | --- |
| **Now** | IT operations and risk, U.S. Army Reserve |
| **Before that** | Accounts Receivable / Financial Operations, Refresco Beverages |
| | Financial Analyst, Guardsman Group (Kingston, Jamaica) |
| **Education** | M.S. Information Technology Management, WGU (2025) |
| | B.S. Information Technology, WGU (2024) |
| | B.S. Computer Science, University of Technology, Jamaica (2015) |
| **Certifications** | PMP · CompTIA Security+, Network+, A+ · AWS Cloud Practitioner |
| | Google Cybersecurity · ITIL Foundation · Linux Essentials |

The through-line across finance and IT is the same problem in different clothes: someone
has to prove a control is working, and the evidence is scattered across systems that were
never designed to be read together.

---

📍 Rochester, NY · 🔗 [LinkedIn](https://www.linkedin.com/in/sharlando-forbes-84108b1b4)
