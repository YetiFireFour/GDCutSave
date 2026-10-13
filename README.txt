GDCutSave - cloud-build starter package

IMPORTANT: This ZIP does not include a compiled .geode binary. It contains the source and a GitHub Actions workflow that builds it remotely, so you do not need to install CMake or a compiler on your PC. You do need to upload this folder to a GitHub repository and run the workflow; GitHub will provide the compiled artifact if the build succeeds.

FAST PATH
1. Create a GitHub repository and upload the contents of this ZIP (not the ZIP itself).
2. Open the repository's Actions tab.
3. Select "Build GDCutSave" and click "Run workflow" (or push to main).
4. When it finishes successfully, download the "GDCutSave-geode" artifact. Extract the .geode file and put it in your Geode mods folder.

WHAT THIS STARTER CAPTURES
- Current completion percentage and frame counter
- Player 1 and player 2 transforms when available
- Accessible level-object positions, rotations, scales, visibility and opacity
- Appends each snapshot as one JSON line to the mod save directory's cuts.jsonl
- Ignores F while paused or outside active gameplay

LIMITATIONS
This is a snapshot recorder, not a complete deterministic cut/replay system. Capturing transforms does not restore trigger history, RNG state, physics internals, particles, or every internal object state. The source/API bindings may need adjustments for your installed Geode SDK/game version. The cloud build is the validation step; if it fails, inspect the Actions log and adjust the code accordingly.

Target in mod.json: Geometry Dash Windows 2.2081, Geode SDK v4 series. Update the target to match your installed environment if needed.
