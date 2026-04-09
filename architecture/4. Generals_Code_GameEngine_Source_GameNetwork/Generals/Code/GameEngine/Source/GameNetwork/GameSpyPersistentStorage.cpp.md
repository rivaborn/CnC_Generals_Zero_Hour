# Generals/Code/GameEngine/Source/GameNetwork/GameSpyPersistentStorage.cpp

## Purpose
Manages GameSpy persistent storage for player data (locale, wins, losses) via callbacks and connection handling.

## Responsibilities
- Handles GameSpy persistent storage connection and authentication
- Manages player profile data (locale, wins, losses) synchronization
- Provides callbacks for data retrieval and updates
- Thread-safe operations via mutex locks
- Global key/value peer synchronization

## Key Types
- **GameSpyPlayerInfo (Class)**: Manages player profile data and server synchronization
- **GameSpyPlayerInfoInterface (Class)**: Abstract interface for player info (not shown in file)

## Key Functions
### `gameSpyInitPersistentStorageConnection`
- Purpose: Initializes and authenticates GameSpy persistent storage connection
- Calls: `InitStatsConnection`, `PreAuthenticatePlayerPM`, `PersistThink`

### `getPersistentDataCallback`
- Purpose: Handles retrieved player data and updates local state
- Calls: `TheGameSpyPlayerInfo->setLocale`, `TheGameSpyPlayerInfo->setWins`, `TheGameSpyPlayerInfo->setLosses`, `peerSetGlobalKeys`, `peerSetGlobalWatchKeys`

### `setPersistentDataCallback`
- Purpose: Handles confirmation of data updates to server
- Calls: None (direct)

### `createGameSpyPlayerInfo`
- Purpose: Factory function to create GameSpyPlayerInfo instance
- Calls: `NEW GameSpyPlayerInfo`

## Globals
- **isProfileAuthorized (Bool)**: Tracks authentication status
- **TheGameSpyPlayerInfo (GameSpyPlayerInfoInterface**)**: Global player info instance

## Dependencies
- GameSpy SDK headers (`gpersist.h`)
- Game engine modules: `GameSpy.h`, `GameSpyGP.h`, `GameSpyThread.h`
- Core utilities: `PreRTS.h`, `Shell.h`, `MessageBox.h`
