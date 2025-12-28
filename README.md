# CS2 Crosshair Follow Guide

Simple configuration for CS2 that changes crosshair color and the `cl_crosshair_recoil` option based on what you are doing in-game.

## Credits
- **u/craygroupious**: [Reddit Post](https://www.reddit.com/r/GlobalOffensive/comments/16wgzkp/comment/k2x048d/)
- **u/Vipitis**: [Reddit Post](https://www.reddit.com/r/GlobalOffensive/comments/16a3yyr/recoil_crosshair_switching_bind_for_cs2/)

---

## What This Config Does

- **Follow Recoil toggle**: `cl_crosshair_recoil` turns on while holding `mouse1` and turns off when you release it.
- **Color feedback**: the crosshair turns bright green while Follow Recoil is active and cyan when it is not.
- **Weapon binds manage mouse1**: pressing `1/2/3` not only selects the weapon slot but also rebinds `mouse1` so the config knows how to behave for that slot.

```cfg
alias ColorActivated "cl_crosshaircolor_r 0; cl_crosshaircolor_b 0; cl_crosshaircolor_g 255; cl_crosshair_recoil true"
alias ColorDeactivated "cl_crosshaircolor_r 50; cl_crosshaircolor_b 255; cl_crosshaircolor_g 255; cl_crosshair_recoil false"
```

Change the numbers in those lines if you want different colors or recoil behavior.


## Bind Behavior (matches `autoexec.cfg`)

- `mouse1` is bound to `+shootr`, which runs `+attack`, enables Follow Recoil, and sets the "activated" color. Releasing `mouse1` runs `-shootr`, stops attacking, disables Follow Recoil, and switches to the "deactivated" color.

```cfg
alias "+shootr" "+attack; cl_crosshair_recoil true; ColorActivated"
alias "-shootr" "-attack; cl_crosshair_recoil false; ColorDeactivated"
bind "mouse1" "+shootr"
```

- Pressing `2` (primary weapons) executes `slot1; bind mouse1 +shootr`. You keep shooting normally and the Follow Recoil automation stays enabled.
- Pressing `3` (secondary weapons) executes `slot2; bind mouse1 +attack`. This restores the default shoot bind, so no automatic color/recoil changes happen on pistols.
- Pressing `1` (melee) executes `slot3; bind mouse1 -shootr`. Left click now only runs the "release" alias, which instantly disables Follow Recoil and applies the deactivated color. This stops accidental knife swings but also means you cannot attack until you switch back to slot 2 or 3.

```cfg
bind "2" "slot1; bind mouse1 +shootr"
bind "3" "slot2; bind mouse1 +attack"
bind "1" "slot3; bind mouse1 -shootr"
```

Keep the binds in the script consistent—if you change one, make sure the others are updated so that `mouse1` behaves the way you expect.

---

## Installation

1. Copy the content of `autoexec.cfg` from this repo.
2. Place it in your CS2 config folder, usually `C:\Program Files (x86)\Steam\steamapps\common\Counter-Strike Global Offensive\game\csgo\cfg`.
3. If `autoexec.cfg` already exists, merge the binds carefully so nothing important is overwritten.
4. Launch CS2 and run `exec autoexec.cfg` in the developer console, or add `+exec autoexec.cfg` to your Steam launch options so it loads automatically.

---

**Need tweaks?** Ping `@OhLasFar` on Twitter for questions or suggestions.

