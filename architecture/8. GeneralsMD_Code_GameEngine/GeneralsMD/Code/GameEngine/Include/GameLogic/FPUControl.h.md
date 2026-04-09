# GeneralsMD/Code/GameEngine/Include/GameLogic/FPUControl.h

## Purpose
Header file declaring FPU state control routines for the game engine.

## Responsibilities
- Declares FPU control interface
- Documents FPU state management requirements
- Provides DirectX FPU state recovery mechanism

## Key Types
- None

## Key Functions
### setFPMode
- Purpose: Sets FPU precision and rounding mode to ensure DirectX doesn't corrupt FPU state
- Calls: Not inferable (implementation in separate file)

## Globals
- None

## Dependencies
- None (pure header file)
- Assumes DirectX usage elsewhere in codebase
