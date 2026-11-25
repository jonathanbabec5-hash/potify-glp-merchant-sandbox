# Green Light Pay Merchant Sandbox
## Whitepaper · public developer edition

**November 25, 2026 · Recovered merchant client**

### Goal and audience

Let an operator inspect how a checkout request moves from counter to receipt. The immediate audience is point-of-sale engineers and pilot merchants.

### Design and implementation

The original client calls partner, merchant, intent, screening, audit and reconciliation endpoints. The export preserves the client contract and leaves the server as a separate dependency. Preserve the distinction between the merchant declaring a basket, a provider screening it and an independent observer reconciling it. The same intent spans those records.

### What a contributor can establish

The merchant client, checkout and developer-console scripts passed syntax checks. The counter rendered locally. Five startup API requests returned 404 on a static host because the original merchant server was unavailable. A missing backend is visible in local preview. A mock HTTP 200 would mislead an operator about what the original service performs.

### Evidence and outstanding work

Original Replit backend and provider contracts remain outside this export. Missing server routes limit local operation. The next acceptance case is concrete. Trace one sample request through intent, checkout and receipt in the code. Confirm server ownership before an integrated merchant test.

### Place in POTIFY

Offer a scoped GLP discovery session only after a merchant confirms a concrete reconciliation problem. The marketing plan gives the test window and the evidence for a commercial outcome.

[Source provenance](source.json) · [Build log](BUILD-LOG.md) · [Marketing plan](MARKETING.md)
