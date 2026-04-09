# GeneralsMD/Code/GameEngine/Include/Common/SubsystemInterface.h

## Purpose
Defines the abstract base class and management framework for game engine subsystems.

## Responsibilities
- Provides interface for subsystem initialization, updates, and rendering
- Manages subsystem lifecycle (init, reset, shutdown)
- Tracks performance metrics (when DUMP_PERF_STATS enabled)
- Maintains a global registry of all subsystems

## Key Types
- **SubsystemInterface (Class)**: Abstract base for all game engine subsystems
- **SubsystemInterfaceList (Class)**: Manages collection of subsystems
- **SubsystemList (Class)**: Typedef for vector of SubsystemInterface pointers
- **Xfer (Class)**: Forward declaration (external transfer object)

## Key Functions
### SubsystemInterface::init
- Purpose: Initialize subsystem with default values and allocate resources
- Calls: None (pure virtual)

### SubsystemInterface::update
- Purpose: Perform per-frame processing for the subsystem
- Calls: None (pure virtual)

### SubsystemInterface::reset
- Purpose: Reset subsystem to empty state ready for new data
- Calls: None (pure virtual)

### SubsystemInterfaceList::initSubsystem
- Purpose: Initialize a subsystem with configuration paths and transfer object
- Calls: SubsystemInterface::init, INI-related functions

### SubsystemInterfaceList::postProcessLoadAll
- Purpose: Call postProcessLoad on all registered subsystems
- Calls: SubsystemInterface::postProcessLoad

## Globals
- **TheSubsystemList (SubsystemInterfaceList*)**: Global registry of all subsystems

## Dependencies
- Common/INI.h (INI configuration)
- Common/STLTypedefs.h (STL typedefs)
- Xfer class (external transfer object)
