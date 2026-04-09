# Generals/Code/Tools/Autorun/leanAndMeanAutorun.h

## Purpose
Defines a header to exclude unnecessary code when building autorun tools without linking the full game engine.

## Responsibilities
- Prevents inclusion of game engine dependencies in autorun tools
- Defines `LEAN_AND_MEAN` macro to strip down functionality
- Provides minimal interface for autorun-specific code extraction

## Key Types
- None

## Key Functions
- None

## Globals
- None

## Dependencies
- None (header-only, no includes or external symbols)
