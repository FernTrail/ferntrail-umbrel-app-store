# BitGarth for Umbrel

This repository contains the Umbrel App Store packaging for
[BitGarth](https://bitgarth.app), a local-first cryptocurrency portfolio
tracker developed by [FernTrail B.V.](https://ferntrail.tech/).

## What is in this repository

- The Umbrel app-store manifest
- The BitGarth app manifest and Docker Compose configuration
- App Store screenshots and metadata

These files let Umbrel install the published BitGarth container image and keep
its data in Umbrel's persistent app-data directory.

## Privacy model

You create local users on your own instance — no central BitGarth account is
required. Portfolio data, labels, settings, and saved API keys live in an
encrypted local database on your Umbrel, unlocked by each user's password. We
never hold that password, so we cannot read your data even if we wanted to. Keep
a backup: nobody can unlock it for you either.

Payment and entitlement checks for the optional paid plan use pseudonymous
identifiers that are separate from your local app users. Your portfolio and
transaction data are not sent to BitGarth's entitlement service.

You do not have to take our word for any of this. The container runs on your own
machine, so you can inspect its network traffic and see for yourself exactly what
BitGarth talks to.

See the [Privacy Policy](https://bitgarth.app/privacy.html) and
[Security page](https://bitgarth.app/security.html) for details.

## Pricing

BitGarth is free to use as a portfolio tracker: balance sync for Bitcoin xpubs
and Ethereum addresses, manual assets, net worth in your own currency, and
plain-text accounting exports for hledger and ledger-cli.

An optional paid plan adds transaction-history backfill and reports to support
tax filing. Upgrading does not create a central account.

## Source and licensing

This packaging repository is public so you can see exactly what Umbrel installs
and how it is configured. The BitGarth application itself is not open source —
its source code and container image stay with FernTrail B.V., and use is governed
by the [BitGarth Terms](https://bitgarth.app/terms.html).

The `repo` field in the app manifest is left empty on purpose: it points at an
upstream source repository, and this repository holds the packaging only.

## Support and security

- Product and Umbrel support: [hello@bitgarth.app](mailto:hello@bitgarth.app)
- Security information and reporting: [bitgarth.app/security.html](https://bitgarth.app/security.html)
- Published container images: [Docker Hub](https://hub.docker.com/r/bitgarth/bitgarth)

Issues and pull requests in this repository should be limited to the Umbrel
packaging.
