# GeneralsMD/Code/GameEngineDevice/Source/W3DDevice/GameClient/W3DAssetManagerExposed.cpp

## Purpose
Exposes asset management functionality for the W3D rendering system, specifically texture reloading.

## Responsibilities
- Provides external interface for texture management
- Delegates operations to W3DAssetManager singleton
- Handles texture resource reloading

## Key Types
- None

## Key Functions
### ReloadAllTextures
- Purpose: Reloads all textures in the game
- Calls: W3DAssetManager::Get_Instance()->Release_All_Textures()

## Globals
- None

## Dependencies
- W3DDevice/GameClient/W3DAssetManagerExposed.h
- W3DDevice/GameClient/W3DAssetManager.h
- W3DAssetManager singleton class
