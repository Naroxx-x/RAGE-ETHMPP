# RageSMP

A Rage-based PvP progression plugin for Paper 1.21.11.

## Rage
- Kill: +1 Rage
- Death: -1 Rage
- Maximum: 5
- If the killer is already at max Rage, they gain nothing: a **Rage Shard**
  drops on the ground instead. Any player can pick it up (it goes into their
  inventory) and **right-click it** to convert it into Rage.
- `/rage withdraw <amount>` lets you convert your own Rage back into physical
  shards (useful to store it, give it away, or trade it).
- Every Rage gain or loss is shown in **bold purple in chat** (in addition to
  the action bar).

## Bonuses per level
- **Rage 1**: +5% damage, and Blood Combo — after 3 consecutive sword hits on
  the same target, every hit after that is critical until you miss a swing.
- **Rage 2**: +10% damage, permanent Speed I.
- **Rage 3**: +15% damage, +2 hearts.
- **Rage 4**: +20% damage, +4 hearts, and Armor Break — after 5 consecutive
  hits on the same target, the next hit ignores part of their armor.
- **Rage 5**: +25% damage, +6 hearts, and sword hits break the target's
  raised shield for a few seconds.

All of this is configurable in `config.yml`.

Commands:
- `/rage`
- `/rage <player>`
- `/rage withdraw <amount>`
- `/setrage <player> <0-5>` (admin)

## Build
Compiling requires downloading the `paper-api` dependency from
`repo.papermc.io`, so an internet connection is required.

```
./gradlew build
```

The compiled plugin will be at `build/libs/RageSMP-1.0.0.jar`.
