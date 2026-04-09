# Generals/Code/GameEngine/Source/GameLogic/Object/Behavior/BridgeBehavior.cpp

## Purpose
This file contains the implementation of the `BridgeBehavior` class, which manages the behavior and logic for bridges in the game, including scaffolding creation, removal, and state management.

## Responsibilities
- Manage bridge scaffolding creation and removal.
- Handle bridge damage and repair effects.
- Update bridge state and interact with AI pathfinding.
- Serialize and deserialize bridge data.

## Key Types
- `BridgeBehaviorModuleData`: Stores configuration data for bridge behavior.
- `TimeAndLocationInfo`: Holds timing and location information for effects.
- `BridgeFXInfo` and `BridgeOCLInfo`: Store FX and OCL (Object Creation List) information with timing details.

## Key Functions
### parseTimeAndLocationInfo
- Purpose: Parses time and optional bone location information from an INI file.
- Calls:
  - `ini->getNextToken`
  - `ini->parseDurationUnsignedInt`
  - `ini->getNextAsciiString`

### BridgeBehavior::BridgeBehavior
- Purpose: Constructor for the bridge behavior module, initializes data members.

### BridgeBehavior::~BridgeBehavior
- Purpose: Destructor, destroys associated tower objects if present.

### BridgeBehavior::resolveFX
- Purpose: Resolves FX and OCL lists based on the current bridge template.

### BridgeBehavior::createScaffolding
- Purpose: Creates scaffolding objects for a bridge, including support layers.

### BridgeBehavior::removeScaffolding
- Purpose: Removes scaffolding by reversing the motion of scaffold objects.

## Globals
- None

## Dependencies
- Includes headers from various modules such as `GameLogic`, `Common`, and `GameClient`.
- Uses external symbols like `TheGameLogic`, `TheTerrainLogic`, `TheThingFactory`, etc.
