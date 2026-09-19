# Guarded Roads

**Guarded Roads** is an Europa Universalis V gameplay mod that adds a military road-security building chain. Guard posts and patrol detachments can only be established where the matching road infrastructure already exists.

## Building chain

| Tier | Building | Required road | Unlock advance | Proximity source | Gold | Manpower |
|---|---|---|---|---:|---:|---:|
| I | Guarded Gravel Roads | Gravel Road | Road Building | +5 | 150 | 0.10 |
| II | Guarded Paved Roads | Paved Road | Paved Roads | +10 | 300 | 0.20 |
| III | Guarded Modern Roads | Modern Road | Modern Roads | +15 | 600 | 0.30 |
| IV | Guarded Rail Network | Railroad | Railroads | +20 | 1200 | 0.50 |

Each tier makes the previous guarded-road building obsolete. A building is only available in a Location that has a road connection of the corresponding exact road type to a neighboring Location.

The proximity values use EU5's verified `local_proximity_source` Location modifier. They are flat proximity-source values, not percentage modifiers.

## Upkeep and manpower

The buildings employ Soldier POPs and require full maintenance demand even when employment is incomplete. Maintenance is deliberately restricted to:

- Weaponry
- Tools
- Coal

Higher tiers consume progressively more of all three goods. In addition to the construction manpower price, each tier applies a persistent negative `local_manpower` raw modifier (-0.005 / -0.010 / -0.015 / -0.020), representing manpower tied down in checkpoints, escorts and patrol detachments.

## Languages

- English
- German / Deutsch

## Compatibility

The mod injects its building unlocks into the four vanilla road advances instead of replacing those advances. It is marked multiplayer-synchronized and currently declares compatibility with EU5 `1.*.*`.

## Installation / Workshop structure

The repository root is the mod root. `.metadata/metadata.json` contains the launcher/Workshop metadata, while gameplay files live under `in_game/` and localisation/UI metadata under `main_menu/`.
