# Health Modifiers

PokéHealth reads four daily health metrics and maps each one to a gameplay modifier through simple tier tables.

## Health inputs

| Input | Source |
|---|---|
| Steps | HealthKit (daily total) |
| Sleep hours | HealthKit (last night) |
| Active calories | HealthKit (daily total) |
| Workout minutes | HealthKit (daily total) |

A debug page lets you override these values manually for testing and development.

## Tier tables

### Steps → B-held movement speed

| Steps | Effect |
|---|---|
| < 3,000 | B does nothing (vanilla walking) |
| 3,000 – 9,999 | Holding B = 2× speed |
| 10,000 – 14,999 | Holding B = 4× speed |
| 15,000+ | Holding B = 8× speed |

### Sleep → Pokémon Center healing

| Sleep | Effect |
|---|---|
| < 5h | Heal to 60% HP, no PP restore |
| 5 – 6.9h | Heal to 85% HP, PP restored |
| 7h+ | Full heal, PP restored, +1 Revive |

### Active calories → XP multiplier

| Calories | XP |
|---|---|
| < 100 | ×0.75 |
| 100 – 399 | ×1.00 |
| 400 – 599 | ×1.25 |
| 600+ | ×1.50 |

### Workout minutes → Money + catch rate

| Minutes | Money | Catch |
|---|---|---|
| 0 | ×0.75 | ×0.90 |
| 1 – 29 | ×1.00 | ×1.00 |
| 30 – 59 | ×1.25 | ×1.20 |
| 60+ | ×1.50 | ×1.35 |

The player can inspect all active modifiers from the in-game START menu under **HEALTH**.
