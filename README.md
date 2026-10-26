# Darpan

Mintlify site for [docs.drpn.ai](https://docs.drpn.ai): Darpan product docs and release notes for the people who use the app. The GraphQL API, self-hosting, and engineering docs live in [darpan-developers](https://github.com/drpn-ai/darpan-developers) at [developers.drpn.ai](https://developers.drpn.ai).

## Content model

- `index.mdx` and `quickstart.mdx` introduce the product and first workflow.
- `getting-started/**` explains concepts, Ask Darpan navigation, users, and environments.
- `guides/**` holds task-oriented product guides.
- `reference/**` holds stable product reference material.
- `troubleshooting/**` captures symptom-first repair paths.
- `releases/**` holds release updates, the roadmap, and the community boards.

## Local preview

Install the Mintlify CLI:

```bash
npm i -g mint
```

Run the docs site from this repository root:

```bash
mint dev
```

Preview at `http://localhost:3000`.

## Validation

Run these checks before publishing larger updates:

```bash
mint broken-links
mint validate
```

If the CLI is not installed, at minimum validate `docs.json`:

```bash
jq empty docs.json
```

## Publishing

Mintlify deploys from the connected GitHub repository after changes are pushed to `main`. Use small commits and keep docs changes tied to the product, release, or support work that made them necessary.

## Documentation principles

Darpan uses Ask Darpan as the primary navigation model. Product pages should describe how users move from setup to reconciliation runs and result review.

Connections, schemas, RuleSets, saved runs, and generated outputs are not separate product stories; they are the support structure for setting up, running, and reviewing reconciliation.
