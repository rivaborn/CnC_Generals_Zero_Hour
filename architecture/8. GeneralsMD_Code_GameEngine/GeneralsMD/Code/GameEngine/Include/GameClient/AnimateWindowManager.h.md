# GeneralsMD/Code/GameEngine/Include/GameClient/AnimateWindowManager.h

## Purpose
Header for managing window animations in the game UI, defining animation types and control logic.

## Responsibilities
- Define animation types and window animation behavior
- Manage lists of animating windows
- Provide interface for registering and updating animations
- Handle animation reversal and reset to rest positions

## Key Types
- **AnimateWindow (Class)**: Represents a single window animation with position, velocity, and timing data
- **AnimTypes (Enum)**: Defines available animation types (slide right/left/top/bottom, spiral, etc.)
- **AnimateWindowManager (Class)**: Manages all window animations and their lifecycle
- **AnimateWindowList (typedef)**: List of AnimateWindow pointers for tracking animations

## Key Functions
### AnimateWindowManager::registerGameWindow
- Purpose: Registers a window for animation with specified parameters
- Calls: Not inferable (implementation in .cpp)

### AnimateWindowManager::update
- Purpose: Updates all active animations
- Calls: Not inferable (implementation in .cpp)

### AnimateWindowManager::reverseAnimateWindow
- Purpose: Reverses all active animations
- Calls: Not inferable (implementation in .cpp)

## Globals
- None

## Dependencies
- "Lib/BaseType.h" - Base types
- "Common/SubsystemInterface.h" - Subsystem base class
- "Common/GameMemory.h" - Memory management
- Forward references to various ProcessAnimateWindow* classes
