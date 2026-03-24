nprotocol-ar-spec
Attestation Record Schema v0.1 — Field Documentation

What This Is
A 30-day field operation documenting that a sovereign node can assume micro-risks and deliver value in an ex-post recognition economy — using only available tools, with no prior contracts, no corporate structure, and no employer.
The existence of bounty platforms (Algora, Gitcoin, Stacker News) already proves the demand. This operation does not test whether the market exists. It documents how a node operates within it, and what that looks like when cognitive functions are explicitly stratified across humans and machines.

The Framing
The knowledge economy is undergoing a structural shift. As AI consumes execution tasks from below, cognitive labor is stratifying into distinct layers:
Layer
Who
What it does
Execution
Antigravity / Claude Code
Implements, tests, runs — no judgment
Agency
Manu + Gemini Chat
Operates tools, coordinates flow, ensures integrity
Judgment / Axiology
Diogo
Decides what is worth doing and why

These layers are not a theory being tested. They are the operational structure of this experiment — made explicit so the documentation is legible.
The Agency layer Manu occupies today will become increasingly automatable. That is not a problem. Exercising reflective Agency with real tools on real deliveries is how someone builds the cognitive scaffolding to eventually exercise Judgment. The inefficiency is the point: it is the cost of the apprenticeship.

What Is Being Documented
A sovereign node assuming micro-risks under a market signal.
The signal already exists — bounty amounts are public, platforms are live, demand is proven. What this operation records is the node's behavior within that signal: which problems it selects, how it delivers, what it earns, and what each delivery reveals about coordination without prior agreement.
Each delivery is recorded as an Attestation Record (AR) — a structured document linking a problem, a solution, a verified payment, and an interpretive note written by the node's Judgment layer.

The AR Schema v0.1
Every record in /records conforms to this structure:
{
  "ar_version": "0.1",
  "node_id": "[Nostr npub of the author]",
  "timestamp_iso": "[ISO 8601 timestamp]",
  "problem": {
    "source_url": "[bounty issue URL]",
    "description": "[what was broken or missing]",
    "domain": "infra | coordination | protocol | ui | security"
  },
  "delivery": {
    "commit_sha": "[merged commit hash]",
    "approach_summary": "[root cause → solution in 2–3 lines]",
    "hours_spent": 0
  },
  "recognition": {
    "type": "bounty | zap | grant",
    "amount_sats": 0,
    "recognized_by": "[npub or public address of the payer]",
    "tx_proof": "[paid Lightning invoice or transaction ID]"
  },
  "recognition_ratio": "[sats/hour]",
  "protocol_note": "[what this delivery reveals about ex-post coordination]",
  "nostr_event_id": "[kind:30023 Nostr event ID]"
}

tx_proof links each AR to a verifiable transaction. Recognition is not claimed — it is proven.
protocol_note is the only field no tool fills. It is written by the Judgment layer and records what this specific delivery reveals — or complicates — about operating as a sovereign node in an ex-post economy. It is what makes this a documented case rather than a work log.

Repository Structure
nprotocol-ar-spec/
├── README.md              — this file
├── ar-schema.json         — canonical JSON Schema for AR v0.1
├── records/               — one .json per published Attestation Record
│   ├── AR-001.json
│   └── ...
└── FIELD-REPORT-D30.md    — closing document published on day 30


Relationship to nProtocol
The nProtocol defines a multi-layer coordination architecture with immutable on-chain Attestation Records, Recognition Markets and a local sovereign agent (nodeP) acting as a cryptographic membrane between cognition and the permanent registry.
This repository is not that. It uses available infrastructure — GitHub, Nostr, Lightning — to simulate the record-keeping behavior of the protocol at minimal cost. The gap between what is here and what nProtocol specifies is documented, not hidden.
Component
nProtocol (target)
This repository
Attestation Record
On-chain, Ethereum L2
JSON file + Nostr event
Recognition
Escrow smart contract
Bounty payment + tx proof
Resolver
Contract reading the chain
Script aggregating Nostr by npub
Declaration
ECDSA signature + on-chain tx
git push + Nostr publication


The Nodes
Node Zero — Diogo Carlotto — Judgment / Axiology. Selects targets, defines what is worth pursuing, writes every protocol_note. Does not operate execution tools.
Manu — Agency. Operates Antigravity agents, reviews all generated code before submission, manages git, publishes ARs after merge and payment.

Period
Start: March 2026 Duration: 30 days Close: FIELD-REPORT-D30.md — a public record of what the operation produced, what each AR reveals, and what operating as a sovereign node in an ex-post economy actually looks like.

This README is an Attestation Record of Intent. It resolves with FIELD-REPORT-D30.md — or the record stands open.

MIT License