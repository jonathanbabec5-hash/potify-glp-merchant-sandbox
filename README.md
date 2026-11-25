# Green Light Pay Merchant Sandbox

[Complete repository directory tree](docs/DIRECTORY.md)

**Recovered merchant client.** Let an operator inspect how a checkout request moves from counter to receipt.

### Setup and usage

Use Node.js 24 for the included checks. Use Python 3 for the local static preview.

```sh
python3 -m http.server 8000 --bind 127.0.0.1 --directory public
```

Review the receipt contract. Open http://127.0.0.1:8000/green-light-pay/ in a browser. 

### Developer entry points

The original client calls partner, merchant, intent, screening, audit and reconciliation endpoints. The export preserves the client contract and leaves the server as a separate dependency. Explore `public/` in the full tree.

### Verification

The merchant client, checkout and developer-console scripts passed syntax checks. The counter rendered locally. Five startup API requests returned 404 on a static host because the original merchant server was unavailable.

```sh
node --check public/green-light-pay/app.js
node --check public/green-light-pay/nav.js
node --check public/green-light-pay/checkout.js
node --check public/green-light-pay/developer.js
```

### Release scope

Original Replit backend and provider contracts remain outside this export. Missing server routes limit local operation. potify-green-light-pay at `9cde0741196d23098527067271b89c3d4e5023b8`. Five recovered public merchant frontend files. Preview at the original base path. Server-backed actions require the original sandbox API. The favicon was recovered separately from the public merchant route. Recovered the original public checkout and developer pages plus their separate JavaScript and styles from green-light-pay.replit.app on November 25.

[Technical whitepaper](docs/WHITEPAPER.md) · [Marketing and sales plan](docs/MARKETING.md) · [Dated developer log](docs/BUILD-LOG.md)

Existing asset and code terms remain applicable. Public access to a recording, illustration, brand or manuscript does not itself grant commercial reuse rights.
