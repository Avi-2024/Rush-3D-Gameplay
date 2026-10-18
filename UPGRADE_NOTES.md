# Night Rush 3D — October 2026 Upgrade Notes

### Implemented on `main`
- P0: six car variants (distinct paint, wings/decal/lighting accents), extra roadway edge lights, crash shake/flash, nitro speed streaks
- P0: graphics quality options (Auto, Battery, Quality), WebGL fallback/context-loss handling and basic render error messaging
- P1: six-car garage with five credit-priced unlocks and local save persistence
- P1: four milestone missions, one changing daily task with a claim lock, and five achievements; credits and rewards persist
- P1: independently toggleable engine/effects and **original procedural background music** (no licensed audio files / third-party services)
- P2: three visual track/weather presets (City, Sunset, Rain) and two gameplay modes (Endless, 90-second Sprint)

### How music works
The music is generated on-device using the Web Audio API. Because browser autoplay rules block audio before user gestures, press **Start Race** to begin. In the race setup, use **Music** and **Effects** toggles independently. Their states save in localStorage. No music MP3 is downloaded, and no third-party audio license is needed for this synthesized arrangement.

### Saves
`nightRush3DBest` stores personal best. `nightRush3DProfile` stores earned credits, owned/selected car, mission completion and lifetime run statistics. `nightRush3DSettings` stores track/mode/quality/music/effects settings. There is no cloud save; clearing site data removes progression.

### Reality check
- These are playable visual environments on one highway configuration, not three uniquely modeled race circuits.
- Driving remains arcade lane switching, not drift-physics simulation.
- Race progress saves locally; there is no server leaderboard or cross-device sync.
- Music, graphics and controls should be checked on actual target devices before public promotion.
- **AdSense is not activated.** Read `ADSENSE_SETUP.md`, set up an appropriate domain and policy/consent handling, and apply for approval before adding ad code.

### Next quality pass
1. Realistic handling curve, wheel spinning, tire marks, collision damage state
2. Additional track geometry/branches and proper weather particle GPU batches
3. Optimize GPU draw calls via geometry merging/instancing; verify 30/60 FPS on low-end phones
4. More distinctive vehicle silhouettes, garage preview with turntable, car performance attributes
5. Gameplay balancing and automated accessibility/browser checks
