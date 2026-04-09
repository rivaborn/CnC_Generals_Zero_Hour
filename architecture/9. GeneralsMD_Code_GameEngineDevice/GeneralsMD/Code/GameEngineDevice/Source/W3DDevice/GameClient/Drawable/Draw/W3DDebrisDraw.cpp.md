# GeneralsMD/Code/GameEngineDevice/Source/W3DDevice/GameClient/Drawable/Draw/W3DDebrisDraw.cpp

## Purpose
Handles rendering and animation of debris objects in the W3D engine.

## Responsibilities
- Manages debris model rendering and animations
- Handles state transitions (initial, flying, final)
- Controls shadows and shroud visibility
- Processes transform changes
- Serializes/deserializes debris state

## Key Types
- W3DDebrisDraw (Class): Main debris rendering module
- RenderObjClass (External): Base render object class
- HAnimClass (External): Animation class
- Shadow (External): Shadow management interface

## Key Functions
### isAnimationComplete
- Purpose: Checks if an animation is complete for a render object
- Calls: HLodClass::Is_Animation_Complete()

### isNearlyZero
- Purpose: Determines if a velocity vector is nearly zero
- Calls: fabs()

### setModelName
- Purpose: Sets the debris model and creates render object
- Calls: W3DAssetManager::Create_Render_Obj(), W3DScene::Add_Render_Object(), W3DShadowManager::addShadow()

### setAnimNames
- Purpose: Configures animation sequences for debris states
- Calls: W3DAssetManager::Get_HAnim()

### doDrawModule
- Purpose: Renders debris with current state and animations
- Calls: RenderObjClass::Set_Animation(), FXList::doFXPos(), isAnimationComplete()

### xfer
- Purpose: Serializes/deserializes debris state
- Calls: DrawModule::xfer(), setModelName(), setAnimNames()

## Globals
- None

## Dependencies
- Common/FileSystem.h, Common/GlobalData.h, Common/ThingTemplate.h, Common/Xfer.h
- GameClient/Drawable.h, GameLogic/Object.h, GameClient/Shadow.h, GameClient/FXList.h
- GameLogic/TerrainLogic.h
- WW3D2/HAnim.h, WW3D2/HLod.h, WW3D2/RendObj.h
- W3DDevice/GameClient/Module/W3DDebrisDraw.h, W3DDevice/GameClient/W3DAssetManager.h
- W3DDevice/GameClient/W3DDisplay.h, W3DDevice/GameClient/W3DScene.h, W3DDevice/GameClient/W3DShadow.h
