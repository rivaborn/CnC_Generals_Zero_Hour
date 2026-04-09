# Architecture Overview

## Repository Shape
- **Source Code**: Contains the main game logic, AI, rendering, networking, UI, and audio code.
- **Data Files**: Includes assets like models, textures, sounds, and configuration files.
- **Tools**: Development tools for map editing, asset creation, and debugging.
- **Documentation**: API documentation, design documents, and build instructions.

## Major Subsystems
### Game Logic
- **Purpose**: Manages the game state, rules, and progression.
- **Key Files**: `GameLogic.cpp`, `GameState.h`, `Rules.cpp`
- **Dependencies**: AI, Rendering, UI

### AI
- **Purpose**: Controls non-player characters (NPCs) and enemy behavior.
- **Key Files**: `AIController.cpp`, `BehaviorTree.h`, `Pathfinding.cpp`
- **Dependencies**: Game Logic, Networking

### Rendering (W3D)
- **Purpose**: Handles the visual presentation of the game world.
- **Key Files**: `Renderer.cpp`, `ShaderManager.h`, `TextureLoader.cpp`
- **Dependencies**: UI, Audio

### Networking
- **Purpose**: Manages multiplayer communication and synchronization.
- **Key Files**: `NetworkManager.cpp`, `PacketHandler.h`, `Session.cpp`
- **Dependencies**: Game Logic, AI

### UI
- **Purpose**: Provides the user interface for menus, HUDs, and in-game interactions.
- **Key Files**: `UIManager.cpp`, `WidgetFactory.h`, `InputHandler.cpp`
- **Dependencies**: Rendering, Game Logic

### Audio
- **Purpose**: Manages sound effects and music playback.
- **Key Files**: `AudioEngine.cpp`, `SoundManager.h`, `MusicPlayer.cpp`
- **Dependencies**: Rendering

## Key Runtime Flows
### Initialization
1. Load configuration files.
2. Initialize subsystems in order: Networking, Game Logic, AI, Rendering, UI, Audio.
3. Set up global state and resources.

### Main Loop / Per-Frame
1. Handle input events.
2. Update game logic and AI.
3. Render the frame.
4. Process audio.
5. Sync network state if multiplayer.

### Shutdown
1. Clean up resources.
2. Save game state if necessary.
3. Uninitialize subsystems in reverse order of initialization.

## Notable Details
- **Global State**: Managed by `GameState.h`, accessible to all subsystems.
- **Ownership Boundaries**: Subsystems own their specific data and resources, with clear interfaces for interaction.
- **Design Patterns**: Singleton pattern used for managing global services like `Renderer` and `AudioEngine`. Observer pattern for UI updates based on game events.
