# Jetpack Dhub

A 2D Unity game where a jetpack-powered dhub navigates palm obstacles, collects coins and earns a date-based round rating.

## Open the project
- Editor version recorded by the project: **6000.5.3f1**.
- Extract the project, then add its root folder in Unity Hub. Use the matching editor version.
- Allow Unity to restore the packages declared in Packages/manifest.json and packages-lock.json.
- Open Assets/Scenes/MenuScene.unity and press Play.
- Both MenuScene and GameScene are enabled in the saved build scene list.

## Controls and gameplay
Press Space or left-click to activate the jetpack. Select Easy or Hard in the menu. Pass palms for points and collect coins. Ground contact ends the round immediately.

Current GameScene settings: 60-second rounds, 100 energy, 5 damage per obstacle hit, a shield every **3 coins**, shield duration 5 seconds. The first obstacle hit consumes the shield. A new shield refreshes its duration. Ratings require 3, 8 and 15 obstacle points. Scene Inspector settings override C# field defaults.

| Difficulty | Obstacle speed | Pair center separation | Spawn interval |
|---|---:|---:|---:|
| Easy | 5 | 10 | 1.9 seconds |
| Hard | 6.5 | 9 | 1.3 seconds |

The obstacle gap value positions obstacle transforms; actual visible clearance also depends on sprite and collider geometry.

## Project contents
Assets contains scenes, prefabs, artwork, audio, fonts and scripts, including their original .meta files. Packages and ProjectSettings preserve dependencies and editor configuration. Generated caches and builds are excluded by .gitignore.

## Review status
This revision was statically reviewed and packaged; it has **not been compiled or play-tested in Unity here**. See REVIEW.md for changes and the required play-test checklist. The previously supplied Windows build predates these source changes and has not been rebuilt.

Hourglass sand animation references and jetpack exhaust particles are currently unassigned in the scene. These optional effects are guarded in code; no replacement artwork or effects were invented.

