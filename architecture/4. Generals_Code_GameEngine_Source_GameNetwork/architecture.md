# Architecture Overview

## Repository Shape
- `Generals/Code/GameEngine/Source/GameNetwork/` â Core networking code (multiplayer, GameSpy, LAN, UDP transport).
- `Generals/Code/GameEngine/Source/GameNetwork/GameSpy/` â GameSpy-specific modules (chat, ladder, threads, storage).
- `Generals/Code/GameEngine/Source/GameNetwork/WOLBrowser/` â Web browser integration for in-game content.
- Other subsystems (AI, rendering, UI) reside in separate directories.

## Major Subsystems

### Networking
- **Purpose**: Manages multiplayer communication, synchronization, and connectivity (UDP, NAT, GameSpy).
- **Key files**:
  - `Network.cpp` (singleton for game networking)
  - `Transport.cpp` (UDP sockets, encryption)
  - `ConnectionManager.cpp` (session management)
  - `GameSpy.cpp` (GameSpy integration)
- **Dependencies**: Uses `GameNetwork` (subsystem), `User.cpp` (player identities).

### GameSpy Integration
- **Purpose**: Handles online features (chat, lobbies, ladder, buddy list) via GameSpy.
- **Key files**:
  - `GameSpy.cpp` (core GameSpy logic)
  - `GameSpyChat.cpp` (chat system)
  - `Thread/PeerThread.cpp` (async peer communication)
  - `PersistentStorageThread.cpp` (player data storage)
- **Dependencies**: Relies on `Networking` subsystem for transport.

### LAN & P2P
- **Purpose**: Manages local multiplayer and peer-to-peer connections.
- **Key files**:
  - `LANAPI.cpp` (LAN lobby/game management)
  - `NAT.cpp` (NAT traversal)
  - `FileTransfer.cpp` (map/file sharing)
- **Dependencies**: Uses `Networking` for transport, `GameNetwork` for commands.

### Frame Synchronization
- **Purpose**: Ensures consistent game state across clients via frame-based commands.
- **Key files**:
  - `FrameDataManager.cpp` (command buffering)
  - `FrameMetrics.cpp` (latency/performance tracking)
- **Dependencies**: Depends on `Networking` for command delivery.

## Key Runtime Flows

### Initialization
1. `Network.cpp` initializes transport (`Transport.cpp`), GameSpy (`GameSpy.cpp`), and LAN APIs (`LANAPI.cpp`).
2. `User.cpp` sets up player identities.
3. GameSpy threads (`PeerThread.cpp`, `BuddyThread.cpp`) start for async operations.

### Main Loop / Per-Frame
1. `Network.cpp` processes incoming packets (`NetPacket.cpp`), updates frame data (`FrameDataManager.cpp`), and syncs game state.
2. GameSpy modules poll for chat/lobby updates (`GameSpyChat.cpp`, `LobbyUtils.cpp`).
3. NAT traversal (`NAT.cpp`) and file transfers (`FileTransfer.cpp`) run as needed.

### Shutdown
1. GameSpy threads terminate (`PeerThread.cpp` cleanup).
2. `Network.cpp` closes sockets (`Transport.cpp`), disconnects peers (`DisconnectManager.cpp`).
3. Resources (e.g., web browser `WebBrowser.cpp`) are released.

## Notable Details
- **Global State**: `Network` singleton owns all networking state (connections, commands, GameSpy).
- **Ownership**: `FrameDataManager` owns frame-based command buffers; `ConnectionManager` owns session state.
- **Design Patterns**: Heavy use of message queues (e.g., `PeerThread.cpp`) for async GameSpy operations.
