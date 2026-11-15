# Two Minute Billing — Agent Skills

Agent Skills that add billing to an application with
[Two Minute Billing](https://twominutebilling.com): subscriptions, one-time purchases, usage-based
and AI billing, hosted checkout and a customer portal. A coding agent reads them and does the
work in your code, on a test-mode key.

| Skill | What it does |
| --- | --- |
| `two-minute-billing` | Start here to add subscription, one-time purchase, usage-based or AI billing to an application with Two Minute Billing (tmbilling). |
| `two-minute-billing-go-live` | Take a Two Minute Billing integration live safely. |
| `two-minute-billing-integrate` | Wire Two Minute Billing into an application's code. |
| `two-minute-billing-pricing` | Decide what to charge and put it in Two Minute Billing as code. |
| `two-minute-billing-usage` | Meter and bill usage with Two Minute Billing. |
| `two-minute-billing-verify` | Prove a Two Minute Billing integration works before go-live, on real test-mode invoices. |

Start with `two-minute-billing`. It connects to your account and sends the agent to the other skills.

## Install in Claude Code

This repository is a Claude Code plugin marketplace. In a Claude Code session:

```text
/plugin marketplace add gox-ai/two-minute-billing-skills
/plugin install two-minute-billing@two-minute-billing
```

Or from your shell:

```sh
claude plugin marketplace add gox-ai/two-minute-billing-skills
claude plugin install two-minute-billing@two-minute-billing
```

The skills then show as `/two-minute-billing:<skill>`, for example `/two-minute-billing:two-minute-billing`, and the
agent also loads them by itself when your request matches one.

Auto-update is off by default for marketplaces outside Anthropic's own. To get a new release,
run `claude plugin update two-minute-billing@two-minute-billing`, or turn on auto-update for this
marketplace on the **Marketplaces** tab of `/plugin`.

## Install in other agents

The same skills install into Cursor, Codex, Gemini CLI and other agents that read Agent Skills:

```sh
npx skills add https://twominutebilling.com
```

## Test mode only

The skills work on test-mode keys only. Before any write, the agent checks the key's mode, and
the bundled preflight script refuses a key that can change live data. Going live (live gateway,
live keys, production webhooks) is a step you take yourself; the go-live skill gives you the
list and a read-only audit.

The skills never ask for a key in the chat and never print one: their scripts read keys from
the environment.

## Source

This repository is built from `docs-site/skills/` in
[gox-ai/two-minute-billing](https://github.com/gox-ai/two-minute-billing) at each release. A
change made here is replaced by the next release, so send changes to that repository.

Documentation: https://twominutebilling.com/help/developers

## License

MIT. See [LICENSE](./LICENSE).
