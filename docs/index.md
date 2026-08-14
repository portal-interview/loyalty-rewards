# Loyalty Rewards

Flavortown regulars are the best of the best — and the **Loyalty Rewards** service makes sure they feel like VIPs every time they come back.

This service tracks points, perks, and repeat-visit rewards across every Flavortown channel. When a regular orders through the Flavor Portal or Triple D Mobile, Loyalty Rewards quietly racks up their points and unlocks perks like free sides, skip-the-line pickup, and members-only menu drops. Points earned and redeemed are also recorded on a blockchain, giving participating channels a shared, tamper-evident history of loyalty activity.

## Responsibilities

- **Points Ledger** — Earns and redeems loyalty points per customer
- **Blockchain Record** — Anchors points activity on-chain for traceability and consistent reconciliation across channels
- **Perks Engine** — Unlocks tiers and rewards as regulars hit milestones
- **Menu Awareness** — Consumes the Menu API to tailor rewards to what customers actually order
- **Rewards API** — Exposes balances and perks to the rest of Flavortown via `loyalty-rewards-api`

## How blockchain fits

The Loyalty Rewards service remains the interface used by Flavortown applications. When points are earned or redeemed, it processes the activity through the usual rewards flow and records the resulting transaction on the loyalty blockchain. That on-chain record provides an auditable history that channels can use to verify activity and reconcile balances without changing the customer experience.

Customers do not need a crypto wallet, and loyalty points are not cryptocurrency. They remain promotional rewards governed by the Flavortown loyalty program and have no cash value.

!!! note "Demo implementation"
    The blockchain integration described here is for demonstration purposes. It illustrates the intended architecture and should not be treated as a production financial or custody system.

## Where it fits

Loyalty Rewards is part of the **ordering-system** and is owned by **team-triple-d**. It consumes the `menu-api` and provides the `loyalty-rewards-api`.
