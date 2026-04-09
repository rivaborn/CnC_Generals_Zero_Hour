# GeneralsMD/Code/GameEngineDevice/Include/W3DDevice/GameClient/Module/W3DTruckDraw.h

## Purpose
Defines classes for rendering truck-like vehicles in the game, including wheel rotation, particle effects, and segmented body parts.

## Responsibilities
- Manage truck-specific visual effects (dust, dirt, powerslide)
- Handle wheel and segmented body (cab/trailer) animations
- Control particle emitters based on movement state
- Integrate with the W3D rendering system

## Key Types
- **W3DTruckDrawModuleData (Class)**: Stores configuration data for truck visuals (effect names, bone names, rotation factors)
- **W3DTruckDraw (Class)**: Main truck rendering module handling drawing, animations, and effects
- **W3DTruckDrawMagicEnum (Enum)**: Not inferable (likely internal macro enum)
- **W3DTruckDraw_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable (likely internal macro enum)

## Key Functions
### W3DTruckDrawModuleData::buildFieldParse
- Purpose: Parse configuration fields for truck module data
- Calls: Not inferable

### W3DTruckDraw::setHidden
- Purpose: Show/hide the truck model
- Calls: Not inferable

### W3DTruckDraw::doDrawModule
- Purpose: Render the truck with current transformations
- Calls: Not inferable

### W3DTruckDraw::onRenderObjRecreated
- Purpose: Handle recreation of render object (e.g., after level load)
- Calls: Not inferable

### W3DTruckDraw::createEmitters
- Purpose: Initialize particle effects for the truck
- Calls: Not inferable

### W3DTruckDraw::enableEmitters
- Purpose: Enable/disable particle emitters based on movement
- Calls:
