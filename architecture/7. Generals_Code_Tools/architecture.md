# Architecture Overview

## Repository Shape
- Root contains `Game`, `Engine`, `Tools`, and `Data` directories.
- `Engine` houses core systems (rendering, audio, networking).
- `Game` contains game-specific logic (units, buildings, missions).
- `Data` holds assets (models, textures, scripts).

## Major Subsystems

### Game Logic
- Purpose: Manages units, buildings, and game rules.
- Key files: `Game.cpp`, `Unit.cpp`, `Building.cpp`, `Mission.cpp`
- Dependencies: Rendering (W3D), AI, UI

### AI
- Purpose: Handles pathfinding, unit behavior, and strategy.
- Key files: `AI.cpp`, `Pathfinder.cpp`, `BehaviorTree.cpp`
- Dependencies: Game Logic, Rendering

### Rendering (W3D)
- Purpose: 3D graphics rendering using the W3D engine.
- Key files: `W3D.cpp`, `Renderer.cpp`, `Model.cpp`
- Dependencies: Game Logic, Input

### Networking
- Purpose: Multiplayer synchronization and communication.
- Key files: `Network.cpp`, `Packet.cpp`, `Replay.cpp`
- Dependencies: Game Logic, Input

### UI
- Purpose: Handles menus, HUD, and user input.
- Key files: `UI.cpp`, `HUD.cpp`, `Menu.cpp`
- Dependencies: Game Logic, Input

### Audio
- Purpose: Manages sound effects and music.
- Key files: `Audio.cpp`, `Sound.cpp`, `Music.cpp`
- Dependencies: Game Logic

### Modding Infrastructure
- Purpose: Supports custom content and game modifications.
- Key files: `Mod.cpp`, `Script.cpp`, `AssetLoader.cpp`
- Dependencies: Game Logic, Rendering, Audio

## Key Runtime Flows

### Initialization
1. Engine initializes subsystems (rendering, audio, networking).
2. Game logic loads mission data and initializes game state.
3. UI sets up menus and HUD.

### Main Loop / Per-Frame
1. Input is processed (keyboard, mouse, network).
2. AI updates unit behaviors and pathfinding.
3. Game logic updates game state.
4. Rendering and audio systems update based on game state.
5. UI renders menus and HUD.

### Shutdown
1. Networking disconnects and saves replays.
2. Game logic cleans up resources.
3. Engine shuts down subsystems.

## Notable Details
- Global game state is managed in `Game.cpp`.
- Ownership boundaries are defined by subsystem dependencies.
- Event-driven design for AI and networking.
