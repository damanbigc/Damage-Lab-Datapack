# Damage Lab: see every hit in Minecraft

A data pack for **Minecraft Java 26.3** that shows you exactly how much damage every hit does. Training dummies in every armor tier pop up floating damage numbers, show a heart bar, and count how many hits it takes to knock them out. No mods.

## What's in it
- **6 training dummies**: no armor, leather, iron, diamond, netherite, and netherite + Protection IV. A board behind each one shows its armor and toughness.
- **Floating damage numbers** on every hit (white, yellow, orange, then red for huge hits).
- **Heart bar + hit counter** above each dummy. At 20 damage it gets **KNOCKED OUT**: it glows red and shows how many hits it took.
- The dummies never actually die. They **heal back to full 3 seconds** after the last hit.
- **Mace Tower**: climb the ladder and jump off either side onto a dummy for big smash hits.
- `/function dmglab:kit` gives you swords (wood to netherite, plus Sharpness V), a netherite axe, maces (normal, Density V, Breach IV), a Power V bow, a trident and wind charges.

## How to use it
1. Make a **Superflat** Java 26.3 world with cheats on (Creative works).
2. Put `Damage_Lab.zip` in `saves/<your world>/datapacks`, then run `/reload` in game.
3. Stand somewhere open and run `/function dmglab:build`. The dummies appear 6 blocks north of you, in a row going east.
4. Run `/function dmglab:kit` and start hitting.

Other commands: `/function dmglab:heal_all` heals every dummy right away.

## Numbers to try (netherite sword, 8 damage)
| Dummy | Damage per hit | Hits to knock out |
|---|---|---|
| No armor | 8 | 3 |
| Leather | 7.04 | 3 |
| Iron | 4.48 | 5 |
| Diamond | 2.24 | 9 |
| Netherite | 2.11 | 10 |
| Netherite + Prot IV | 0.76 | 27 |

## How it works
Every tick each dummy compares its health to the tick before. When it drops, the difference is the damage, so the numbers are always the game's real numbers (armor, toughness, enchantments, invulnerability frames and all). The dummies have 1024 max health so they never die. The "20 HP" on the bar counts down from a normal player's health.
