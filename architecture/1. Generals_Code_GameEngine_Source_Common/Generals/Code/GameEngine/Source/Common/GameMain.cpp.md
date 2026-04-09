# Generals/Code/GameEngine/Source/Common/GameMain.cpp

## Purpose
This file contains the main entry point for the Command & Conquer Generals game, initializing and running the game engine.

## Responsibilities
- Initializes the game engine.
- Executes the game loop.
- Cleans up resources upon exiting.

## Key Types
- None

## Key Functions
### GameMain
- Purpose: The main entry point for the game system.
- Calls:
  - CreateGameEngine()
  - init(argc, argv)
  - execute()

## Globals
- TheGameEngine (GameEngine*): Pointer to the game engine instance.

## Dependencies
- Includes:
  - "PreRTS.h"
  - "Common/GameEngine.h"
- External symbols used but not defined here:
  - CreateGameEngine()
