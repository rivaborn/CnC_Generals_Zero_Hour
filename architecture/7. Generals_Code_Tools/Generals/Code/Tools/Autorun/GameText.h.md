# Generals/Code/Tools/Autorun/GameText.h

## Purpose
Defines the interface for localized game text management.

## Responsibilities
- Declares the `GameTextInterface` abstract class for text localization
- Provides factory function to create the text interface
- Exposes global singleton instance for text access

## Key Types
- **GameTextInterface (Class)**: Abstract base class for localized text retrieval

## Key Functions
### CreateGameTextInterface
- Purpose: Factory function to create the text interface instance
- Calls: Not inferable

## Globals
- **TheGameText (GameTextInterface*)**: Global singleton instance for text access

## Dependencies
- None explicitly included (header-only interface)
