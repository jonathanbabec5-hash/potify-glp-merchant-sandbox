# Green Light Pay Merchant Sandbox
## Whitepaper · public developer edition

**November 26, 2026 · Recovered merchant client and sandbox server**

### Goal and audience

Let an operator inspect how a checkout request moves from counter to receipt. The immediate audience is point-of-sale engineers and pilot merchants.

### From intent to receipt

The Replit server binds a frozen basket to a customer handoff, compares the point-of-sale amount against the partner and observer fixtures, and records successive states. A receipt is meaningful when the supporting records reconcile. Inspect the [domain logic](../sandbox/src/core.mjs) beside the [HTTP lifecycle tests](../sandbox/test/stage1-http.test.mjs) and trace a declined path alongside an accepted one.

### Evidence and limits

The restored frontend matches nine static files byte for byte. The three HTML entry points also match after substituting the server’s documented base path. The SQLite sandbox and its seeded fixtures support local verification. Real provider approvals, custody arrangements, customer transactions and signed merchant agreements require their own evidence.

### Proposed first contribution

Pick one fictional intent and trace the status, amount and evidence available to the cashier and the customer at each step. Report the first state whose explanation on screen is inconsistent with the fixture. Green Light Pay maintains its own finances, contracts and governance.
