# ConfidenceNode

**Infrastructure for honest collaboration under information asymmetry.**

---

## The problem we work on

Every act of collaboration involves a decision about information: what to reveal, what to protect, and when. This decision is rarely neutral. Revealing uncertainty can be used against you. Hiding it has costs for everyone. The result is a world built on noise — inflated estimates, unverifiable credentials, uncoordinated organisations.

ConfidenceNode builds infrastructure that changes this calculus. Our tools make it safe to be honest, and make honesty verifiable by others.

---

## Three projects, one problem

### [ctx](https://github.com/confidencenode/ctx-v2)
**Capture and prioritise technical uncertainty.**

ctx lives where your doubts live: in the code. It scans `# ?` markers, converts them into prioritised gaps using a Bayesian DIC model (Difficulty, Impact, Coordination), and connects each gap to the knowledge that resolves it. The vault is local and encrypted — your calibration profile belongs to you, not your employer.

*The problem it solves:* developers accumulate doubts that block decisions. Without a system, all doubts seem equally urgent — or equally ignorable. ctx makes the structure of uncertainty visible and actionable.

### [Trusteando Protocol](https://github.com/confidencenode/Trusteando_Protocol)
**A verifiable knowledge graph built on the web you already have.**

Trusteando is an open protocol for publishing cryptographically verifiable facts. Its core is four functions and twenty lines of code. Any entity that publishes a `trusteando/` folder on a domain it controls adds a node to a distributed graph of signed, timestamped, immutable facts. Verification requires no central server — only the issuer's URL.

*The problem it solves:* verifying that a credential, a relationship, or an authority claim is real currently requires bilateral agreements, proprietary APIs, or trusting whoever sends you a copy. Trusteando replaces all of that with a public URL and a signature.

### [ConfidenceNode Protocol](https://github.com/confidencenode/ConfidenceNode_Protocol)
**A trust framework for collaborative estimation under information asymmetry.**

The ConfidenceNode Protocol addresses the root cause of why estimates are systematically dishonest: the incentive structure punishes honesty. When estimates are used as performance targets, rational agents optimise for safety over accuracy. The protocol defines a Bayesian model that builds latent agent profiles from observed behaviour, a local encrypted vault that keeps those profiles opaque to employers, and a certification authority (ConfidenceNode0) that signs organisational commitments not to exploit the information the system generates.

*The problem it solves:* an engineer who estimates honestly is giving away information about themselves with no contractual protection. The protocol makes honest estimation safe — technically, contractually, and economically.

---

## How the projects connect

The three projects are layers of the same infrastructure:

```
ConfidenceNode Protocol    ← the social contract: make honesty safe
        │
        ▼
    Trusteando             ← the verification layer: make facts checkable
        │
        ▼
       ctx                 ← the capture layer: make uncertainty visible
```

**ctx → Trusteando:** The C (Coordination) variable in ctx's DIC model can be inferred from the dependency structure of a project expressed as a Trusteando graph. A task with `extern/` references to three different teams signals high coordination cost — automatically, without subjective estimation.

**Trusteando → ConfidenceNode Protocol:** The ConfidenceNode0 certification seal — the public commitment that an organisation will not exploit estimation data — is itself a Trusteando node. The commitment is published under a URL the certifier controls, signed, and immutable. Anyone can verify it without asking anyone.

**ConfidenceNode Protocol → ctx:** The encrypted vault in ctx is the technical implementation of Layer 3 of the ConfidenceNode Protocol. The Bayesian calibration profile is exactly the kind of implicit disclosure the protocol protects.

---

## The common thread

All three projects respond to the same question: *when is it rational to reveal what you know, and when is it not?*

The answer depends on whether the infrastructure for safe disclosure exists. ConfidenceNode builds that infrastructure — for individuals estimating tasks, for professionals asserting credentials, and for organisations coordinating without bilateral agreements.

---

## The philosophy

We publish everything. The reference implementations are open source. The protocols are public. The enforcement mechanisms rely on verifiability, not obscurity.

This is consistent with the central claim of all three projects: transparency and protection are not in conflict. An agent can be fully transparent about how a system works while maintaining meaningful protection for the data the system generates. The protection comes from contracts, cryptography, and social norms — not from hiding the mechanism.

> *You cannot build a system of trust in secret.*

---

## Status

| Project | Status | License |
|---|---|---|
| ctx | Active development | GPL v3 |
| Trusteando Protocol | v0.2.1 published | GPL v3 |
| ConfidenceNode Protocol | v0.1 draft for public comment | — |

---

## Contact

protocol@confidencenode.org — confidencenode.org
