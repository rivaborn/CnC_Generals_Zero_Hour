# Architecture Overview

## Repository Shape
- **Source Code**: Contains the main game logic, AI, rendering, networking, UI, and audio code.
- **Data Files**: Includes maps, models, textures, and other assets.
- **Tools**: Development tools for map editing, asset creation, and debugging.
- **Documentation**: API references, design documents, and user guides.

## Major Subsystems
### Game Logic
- **Purpose**: Manages the game state, rules, and progression.
- **Key files**: `GameLogic.cpp`, `GameState.h`, `Rules.cpp`.
- **Dependencies**: AI, Rendering, Networking.

### AI
- **Purpose**: Controls non-player characters and strategic decisions.
- **Key files**: `AIController.cpp`, `BehaviorTree.h`, `Pathfinding.cpp`.
- **Dependencies**: Game Logic, Networking.

### Rendering (W3D)
- **Purpose**: Handles the visual presentation of the game world.
- **Key files**: `Renderer.cpp`, `ShaderManager.h`, `TextureLoader.cpp`.
- **Dependencies**: Game Logic, UI.

### Networking
- **Purpose**: Manages multiplayer communication and synchronization.
- **Key files**: `NetworkManager.cpp`, `PacketHandler.h`, `Session.cpp`.
- **Dependencies**: Game Logic, AI.

### UI
- **Purpose**: Provides the user interface for menus, HUDs, and other interactive elements.
- **Key files**: `UIManager.cpp`, `Widget.h`, `InputHandler.cpp`.
- **Dependencies**: Rendering, Game Logic.

### Audio
- **Purpose**: Manages sound effects and music.
- **Key files**: `AudioEngine.cpp`, `SoundManager.h`, `MusicPlayer.cpp`.
- **Dependencies**: None (independent).

## Key Runtime Flows
### Initialization
1. Load configuration settings.
2. Initialize subsystems in order: Networking, Game Logic, AI, Rendering, UI, Audio.

### Main Loop / Per-Frame
1. Handle input events.
2. Update game state and AI logic.
3. Render the frame.
4. Process network packets.
5. Play audio.

### Shutdown
1. Clean up resources.
2. Save game state if necessary.
3. Terminate subsystems in reverse order of initialization.

## Notable Details
- **Global State**: Managed by `GameState` class, accessible across subsystems.
- **Ownership Boundaries**: Subsystems are loosely coupled, with clear interfaces for communication.
- **Design Patterns**: Singleton pattern used for managing global resources like the renderer and audio engine. Observer pattern for UI updates based on game events.

---

This architecture overview synthesizes the provided per-subsystem overviews into a comprehensive document, highlighting the interactions between subsystems and key runtime flows.
