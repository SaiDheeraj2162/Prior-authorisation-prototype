# Complete First Prior Authorization Prototype

An interactive, dependency-free Carelon-inspired prototype for the **Complete-First** prior-authorization operating model. It turns the supplied solution into an inspectable product demo: providers submit requests, coordinators work pends, clinicians make controlled decisions, integration teams exercise API outcomes, and executives review performance and gated readiness.

All request records, API outcomes, alerts, decision histories, and AI evidence are synthetic. This is not a clinical, payer, API, or AI production system.

## Live demo

The live GitHub Pages URL is created only after the repository is pushed and the Pages workflow succeeds. Add the resulting URL here after the first deployment; no repository owner or remote is configured in this local copy, so no URL is invented.

## What a judge can inspect

- **Operations center** — deadline-first work, channels, metrics, routing and release posture.
- **Submit request** — coverage/network interception, document guidance, attestation, exact duplicates, probable duplicates, and urgent bypass.
- **Pend desk / Clinical queue** — coordinator-owned completion work, reminders, escalation, clinician-only decisions, high-overturn second review, and breach root-cause capture.
- **API onboarding** — two health-system fixtures, acknowledgement, validation error, outage/fallback, recovery, and status lookup.
- **Performance & quality / Scenario model** — source-labelled planning figures, operational measures, denial/appeal bridge, and a deliberately modelled appeal-rate slider.
- **Safety & readiness** — gold-card proposal, AI G4 evidence, fail-safe manual routing, and a recorded kill-switch drill.
- **Judge mode** — 12 deterministic end-to-end scenarios; state persists across pages in the browser.

## Run and verify

Requires Node 20+; there are no runtime dependencies.

```sh
npm run verify
```

For a local static preview:

```sh
/Users/srishtirathour/.cache/codex-runtimes/codex-primary-runtime/dependencies/python/bin/python3 -m http.server 4173
```

Open `http://localhost:4173`. The browser stores demo state locally; use **Reset demo** in the sidebar to restore the seeded fixture.

## Build output

```sh
npm run build
```

The deployable static site is written to `dist/`.

## Repository structure

```text
complete-first-prototype/
├── index.html          # Application shell
├── styles.css          # Responsive visual design system
├── script.js           # Interactive interface and workflows
├── core.mjs            # Testable workflow and metric rules
├── assets/
│   ├── logos/          # Supplied brand asset
│   ├── icons/          # Guidance for the inline SVG icon system
│   └── images/         # Original product diagrams
├── README.md
├── LICENSE             # MIT source-code license
└── .gitignore
```

See [NOTICE.md](NOTICE.md) for Carelon trademark handling and the synthetic-data boundary.

## Publish on GitHub Pages

1. Create an empty GitHub repository and push this directory to its `main` branch.
2. In GitHub, open **Settings → Pages** and set **Source** to **GitHub Actions**.
3. The included [Pages workflow](.github/workflows/pages.yml) runs `npm ci`, `npm run verify`, builds `dist/`, and deploys it on every `main` push.
4. Open the deployment URL reported by the workflow after it succeeds.

## Key documents

- [Demo walkthrough](docs/demo-walkthrough.md)
- [Solution traceability](docs/solution-traceability.md)
- [Architecture](docs/architecture.md)
- [Visual design system](docs/visual-design-system.md)
- [Visual review and known limitation](docs/visual-review.md)
- [Assumptions and limitations](docs/assumptions-and-limitations.md)
- [GitHub publishing guide](docs/github-publishing.md)
- [Contributing](CONTRIBUTING.md), [security reporting](SECURITY.md), and [support](SUPPORT.md)
