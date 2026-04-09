# Generals/Code/Tools/ParticleEditor/ISwapablePanel.h

## Purpose
Defines an interface for swapable panels in the Particle Editor tool, allowing derived classes to implement update and initialization logic.

## Responsibilities
- Declares the `ISwapablePanel` interface for panel management.
- Requires implementation of panel ID, update, and initialization methods.
- Inherits from `CDialog` for UI integration.
- Provides a default constructor.

## Key Types
- ISwapablePanel (interface): Base interface for panels that need dynamic updates and initialization.

## Key Functions
### ISwapablePanel::GetIDD
- Purpose: Returns the panel's dialog resource ID.
- Calls: None.

### ISwapablePanel::performUpdate
- Purpose: Updates the panel's state (to/from UI).
- Calls: None.

### ISwapablePanel::InitPanel
- Purpose: Initializes the panel.
- Calls: None.

## Globals
- None.

## Dependencies
- `CDialog` (from MFC): Base class for dialog-derived panels.
- `Bool` (from `Lib/BaseType.h`): Boolean type used in `performUpdate`.
