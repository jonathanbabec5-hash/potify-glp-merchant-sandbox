# November 25, 2026 · Green Light Pay Merchant Sandbox

**Question.** Let an operator inspect how a checkout request moves from counter to receipt.

**Source and change.** potify-green-light-pay at `9cde0741196d23098527067271b89c3d4e5023b8`. Five recovered public merchant frontend files. Preview at the original base path. Server-backed actions require the original sandbox API. The favicon was recovered separately from the public merchant route. Recovered the original public checkout and developer pages plus their separate JavaScript and styles from green-light-pay.replit.app on November 25.

**Observed result.** The merchant client, checkout and developer-console scripts passed syntax checks. The counter rendered locally. Five startup API requests returned 404 on a static host because the original merchant server was unavailable.

```sh
node --check public/green-light-pay/app.js
node --check public/green-light-pay/nav.js
node --check public/green-light-pay/checkout.js
node --check public/green-light-pay/developer.js
```

**Next acceptance check.** Trace one sample request through intent, checkout and receipt in the code. Confirm server ownership before an integrated merchant test.

**Owner and decision.** Chance coordinates public materials. The GLP project owner must confirm any commercial agreement. Original Replit backend and provider contracts remain outside this export. Missing server routes limit local operation.

This dated record describes the developer package. Verify remote commit and tree in the publication receipt before announcing a GitHub release.

## November 26 · merchant server restored

The original Replit export contained 27 tracked files for the fictional checkout. Nine public assets matched the published merchant frontend byte for byte. All three HTML entries also matched after substituting the configured base path. This verified that the recovered server belongs with this client.

A clean Node.js 24 workspace install passed all 99 offline tests. The restored server also passed the developer terminal input and transaction-filter scenarios in Chromium at 1280 × 900 and 390 × 844. The initial browser run uncovered a deep-link bug: opening the terminal directly left its loading panel in place. The working copy now mounts and focuses the terminal once while preserving in-progress typing on later refreshes. The browser fixture recognizes a retained invalid command and waits for the actual health response. The upstream snapshot remains linked in the README.

The checks used disposable local SQLite data and fictional amounts. They establish the sandbox flow and developer interactions. Merchant acquisition, provider approval and customer settlement have separate acceptance criteria.
