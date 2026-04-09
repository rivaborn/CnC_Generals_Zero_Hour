# Generals/Code/GameEngineDevice/Include/Win32Device/Common/Win32GameEngine.h

## Purpose
Defines the Win32-specific implementation of the game engine, creating device interfaces for Windows.

## Responsibilities
- Implements core game engine functionality for Win32
- Manages factory methods for game subsystems
- Handles Windows OS maintenance
- Initializes and updates the game engine

## Key Types
- **Win32GameEngine (Class)**: Win32 implementation of the game engine

## Key Functions
### Win32GameEngine::createGameLogic
- Purpose: Factory method for game logic creation
- Calls: NEW W3DGameLogic

### Win32GameEngine::createGameClient
- Purpose: Factory method for game client creation
- Calls: NEW W3DGameClient

### Win32GameEngine::createNetwork
- Purpose: Factory method for network interface creation
- Calls: NetworkInterface::createNetwork()

## Globals
- **m_previousErrorMode (UINT)**: Stores previous Windows error mode

## Dependencies
- GameEngine.h, GameLogic.h, NetworkInterface.h
- MilesAudioManager.h, Win32BIGFileSystem.h, Win32LocalFileSystem.h
- W3DModuleFactory.h, W3DGameLogic.h, W3DGameClient.h
- W3DWebBrowser.h, W3DFunctionLexicon.h, W3DRadar.h
- W3DThingFactory.h
