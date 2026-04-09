# Generals/Code/Libraries/Source/WWVegas/WW3D2/robjlist.h

## Purpose
Defines render object list types for the SAGE engine's rendering system.

## Responsibilities
- Declares reference-counted and non-reference-counted render object list classes
- Provides iterator types for traversing render object lists
- Serves as a header for render object management

## Key Types
- RenderObjClass (Class): Base class for renderable objects
- RefRenderObjListClass (Class): Reference-counted render object list
- RefRenderObjListIterator (Class): Iterator for reference-counted lists
- NonRefRenderObjListClass (Class): Non-reference-counted render object list
- NonRefRenderObjListIterator (Class): Iterator for non-reference-counted lists

## Key Functions
None

## Globals
None

## Dependencies
- always.h
- multilist.h
- wwdebug.h
- RefMultiListClass<RenderObjClass>
- RefMultiListIterator<RenderObjClass>
- MultiListClass<RenderObjClass>
- MultiListIterator<RenderObjClass>
