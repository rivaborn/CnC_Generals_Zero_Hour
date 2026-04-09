# GeneralsMD/Code/GameEngineDevice/Source/W3DDevice/GameClient/Shadow/W3DShadow.cpp

## Purpose
Manages real-time shadow rendering in the game, including projected and volumetric shadows.

## Responsibilities
- Initializes and manages shadow systems
- Handles shadow creation, removal, and updates
- Coordinates between projected and volumetric shadow managers
- Updates light positions for shadows based on time of day

## Key Types
- W3DShadowManager (Class): Main shadow management class
- Shadow (Class): Base shadow type (defined elsewhere)
- RenderInfoClass (Class): Rendering context (defined elsewhere)

## Key Functions
### DoShadows
- Purpose: Renders shadows based on current render state
- Calls: TheW3DProjectedShadowManager->renderShadows, TheW3DVolumetricShadowManager->renderShadows, TheW3DShadowManager->isShadowScene, TheW3DShadowManager->queueShadows

### W3DShadowManager::init
- Purpose: Initializes shadow systems
- Calls: TheW3DVolumetricShadowManager->init, TheW3DProjectedShadowManager->init, TheW3DVolumetricShadowManager->ReAcquireResources, TheW3DProjectedShadowManager->ReAcquireResources

### W3DShadowManager::addShadow
- Purpose: Adds a shadow to the appropriate manager based on type
- Calls: TheW3DVolumetricShadowManager->addShadow, TheW3DProjectedShadowManager->addShadow

## Globals
- TheW3DShadowManager (W3DShadowManager*): Global shadow manager instance
- shadowCameraFrustum (const FrustumClass*): Current shadow camera frustum
- LightPosWorld (Vector3[MAX_SHADOW_LIGHTS]): World positions of shadow lights

## Dependencies
- "GameClient/View.h", "WW3D2/Camera.h", "WW3D2/Light.h", "WW3D2/DX8Wrapper.h", "WW3D2/HLod.h", "WW3D2/mesh.h", "WW3D2/meshmdl.h", "Lib/BaseType.h", "W3DDevice/GameClient/W3DGranny.h", "W3DDevice/GameClient/Heightmap.h", "D3dx8math.h", "common/GlobalData.h", "W3DDevice/GameClient/W3DVolumetricShadow.h", "W3DDevice/GameClient/W3DProjectedShadow.h", "W3DDevice/GameClient/W3DShadow.h", "WW3D2/statistics.h", "Common/Debug.h", "Common/PerfTimer.h"
