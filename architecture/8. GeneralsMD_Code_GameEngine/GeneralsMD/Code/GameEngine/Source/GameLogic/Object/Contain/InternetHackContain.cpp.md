# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Contain/InternetHackContain.cpp

## Purpose
Implements a containment module that triggers the "aiHackInternet" command for passengers when they enter a containing object.

## Responsibilities
- Inherits from `TransportContain` to extend containment behavior
- Calls `aiHackInternet` on passenger AI when contained
- Implements standard SAGE module methods (CRC, Xfer, loadPostProcess)

## Key Types
- `InternetHackContainModuleData` (Class): Module data container (empty implementation)
- `InternetHackContain` (Class): Main containment module class that triggers hacking

## Key Functions
### `InternetHackContain::onContaining`
- Purpose: Triggers AI hacking when an object is contained
- Calls: `TransportContain::onContaining`, `rider->getAI()->aiHackInternet`

### `InternetHackContain::crc`
- Purpose: Serialization CRC calculation
- Calls: `TransportContain::crc`

### `InternetHackContain::xfer`
- Purpose: Serialization/deserialization
- Calls: `TransportContain::xfer`

### `InternetHackContain::loadPostProcess`
- Purpose: Post-load initialization
- Calls: `TransportContain::loadPostProcess`

## Globals
None

## Dependencies
- `PreRTS.h`, `InternetHackContain.h`, `Object.h`, `AIUpdate.h`
- `TransportContain`, `MultiIniFieldParse`, `Xfer`, `Thing`, `Object`, `Bool`
