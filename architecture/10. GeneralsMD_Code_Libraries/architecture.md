# Architecture Overview

## Repository Shape
- Root contains `Game`, `Engine`, `W3D`, `UI`, `Audio`, `Network`, and `Mods` directories.
- `Game` holds game-specific logic (units, buildings, missions).
- `Engine` contains core systems (AI, rendering, input).
- `W3D` is the 3D rendering subsystem.

## Major Subsystems

### Game Logic
- Purpose: Manages units, buildings, resources, and game rules.
- Key files: `Game.cpp`, `Unit.cpp`, `Building.cpp`, `Mission.cpp`
- Dependencies: AI, W3D, UI

### AI
- Purpose: Handles pathfinding, unit behavior, and tactical decisions.
- Key files: `AI.cpp`, `Pathfinder.cpp`, `TacticalAI.cpp`
- Dependencies: Game Logic, W3D

### W3D (Rendering)
- Purpose: 3D graphics rendering, animation, and scene management.
- Key files: `W3D.cpp`, `Model.cpp`, `Scene.cpp`
- Dependencies: None (low-level)

### Networking
- Purpose: Multiplayer synchronization and peer-to-peer communication.
- Key files: `Network.cpp`, `Packet.cpp`, `GameSpy.cpp`
- Dependencies: Game Logic, UI

### UI
- Purpose: Handles menus, HUD, and user input.
- Key files: `UI.cpp`, `HUD.cpp`, `Menu.cpp`
- Dependencies: Game Logic, W3D

### Audio
- Purpose: Sound effects, music, and voiceovers.
- Key files: `Audio.cpp`, `Sound.cpp`, `Music.cpp`
- Dependencies: None (low-level)

### Modding Infrastructure
- Purpose: Allows custom content via scripts and asset overrides.
- Key files: `Mod.cpp`, `Script.cpp`, `AssetManager.cpp`
- Dependencies: Game Logic, W3D, UI

## Key Runtime Flows

### Initialization
1. W3D initializes rendering context.
2. Game Logic loads mission data.
3. AI initializes pathfinding and behaviors.
4. Networking establishes connection (if multiplayer).
5. UI loads menus and HUD.

### Main Loop / Per-Frame
1. Input polling (UI/Network).
2. AI updates unit behaviors.
3. Game Logic processes rules and state.
4. W3D renders scene.
5. Audio updates sound sources.
6. Networking sends/receives packets.

### Shutdown
1. Networking disconnects.
2. Game Logic saves state (if needed).
3. W3D releases resources.
4. Audio stops all sounds.

## Notable Details
- Global state managed via `GameState` singleton.
- W3D owns rendering resources; other subsystems reference them.
- Modding uses script hooks into Game Logic and UI.
