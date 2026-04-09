# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Contain/OverlordContain.cpp

## Purpose
Implements a specialized containment module for the Overlord unit, which redirects containment queries to its passenger when full.

## Responsibilities
- Manages dynamic redirection of containment operations to the first passenger
- Handles payload creation and management
- Controls experience sinking for passengers
- Manages death/capture sequences with proper redirection handling

## Key Types
- **OverlordContainModuleData (struct)**: Stores module configuration including payload templates and experience settings
- **OverlordContain (class)**: Main containment module class that handles redirection logic

## Key Functions
### createPayload
- Purpose: Creates initial payload objects defined in module data
- Calls: `TheThingFactory->newObject`, `contain->addToContain`

### getRedirectedContain
- Purpose: Returns the containment interface of the first passenger if redirection is active
- Calls: None (direct member access)

### onDie
- Purpose: Handles death sequence with proper redirection deactivation
- Calls: `deactivateRedirectedContain`, `myGuy->kill`, `TransportContain::onDie`

### onContaining
- Purpose: Handles passenger loading with redirection activation
- Calls: `activateRedirectedContain`, `obj->getExperienceTracker()->setExperienceSink`

### isValidContainerFor
- Purpose: Checks container validity, redirecting to passenger if applicable
- Calls: `TransportContain::isValidContainerFor` or `getRedirectedContain()->isValidContainerFor`

## Globals
- None

## Dependencies
- Key includes: `PreRTS.h`, `Common/Player.h`, `GameLogic/Module/OverlordContain.h`
- External symbols: `TheThingFactory`, `TheGameLogic`, `INI` class methods
