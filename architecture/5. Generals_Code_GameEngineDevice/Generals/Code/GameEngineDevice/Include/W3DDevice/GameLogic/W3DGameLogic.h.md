# Generals/Code/GameEngineDevice/Include/W3DDevice/GameLogic/W3DGameLogic.h

## Purpose
Defines the W3D-specific game logic class, extending base GameLogic with W3D engine integration.

## Responsibilities
- Provides W3D-specific game logic functionality
- Manages terrain logic creation
- Manages ghost object manager creation
- Acts as bridge between logical and visual terrain systems

## Key Types
- W3DGameLogic (Class): W3D-specific game logic implementation
- W3DGhostObjectManager (Class): Not inferable (forward declared)

## Key Functions
### createTerrainLogic
- Purpose: Factory method for creating W3DTerrainLogic instance
- Calls: NEW W3DTerrainLogic

### createGhostObjectManager
- Purpose: Factory method for creating W3DGhostObjectManager instance
- Calls: NEW W3DGhostObjectManager

## Globals
None

## Dependencies
- GameLogic.h (base class)
- W3DTerrainLogic.h (terrain logic)
- W3DGhostObject.h (ghost object definitions)
