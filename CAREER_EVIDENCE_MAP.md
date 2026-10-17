# Career Evidence Map

**Beth Gerharts | Cloud GRC**
[Portfolio](https://beth-gerharts-grc.vercel.app/) | [LinkedIn](https://linkedin.com/in/beth-gerharts) | bethgerharts@protonmail.com

This map connects common GRC job requirements to the work that proves them. Each row links to something you can open and check. Rows marked **In progress** or **Not yet demonstrated** are listed on purpose, so you can see what is proven and what I am still building.

**Evidence labels:** `Client work` = paid or real engagement. `Live demo` = deployed and usable. `Portfolio build` = code in a public repo. `Coursework` = academic capstone. `Internship` = supervised work for a real company.

---

## 1. Assess and prioritize risk

| Requirement | Evidence | Type |
|---|---|---|
| Conduct control and risk assessments | [Risk Whisperer](https://riskwhisperer.vercel.app/) generates control assessments with risk scores and control-maturity ratings from plain-language system descriptions. [5-minute walkthrough](https://www.youtube.com/watch?v=QZWTN33ERdE) | Live demo |
| Map controls to frameworks | Risk Whisperer maps one selected framework per assessment across 15 options, including NIST SP 800-53 Rev 5, NIST CSF 2.0, ISO 27001:2022, SOC 2, PCI DSS v4.0, HIPAA, and FedRAMP. [Supported frameworks](https://github.com/bettybangs/Risk-Whisperer/blob/main/README.md#supported-frameworks-15) | Live demo |
| Track remediation and follow up on actions | Risk Whisperer POA&M module for remediation tracking. [POA&M in the README](https://github.com/bettybangs/Risk-Whisperer/blob/main/README.md) and [source](https://github.com/bettybangs/Risk-Whisperer/blob/main/src/App.js) | Live demo |
| Flag uncertain results for human review | Weak control mappings are flagged for a person to review instead of hidden. SOC 2 mappings are grounded in my own verified summaries of the 61 Trust Services Criteria ([grounding](https://github.com/bettybangs/Risk-Whisperer/blob/main/api/_prompts.js)) and checked by a judge model ([judge](https://github.com/bettybangs/Risk-Whisperer/blob/main/api/judge.js)). Design notes: [PROMPTS.md](https://github.com/bettybangs/Risk-Whisperer/blob/main/PROMPTS.md) | Portfolio build |

## 2. Frameworks and readiness

| Requirement | Evidence | Type |
|---|---|---|
| SOC 2 readiness and control scoping | Advising a fintech client on SOC 2 Type 1 readiness for a multi-asset custody platform: trust-services scope, control boundaries, and wallet-segregation requirements. [SOC 2 readiness page](https://beth-gerharts-grc.vercel.app/soc2) | Client work |
| NIST and ISO 27001 compliance assessment | Full-scope assessment for ROKS (Rock Stable Token, LLC) mapped to NIST and ISO 27001, with an executive walkthrough of remediation priorities. | Internship |
| NIST 800-53 and SOC 2 gap analysis | Northstar assessments, clearly labeled demonstration pieces, not client work: [SOC 2 Readiness Report](https://github.com/bettybangs/landing-page/blob/main/Northstar_SOC2_Readiness_Report.pdf) and [NIST 800-53 Gap Assessment](https://github.com/bettybangs/landing-page/blob/main/Northstar_NIST80053_Gap_Assessment.pdf) | Portfolio build |
| Cloud security control mapping | WGU capstone: simulated Azure healthcare tenant using Defender for Cloud, Entra ID (MFA, conditional access), and Sentinel, mapped to NIST RMF, NIST SP 800-53, and CSA CCM. | Coursework |

## 3. Automated control evidence

| Requirement | Evidence | Type |
|---|---|---|
| Automate evidence collection | [GRC Evidence Collector](https://github.com/bettybangs/grc-evidence-collector): Python checks that produce timestamped evidence. Built with Claude Code from my requirements; I reviewed and tested every change and configured the controls. | Portfolio build |
| Verify configuration against a control | [GitHub default-branch protection check](https://github.com/bettybangs/grc-evidence-collector/blob/main/check_branch_protection.py) (classic rules and rulesets), mapped to NIST 800-53 CM-3, SOC 2 CC8.1, and ISO 27001:2022 A.8.32 | Portfolio build |
| Scheduled, repeatable monitoring | Runs weekly through a [GitHub Actions workflow](https://github.com/bettybangs/grc-evidence-collector/blob/main/.github/workflows/weekly-evidence.yml) | Portfolio build |
| Show before and after remediation | Branch protection evidence: [before (fail)](https://github.com/bettybangs/grc-evidence-collector/blob/main/examples/branch_protection_fail.json) and [after (pass)](https://github.com/bettybangs/grc-evidence-collector/blob/main/examples/branch_protection_pass.json). All files: [examples folder](https://github.com/bettybangs/grc-evidence-collector/tree/main/examples) | Portfolio build |
| Cloud IAM review | [AWS IAM MFA check](https://github.com/bettybangs/grc-evidence-collector/blob/main/check_iam_mfa.py) using read-only SecurityAudit access. [Sample output](https://github.com/bettybangs/grc-evidence-collector/blob/main/examples/iam_mfa_pass.json) | Portfolio build |

## 4. AI governance and vendor risk

| Requirement | Evidence | Type |
|---|---|---|
| AI tool intake and review | [AI Tool & Vendor Registry]https://ai-vendor-registry.vercel.app/: employees submit AI tools for compliance and security review. Source: [ai-registry repo](https://github.com/bettybangs/ai-registry), [intake UI](https://github.com/bettybangs/ai-registry/blob/main/src/App.jsx) | Live demo |
| Risk-tier assignment | Registry assigns a risk tier automatically from submitted inputs. [Tiering logic](https://github.com/bettybangs/ai-registry/blob/main/api/tier.py) | Live demo |
| Third-party and vendor risk | Registry captures vendor and data details used for tiering. 20 years running my own business included owning vendor contracts and vendor-risk compliance. | Live demo |

*Note: the registry is a working demo. Logins, a database, and email notifications are planned, not built.*

## 5. Communication and stakeholder work

| Requirement | Evidence | Type |
|---|---|---|
| Explain risk to non-technical stakeholders | Executive walkthrough for ROKS that turned findings from an active incident (a private key exposed in a GitHub repo) into remediation priorities leadership could act on. Risk Whisperer also has a Tech Talk / Plain Talk toggle: [Tech Talk](https://github.com/bettybangs/Risk-Whisperer/blob/main/screenshot-tech-talk.png) and [Plain Talk](https://github.com/bettybangs/Risk-Whisperer/blob/main/screenshot-plain-talk.png) | Internship |
| Work directly with client leadership | SOC 2 advisory engagement: aligning the client's technical architecture with SOC 2 documentation expectations. | Client work |
| Own compliance, licensing, and budgets | Founder and operator of a business for 20 years, responsible for regulatory and licensing compliance, vendor contracts, and budgets. | Business experience |

## 6. Still building (honest gaps)

| Requirement | Status |
|---|---|
| Monitor global AI regulations | **Not yet demonstrated.** Learning area. |
| Maintain public trust content and RFP or security questionnaire responses | **Not yet demonstrated.** Documentation skills transfer, but no direct sample yet. |
| Cross-framework crosswalks | **In progress.** Risk Whisperer assesses one framework at a time; a crosswalk is a possible next feature. |
| Formal audit fieldwork | **Not yet demonstrated.** My experience is readiness and assessment work, not an external audit. |

---

*Last verified: 10/16/2026. Every link above was opened and checked on this date.*
