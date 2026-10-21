APEX RACING 3D — FULL GAME PACKAGE

FILES
- index.html: game interface
- style.css: visual design and layout
- script.js: gameplay, tracks, vehicles, AI drivers, scenery, garage and race systems

HOW TO RUN IN VS CODE
1. Extract this ZIP to a folder.
2. Open that folder in VS Code.
3. Install the Live Server extension if needed.
4. Right-click index.html and choose Open with Live Server.
5. An internet connection is needed for the external Three.js modules used by the game.

AI SPEED UPDATE
AI target pace has been increased by 12%, and the current-speed cap has been raised to allow the cars to use the extra pace. Corner-speed control, passing behavior and stall recovery remain in place.

Update: AI pace has been restored to the normal speed/skill/cornering calculation, with chase-speed boosts removed. Track fences are now substantially taller (about 2.55 game units) with raised rails and mesh.


AI RESTORE
- Restored the original three-opponent race field and earlier AI speed/difficulty behavior.
- Kept the newer maps, crystal/cavern scenery, random starting position, smoother corners, and taller fences.
- JavaScript syntax checked with Node; run in Live Server to verify gameplay and visual placement.

AI speed update: AI racers are faster at every difficulty. Easy: 24, Medium: 31, Hard: 38, Expert: 44. The three racers have slightly less speed separation so the field feels more competitive.

AI difficulty speed update: Easy 70%, Medium 85%, Hard 100%, Expert 110% of the player car top speed. The AI speed automatically follows the player car and upgrades.

AI update: AI racers are capped at the player car's actual top-speed limit, with Easy/Medium/Hard/Expert at 70%/82%/92%/100%. Use the AI RACERS selector in the top bar to choose 1–10 opponents. The painted road edge no longer snaps the car back; the physical metal fence colliders are the boundary.


LATEST UPDATE
- AI level slider now ranges from 1 to 100 with smoother difficulty scaling.
- AI driving is slightly more competitive while retaining the player-based speed cap.
- When 2 PLAYER is enabled, the Garage becomes a split selection layout: Player 1 on the left and a dedicated Player 2 car selector on the right.
- Circuit scenery density has been increased with more trackside details and biome props across maps.

AI slider speed calibration: AI LEVEL 70 matches the player car top-speed limit. Levels below 70 scale AI top speed proportionally; levels above 70 remain at the player speed cap, while higher levels improve AI skill and reduce driving mistakes.

AI SPEED UPDATE
AI speed is increased by 15% relative to its prior level-based target. Level 70 targets 115% of the player top-speed baseline; higher levels remain capped at 115%. Launch acceleration behavior is unchanged.

Player 2 speed fix: Player 2 now uses the same car upgrade formulas, acceleration/braking baseline, top-speed multiplier, and rain speed cap as Player 1. Same-car races should no longer make Player 2 slower because of a lower hardcoded speed cap.

OPTIONAL CRASH EXPLOSION + RESPAWN SETTING
- Use the CRASH FX: OFF / ON button in the race options bar to enable or disable it.
- When enabled, a hard collision at speed with a metal fence or another car creates a short explosion effect and respawns the player at the race starting grid.
- The setting is remembered in this browser using local storage. It starts disabled by default unless previously enabled.
- The feature supports Player 1 and Player 2.

Crash cutscene and recovery choices
-----------------------------------
When CRASH FX is enabled, a hard impact now pauses the race for a brief camera cutscene showing the explosion. A choice screen then lets the crashed player either restart at the starting grid or continue from the crash location with speed reset to zero. The choice screen is intended to support both Player 1 and Player 2 crashes.

CONTINUE AFTER CRASH — ON-TRACK RESUME
- Choosing CONTINUE FROM CRASH now returns the crashed car to the asphalt at the same progress point along the circuit where the crash happened. If the impact pushed the car off the road, its lateral position is clamped to a safe on-road lane. Speed is reset to zero and the car faces along the track. RESTART AT START remains unchanged.
