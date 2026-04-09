# GeneralsMD/Code/GameEngine/Source/Common/GameMain.cpp

## Purpose
Main entry point for the game, initializing and running the game engine.

## Responsibilities
- Initialize the game engine via factory function
- Pass command-line arguments to the engine
- Execute the game loop
- Clean up resources on exit

## Key Types
None

## Key Functions
### GameMain
- Purpose: Entry point that initializes, runs, and cleans up the game engine.
- Calls: `CreateGameEngine()`, `TheGameEngine->init()`, `TheGameEngine->execute()`

## Globals
- `TheGameEngine` (GameEngine*): Global instance of the game engine.

## Dependencies
- `PreRTS.h` (included first)
- `Common/GameEngine.h`
- `CreateGameEngine()` (external factory function)
- `GameEngine` class methods (`init`, `execute`)
