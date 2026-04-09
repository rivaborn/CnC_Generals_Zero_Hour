# GeneralsMD/Code/GameEngine/Source/GameClient/GameClientDispatch.cpp

## Purpose
Handles client-side message dispatching for the game client, filtering messages before they are sent to the network.

## Responsibilities
- Filters game messages based on type
- Determines whether messages should be kept or destroyed
- Handles specific message types (new game, clear game data, frame tick)

## Key Types
- None

## Key Functions
### GameClientMessageDispatcher::translateGameMessage
- Purpose: Determines the disposition of a game message for network transmission.
- Calls: `msg->getType()`, `TheGameClient->getFrame()`

## Globals
- None

## Dependencies
- `GameMessage` (from Common/MessageStream.h)
- `GameClient` (from GameClient/GameClient.h)
- `GameMessageDisposition` enum (from Common/MessageStream.h)
