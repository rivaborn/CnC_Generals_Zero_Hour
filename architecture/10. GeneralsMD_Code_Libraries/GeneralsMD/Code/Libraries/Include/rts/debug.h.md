# GeneralsMD/Code/Libraries/Include/rts/debug.h

## Purpose
Proxy header file that includes the actual debug module header.

## Responsibilities
- Provides a proxy include for debug functionality
- Maintains include guard to prevent multiple inclusions
- Includes the real debug header from the source directory

## Key Types
None

## Key Functions
None

## Globals
None

## Dependencies
- `"../../source/debug/debug.h"`: The actual debug module header
- `_MSC_VER`: Microsoft Visual C++ version macro for pragma once
