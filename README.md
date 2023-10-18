# CS2-Crosshair-Enhancement

This configuration is designed for CS2 players to automatically adjust crosshair colors and Follow Recoil settings based on in-game actions.

## Credits
- **u/craygroupious**: [Reddit Post](https://www.reddit.com/r/GlobalOffensive/comments/16wgzkp/comment/k2x048d/)
- **u/Vipitis**: [Reddit Post](https://www.reddit.com/r/GlobalOffensive/comments/16a3yyr/recoil_crosshair_switching_bind_for_cs2/)

---

## Features

1. **Crosshair Colors Configuration**
   - Change crosshair color when the "Follow Crosshair" is activated or deactivated.
   - Customizable RGB values ranging from 0 to 255.

2. **Shooting Binds**
   - Automatically activate or deactivate follow recoil settings when shooting.

---

## Configurations

### Shooting Binds

- When shooting, the Follow Recoil setting is activated and the crosshair color is set to "Activated Color".
- When not shooting, the Follow Recoil setting is deactivated and the crosshair color is set to "Deactivated Color".

### Weapon Selection Binds

- **Secondary Weapon**: Press `3` 
  - Sets mouse1 to normal attack.
- **Primary Weapon**: Press `2`
  - Sets mouse1 to shooting with the "Activated Color" and recoil enabled.
- **Melee Weapon**: Press `1`
  - Sets mouse1 to shooting with the "Deactivated Color" and recoil disabled.

---

## Installation

1. Copy the provided configuration.
2. Navigate to your CS2 game directory and locate the `C:\Program Files (x86)\Steam\steamapps\common\Counter-Strike Global Offensive\game\csgo\cfg` folder.
3. Create a new file named `autoexec.cfg` (if it doesn't already exist).
4. Paste the copied configuration into this file. (You may need to adjust it to your settings)
5. Save and close the file.
6. In CS2, open the console and type `exec autoexec.cfg` to run the configuration1 or add exec `exec autoexec.cfg` in your launch options.

---

**Note**: Ensure that the binding for mouse1 remains as provided to guarantee functionality.

For further customization or inquiries, refer to @OhLasFar on Twitter.

