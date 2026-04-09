# Generals/Code/GameEngine/Source/GameClient/GameClientDispatch.cpp

## Purpose
Handles client-side message dispatching for the game client, filtering messages before they are sent over the network.

## Responsibilities
- Filters and processes game messages before network transmission
- Determines message disposition (keep/destroy)
- Handles specific message types (new game, clear data, frame ticks)

## Key Types
- GameClientMessageDispatcher (Class): message dispatcher for client-side filtering
- GameMessageDisposition (Enum): message handling disposition (KEEP_MESSAGE/DESTROY_MESSAGE)

## Key Functions
### GameClientMessageDispatcher::translateGameMessage
- Purpose: Determines whether a game message should be kept or destroyed before network transmission
- Calls: msg->getType(), TheGameClient->getFrame()

## Globals
- None

## Dependencies
- PreRTS.h (include)
- Common/MessageStream.h (include)
- GameClient/GameClient.h (include)
- GameMessage (external class)
- TheGameClient (external global)
