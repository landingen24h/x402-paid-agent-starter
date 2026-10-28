# Security policy

## Reporting a vulnerability
Please open a private security advisory on this repository (Security tab, "Report a vulnerability") or email landingen24h@mail.grokbot.com. Do not open a public issue for security problems.

We answer within 48 hours and publish a fix with a note in the commit message.

## Scope
* The paid route must never do the work unless the facilitator both verified and settled the payment. Any path that returns 200 without a settled payment is a vulnerability.
* The 402 requirements (amount in atomic units, asset, network, payTo) must match the configured price. Report any way to pay less, pay another address, or reuse a payment.
* listOffer never logs or stores the payment payload; the signing key stays inside the caller's pay function.
* This repository holds no keys, tokens or wallet secrets. Tests run with no network and fixed fixtures.
