# Loyalty Rewards

Flavortown regulars are the best of the best — and the **Loyalty Rewards** service makes sure they feel like VIPs every time they come back.

This service tracks points, perks, and repeat-visit rewards across every Flavortown channel. When a regular orders through the Flavor Portal or Triple D Mobile, Loyalty Rewards quietly racks up their points and unlocks perks like free sides, skip-the-line pickup, and members-only menu drops.

## Responsibilities

- **Points Ledger** — Earns and redeems loyalty points per customer
- **Perks Engine** — Unlocks tiers and rewards as regulars hit milestones
- **Menu Awareness** — Consumes the Menu API to tailor rewards to what customers actually order
- **Rewards API** — Exposes balances and perks to the rest of Flavortown via `loyalty-rewards-api`

## Where it fits

Loyalty Rewards is part of the **ordering-system** and is owned by **team-triple-d**. It consumes the `menu-api` and provides the `loyalty-rewards-api`.
