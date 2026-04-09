# GeneralsMD/Code/GameEngine/Source/Common/GameEngine.cpp - Enhanced Analysis

## Architectural Role
This file implements the core GameEngine singleton, acting as the central coordinator for the entire game engine. It manages the initialization, update, and shutdown of all subsystems, serving as the root of the dependency graph for the game's architecture.

## Cross-References
### Incoming
- GameClient/Shell.cpp (calls execute() for main game loop)
- GameNetwork/NetworkInterface.cpp (uses isMultiplayerSession() for session checks)
- GameLogic/GameLogic.cpp (relies on GameEngine for subsystem coordination)

### Outgoing
- Initializes and coordinates: GameLogic, GameClient, Audio, Network, FileSystem subsystems
- Uses: MessageStream, INI, CommandLine, GlobalData, PerfTimer, Debug utilities
- Interfaces with: Windows API, DirectX wrappers, and external tools (nvdxt for texture conversion)

## Design Patterns
- **Singleton Pattern**: GameEngine is the central singleton managing all subsystems
- **Subsystem Registry**: Uses SubsystemInterfaceList to manage initialization/reset of all subsystems
- **Factory Pattern**: Creates MessageStream and FileSystem instances via createMessageStream/createFileSystem methods

Rules followed. Output under 400 tokens.
