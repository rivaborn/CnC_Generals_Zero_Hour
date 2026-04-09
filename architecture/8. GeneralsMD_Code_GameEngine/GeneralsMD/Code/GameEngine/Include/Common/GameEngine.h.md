# GeneralsMD/Code/GameEngine/Include/Common/GameEngine.h

## Purpose
Defines the core GameEngine class and its interface for the SAGE engine.

## Responsibilities
- Manages game initialization, updates, and execution
- Provides factory methods for core subsystems
- Handles frame rate limiting and application state
- Serves as the central singleton for game engine access

## Key Types
- **GameEngine (Class)**: Core game engine interface
- **SubsystemInterface (Class)**: Base interface for engine subsystems
- **GameType (Type)**: Not inferable

## Key Functions
### CreateGameEngine
- Purpose: Creates a new GameEngine instance
- Calls: Not inferable

### GameMain
- Purpose: Entry point for the game system
- Calls: Not inferable

## Globals
- **TheGameEngine (GameEngine*)**: Singleton instance of the game engine

## Dependencies
- Common/SubsystemInterface.h
- Common/GameType.h
- Forward declarations for AudioManager, GameLogic, GameClient, etc.
