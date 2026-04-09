# Generals/Code/GameEngineDevice/Source/W3DDevice/GameClient/Shadow/W3DShadow.cpp

## Purpose
Manages real-time shadow rendering in the game, handling both volumetric and projected shadows.

## Responsibilities
- Initializes and manages shadow systems
- Adds/removes shadows for game objects
- Updates shadow positions based on light source
- Renders shadows during the scene rendering process

## Key Types
- W3DShadowManager (Class): Main shadow manager controlling volumetric and projected shadows
- Shadow (Class): Base class for shadow types (not defined here)
- RenderInfoClass (Class): Contains rendering context (external)

## Key Functions
### DoShadows
- Purpose: Renders shadows based on current render state
- Calls: TheW3DProjectedShadowManager->renderShadows, TheW3DVolumetricShadowManager->renderShadows, TheW3DShadowManager->isShadowScene, TheW3DShadowManager->queueShadows

### W3DShadowManager::init
- Purpose: Performs one-time initialization of shadow systems
- Calls: TheW3DVolumetricShadowManager->init, TheW3DProjectedShadowManager->init, ReAcquireResources

### W3DShadowManager::addShadow
- Purpose: Creates a new shadow for a game object
- Calls: TheW3DVolumetricShadowManager->addShadow, TheW3DProjectedShadowManager->addShadow

## Globals
- TheW3DShadowManager (W3DShadowManager*): Global shadow manager instance
- shadowCameraFrustum (const FrustumClass*): Pointer to current camera frustum
- LightPosWorld (Vector3[MAX_SHADOW_LIGHTS]): Stores world positions of light sources

## Dependencies
- WW3D2/Camera.h, WW3D2/Light.h, WW3D2/DX8Wrapper.h
- W3DDevice/GameClient/W3DVolumetricShadow.h, W3DDevice/GameClient/W3DProjectedShadow.h
- Common/GlobalData.h, D3dx8math.h
- Lib/BaseType.h, Common/Debug.h
