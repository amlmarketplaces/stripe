# amlmarketplaces/stripe

Claude Code marketplace federating all `@amlplugins/stripe-*` plugins.

## Install

Add to your project's `.claude/settings.json`:

```json
{
  "extraKnownMarketplaces": {
    "aml-stripe": {
      "source": { "source": "github", "repo": "amlmarketplaces/stripe" }
    }
  },
  "enabledPlugins": {
      "stripe-billing@aml-stripe": true,
      "stripe-checkout@aml-stripe": true,
      "stripe-climate@aml-stripe": true,
      "stripe-connect@aml-stripe": true,
      "stripe-identity@aml-stripe": true
    }
}
```

Then launch Claude Code in the project. The marketplace is fetched from `amlmarketplaces/stripe`, cached under `~/.claude/plugins/cache/aml-stripe/`, and each enabled plugin is loaded from its `amlplugins` source repo.

## Plugins (9 total)

- `stripe-billing` — [@amlplugins/stripe-billing](https://github.com/amlplugins/stripe-billing)
- `stripe-checkout` — [@amlplugins/stripe-checkout](https://github.com/amlplugins/stripe-checkout)
- `stripe-climate` — [@amlplugins/stripe-climate](https://github.com/amlplugins/stripe-climate)
- `stripe-connect` — [@amlplugins/stripe-connect](https://github.com/amlplugins/stripe-connect)
- `stripe-identity` — [@amlplugins/stripe-identity](https://github.com/amlplugins/stripe-identity)
- `stripe-issuing` — [@amlplugins/stripe-issuing](https://github.com/amlplugins/stripe-issuing)
- `stripe-radar` — [@amlplugins/stripe-radar](https://github.com/amlplugins/stripe-radar)
- `stripe-tax` — [@amlplugins/stripe-tax](https://github.com/amlplugins/stripe-tax)
- `stripe-terminal` — [@amlplugins/stripe-terminal](https://github.com/amlplugins/stripe-terminal)

## Related

- npm packages: `@amlplugins/stripe-*` published to GitHub Packages (`https://npm.pkg.github.com`).
- Aggregating parent: [`amlmarketplaces/aml`](https://github.com/amlmarketplaces/aml) — federates every `@amlplugins/*` plugin under a single marketplace.
- AML topology: see `.claude/rules/definitions/ageni.md` § "GitHub Topology" — this repository is a Tier-4 HUB-INSTANCE under the `amlmarketplaces/` Tier-3 HUB-ORGANIZATION.

> Built by `.claude/skills/aml/metateam/marketplace/test/cross-org-amlmarketplaces-batch.mjs`.
