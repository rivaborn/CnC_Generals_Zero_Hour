# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/OverlordContain.h

## Purpose
Defines the OverlordContain module, a specialized transport container that redirects queries to its first passenger when full.

## Responsibilities
- Manages containment logic with redirection behavior when full
- Handles passenger experience and payload management
- Overrides standard contain module functions for custom behavior
- Provides access to contained units and redirection state

## Key Types
- **OverlordContainModuleData (Class)**: Module data containing payload template names and experience sink flag
- **OverlordContain (Class)**: Main overlord contain class implementing redirection logic
- **OverlordContainMagicEnum (Enum)**: Not inferable (empty enum)
- **TemplateNameList (Class)**: List of template names for payload initialization

## Key Functions
### onBodyDamageStateChange
- Purpose: Handles damage state changes for the container
- Calls: Not inferable

### onDie
- Purpose: Cleanup when the container is destroyed
- Calls: Not inferable

### onCapture
- Purpose: Handles ownership transfer while preserving redirection
- Calls: Not inferable

### getRedirectedContain
- Purpose: Returns the contain module to redirect to when full
- Calls: Not inferable

### createPayload
- Purpose: Initializes the container with predefined payload
- Calls: Not inferable

## Globals
- **m_redirectionActivated (Bool)**: Tracks whether redirection is active

## Dependencies
- TransportContain.h
- GameLogic.h
- MultiIniFieldParse, INI classes
- Memory pool and module macros
- ContainModuleInterface, Object, Player, DamageInfo classes
