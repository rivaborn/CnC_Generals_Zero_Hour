# Generals/Code/Libraries/Source/WWVegas/WW3D2/ww3dids.h

## Purpose
Defines chunk IDs for persistent WW3D objects used in save/load functionality.

## Responsibilities
- Declares enum values for render objects, lights, and dazzle effects.
- Provides IDs for the WWSaveLoad library's persist framework.
- Supports serialization of game state for save games.

## Key Types
- (anonymous enum) (Enum): Contains WW3D persistent chunk IDs.
- WW3D_PERSIST_CHUNKID_RENDEROBJ (Enum): ID for render object persistence.
- WW3D_PERSIST_CHUNKID_LIGHT (Enum): ID for light persistence.
- WW3D_PERSIST_CHUNKID_DAZZLE (Enum): ID for dazzle effect persistence.

## Key Functions
None.

## Globals
None.

## Dependencies
- `saveloadids.h`: For base CHUNKID_WW3D_BEGIN definition.
