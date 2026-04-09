# GeneralsMD/Code/GameEngine/Include/GameNetwork/GameSpyChat.h

## Purpose
Header for GameSpy chat functionality in Command & Conquer Generals Zero Hour.

## Responsibilities
- Declares GameSpy chat API functions
- Defines callback handlers for chat messages
- Exposes global UI window pointers for chat interfaces

## Key Types
- GameWindow (Class): UI window container
- WindowLayout (Class): UI layout manager
- PEER (Type): GameSpy peer connection handle
- RoomType (Enum): Type of GameSpy room
- MessageType (Enum): Type of GameSpy message

## Key Functions
### GameSpySendChat
- Purpose: Sends a chat message to GameSpy server
- Calls: Not inferable

### GameSpyAddText
- Purpose: Adds text to a chat window
- Calls: Not inferable

### RoomMessageCallback
- Purpose: Handles room chat messages from GameSpy
- Calls: Not inferable

### PlayerMessageCallback
- Purpose: Handles private messages from other players
- Calls: Not inferable

## Globals
- progressTextWindow (GameWindow*): Text box on progress screen
- quickmatchTextWindow (GameWindow*): Text box on quickmatch screen
- listboxLobbyChat (GameWindow*): Chat box on custom lobby
- listboxLobbyPlayers (GameWindow*): Player list on custom lobby
- listboxLobbyGames (GameWindow*): Game list on custom lobby
- listboxLobbyChatChannels (GameWindow*): Chat channel list
- listboxGameSetupChat (GameWindow*): Chat box on game setup
- WOLMapSelectLayout (WindowLayout*): Map selection overlay

## Dependencies
- "GameSpy/Peer/Peer.h" (GameSpy peer API)
- UnicodeString (string type)
- Bool (boolean type)
- GameSpyColors enum (color
