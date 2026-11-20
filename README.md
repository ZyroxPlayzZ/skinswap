# Skin Swap (Fabric, Minecraft 1.21.11)

Client-side mod. Pick a skin from PNG files with an in-game GUI.

1. Put 64x64 skin PNGs in `config/skinswap/skins/` (inside your profile's game folder).
2. Open the game, tap the **Skins** button (top-left of the title screen and pause menu).
3. Tap a skin to apply it. Toggle Classic/Slim if the arms look wrong.

Needs Fabric Loader + Fabric API for 1.21.11.

## Build
Push this folder to a GitHub repo. The Actions tab builds it; download the jar
from the finished run's "skinswap-jar" artifact (use the one without `-sources`).
On a PC: `gradle build` with Java 21.
