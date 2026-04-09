# Architecture Overview

## Repository Shape
- Root contains `Game`, `Engine`, `W3D`, `UI`, `Audio`, `Network`, and `Mods` directories.
- `Game` holds game-specific logic (units, buildings, missions).
- `Engine` contains core systems (AI, rendering, input).
- `W3D` is the 3D rendering subsystem.

## Major Subsystems

### Game Logic
- **Purpose**: Manages units, buildings, resources, and game rules.
- **Key files**: `GameCore.cpp`, `Unit.cpp`, `Building.cpp`, `Mission.cpp`
- **Dependencies**: AI, W3D, UI, Network

### AI
- **Purpose**: Handles pathfinding, unit behavior, and strategic decisions.
- **Key files**: `AI.cpp`, `Pathfinder.cpp`, `BehaviorTree.cpp`
- **Dependencies**: Game Logic, W3D

### W3D (Rendering)
- **Purpose**: 3D graphics rendering, animations, and scene management.
- **Key files**: `W3DRenderer.cpp`, `Model.cpp`, `Shader.cpp`
- **Dependencies**: Game Logic, Input

### Networking
- **Purpose**: Multiplayer synchronization, peer-to-peer communication.
- **Key files**: `Network.cpp`, `Packet.cpp`, `Replication.cpp`
- **Dependencies**: Game Logic, UI

### UI
- **Purpose**: Handles menus, HUD, and user input.
- **Key files**: `UIManager.cpp`, `HUD.cpp`, `Menu.cpp`
- **Dependencies**: Game Logic, Input

### Audio
- **Purpose**: Sound effects, music, and voiceovers.
- **Key files**: `AudioSystem.cpp`, `Sound.cpp`, `Music.cpp`
- **Dependencies**: Game Logic

### Modding Infrastructure
- **Purpose**: Supports custom content via scripts and asset overrides.
- **Key files**: `ModManager.cpp`, `ScriptEngine.cpp`, `AssetLoader.cpp`
- **Dependencies**: Game Logic, W3D, Audio

## Key Runtime Flows

### Initialization
1. `main()` â `Engine::Initialize()` (W3D, Audio, Network setup).
2. `Game::LoadMission()` (Game Logic, W3D asset loading).
3. `UI::Initialize()` (HUD, menus).

### Main Loop / Per-Frame
1. `Engine::Update()` â AI, Game Logic, Network.
2. `W3D::RenderFrame()` (calls Game Logic for object transforms).
3. `UI::RenderHUD()` (overlay on W3D output).
4. `Audio::Update()` (spatialized sound).

### Shutdown
1. `Network::Disconnect()`.
2. `Game::UnloadMission()`.
3. `Engine::Shutdown()` (W3D, Audio cleanup).

## Notable Details
- **Global State**: `GameState.cpp` holds shared game data (resources, victory conditions).
- **Ownership**: W3D owns rendering resources; Game Logic owns game objects.
- **Design Pattern**: Event-driven for UI/Network; ECS-like for Game Logic (components in `Unit.cpp`).
