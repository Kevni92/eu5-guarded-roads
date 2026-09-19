# Guarded Roads

**Guarded Roads** is an Europa Universalis V gameplay mod that adds a military road-security building chain. Guard posts and patrol detachments can only be established where the matching road infrastructure already exists.

## Building chain

| Tier | Building | Required road | Unlock advance | Proximity propagation | Gold |
|---|---|---|---|---:|---:|
| I | Escort House | Gravel Road | Road Building | +5% | 150 |
| II | Guardhouse | Paved Road | Paved Roads | +10% | 300 |
| III | Patrol Barracks | Modern Road | Modern Roads | +15% | 600 |
| IV | Railway Guardhouse | Railroad | Railroads | +20% | 1200 |

German localisation uses **Geleithaus → Wachhaus → Patrouillenkaserne → Bahnwache**.

Each tier makes the previous guarded-road building obsolete. A building is only available in a Location that has a road connection of the corresponding exact road type to a neighboring Location.

The proximity bonuses use EU5's verified `local_distance_from_capital_speed_propagation` Location modifier, the same modifier used by the vanilla bridge building. Vanilla bridges use `0.1`, i.e. +10%. Guarded Roads therefore scale this modifier as 0.05 / 0.10 / 0.15 / 0.20 for +5% / +10% / +15% / +20%.

## Upkeep and manpower

The buildings employ Soldier POPs and require full maintenance demand even when employment is incomplete. Maintenance is deliberately restricted to:

- Weaponry
- Tools
- Coal

Higher tiers consume progressively more of all three goods. Construction has no direct manpower price. Instead, each tier applies a persistent negative `local_manpower` raw modifier of -0.05 / -0.10 / -0.15 / -0.20, representing 50 / 100 / 150 / 200 manpower tied down in escorts, checkpoints and patrol detachments.

## Languages

- English
- German / Deutsch

## Compatibility

The mod injects its building unlocks into the four vanilla road advances instead of replacing those advances. It is marked multiplayer-synchronized and currently declares compatibility with EU5 `1.*.*`.

## Installation / Workshop structure

The repository root is the mod root. `.metadata/metadata.json` contains the launcher/Workshop metadata, while gameplay files live under `in_game/` and localisation/UI metadata under `main_menu/`.
