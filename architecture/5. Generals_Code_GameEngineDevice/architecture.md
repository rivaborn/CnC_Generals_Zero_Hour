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
- Purpose: Handles pathfinding, unit behavior, and strategic decisions.
- Key files: `AI.cpp`, `Pathfinder.cpp`, `BehaviorTree.cpp`
- Dependencies: Game Logic, W3D

### W3D (Rendering)
- Purpose: 3D graphics rendering, animation, and scene management.
- Key files: `W3DRenderer.cpp`, `Model.cpp`, `Shader.cpp`
- Dependencies: None (low-level)

### Networking
- Purpose: Multiplayer synchronization and peer-to-peer communication.
- Key files: `Network.cpp`, `Packet.cpp`, `Replication.cpp`
- Dependencies: Game Logic

### UI
- Purpose: Handles menus, HUD, and user input.
- Key files: `UIManager.cpp`, `HUD.cpp`, `Input.cpp`
- Dependencies: Game Logic, W3D

### Audio
- Purpose: Sound effects, music, and voice playback.
- Key files: `AudioSystem.cpp`, `Sound.cpp`, `Music.cpp`
- Dependencies: None (low-level)

### Modding Infrastructure
- Purpose: Supports custom content via scripts and asset overrides.
- Key files: `ModManager.cpp`, `ScriptEngine.cpp`, `AssetLoader.cpp`
- Dependencies: Game Logic, W3D, Audio

## Key Runtime Flows

### Initialization
1. W3D initializes rendering context.
2. Game Logic loads mission data.
3. AI initializes pathfinding and behavior trees.
4. Networking establishes connection (if multiplayer).
5. UI loads HUD and menus.

### Main Loop / Per-Frame
1. Input is polled (UI/Network).
2. AI updates unit behaviors.
3. Game Logic processes game state.
4. W3D renders scene.
5. Audio updates sound sources.
6. Networking sends/receives updates.

### Shutdown
1. Networking disconnects.
2. Game Logic cleans up resources.
3. W3D releases rendering context.

## Notable Details
- Global state is centralized in `GameState.cpp`.
- W3D owns all rendering resources.
- AI and Game Logic share ownership of unit data.
