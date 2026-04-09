# GeneralsMD/Code/Libraries/Source/WWVegas/WWAudio/AABTreeSoundCullClass.h

## Purpose
Defines a derived class for sound culling using Axis-Aligned Bounding Box (AABB) trees.

## Responsibilities
- Implements two required methods from AABTreeCullClass for sound culling
- Provides empty implementations for loading/saving node contents
- Serves as a base for sound-specific AABB tree operations

## Key Types
- AABTreeSoundCullClass (Class): Derived class for sound culling using AABB trees

## Key Functions
### AABTreeSoundCullClass()
- Purpose: Default constructor
- Calls: AABTreeCullClass constructor

### ~AABTreeSoundCullClass()
- Purpose: Destructor
- Calls: None

### Load()
- Purpose: Empty implementation for loading
- Calls: None

### Save()
- Purpose: Empty implementation for saving
- Calls: None

### Load_Node_Contents()
- Purpose: Empty implementation for loading node contents
- Calls: None

### Save_Node_Contents()
- Purpose: Empty implementation for saving node contents
- Calls: None

## Globals
- None

## Dependencies
- AABTreeCull.H (header)
- ChunkLoadClass, ChunkSaveClass (external classes)
