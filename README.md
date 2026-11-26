# Green Light Pay Merchant Sandbox

[Complete repository tree](docs/DIRECTORY.md) · [Whitepaper](docs/WHITEPAPER.md) · [Marketing and sales plan](docs/MARKETING.md) · [Build record](docs/BUILD-LOG.md)

A cashier starts a fictional sale. A customer opens the checkout on a phone. The developer console shows how the same request passes screening, gains a simulated authorization and acquires a reconciled receipt. A contributor can follow the complete path locally with the recovered Replit server, client and fixtures.

## Run the counter

Use Node.js 24 and npm. Run these commands from the repository root.

```sh
npm ci
npm test
GLP_SANDBOX=1 HOST=127.0.0.1 BASE_PATH=/green-light-pay npm start
```

Open http://127.0.0.1:4173/green-light-pay/. Start a fictional basket, follow the qualified-partner handoff, and open the developer console to compare the observed facts with the final receipt. Local records are stored in SQLite. The source includes the POS, partner and observer fixtures used by the demonstration.

## Inspect and verify

- Follow the [domain logic](sandbox/src/core.mjs) into the [HTTP routes](sandbox/src/server.mjs).
- Inspect the [cashier interface](sandbox/public/app.js), [customer checkout](sandbox/public/checkout.js) and [developer console](sandbox/public/developer.js).
- Reproduce one discrepancy with a synthetic basket and name the state that should have changed. Partner agreements and actual settlements require separate evidence.
- The [static frontend](public/green-light-pay/) remains available for interface review at its original route. The server-backed sandbox is the local entry point for the full checkout.

For the optional browser suite, keep the sandbox running as above, then run the following commands in a second terminal.

```sh
npx playwright install chromium
GLP_TEST_URL=http://127.0.0.1:4173/green-light-pay npm run test:browser
```

## Source

The [original Replit source snapshot](https://github.com/jonathanbabec5-hash/potify-green-light-pay/tree/82f4f6265044034b144ad11f64a916be319aa97f/replit-source/green-light-pay) contains 27 source, configuration and test files. The working copy lives in `sandbox/`. The root npm workspace adds a reproducible lockfile and separates offline tests from the optional browser suite. No live payment processor is connected. Green Light Pay retains its own governance, contracts and finances.
