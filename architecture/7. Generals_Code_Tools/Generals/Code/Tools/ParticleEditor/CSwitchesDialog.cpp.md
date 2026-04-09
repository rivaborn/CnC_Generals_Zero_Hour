# Generals/Code/Tools/ParticleEditor/CSwitchesDialog.cpp

## Purpose
Handles the UI dialog for particle system switches in the Particle Editor tool.

## Responsibilities
- Manages checkbox controls for particle system switches
- Synchronizes UI state with the particle system
- Notifies parent dialog of changes via `signalParticleSystemEdit()`

## Key Types
- `CSwitchesDialog` (Class): Dialog for particle system switch controls
- `DebugWindowDialog` (External): Parent dialog providing particle system access

## Key Functions
### `performUpdate(Bool toUI)`
- Purpose: Syncs UI and particle system switch states
- Calls: `GetDWDParent()`, `getSwitchFromSystem()`, `updateSwitchToSystem()`

### `OnParticleSystemEdit()`
- Purpose: Notifies parent of particle system edits
- Calls: `GetDWDParent()`, `signalParticleSystemEdit()`

## Globals
None

## Dependencies
- `StdAfx.h`, `Resource.h`, `CSwitchesDialog.h`, `ParticleEditorDialog.h`
- `CDialog`, `CButton`, `Bool` (MFC/Windows types)
- `DebugWindowDialog` methods: `getSwitchFromSystem()`, `updateSwitchToSystem()`, `signalParticleSystemEdit()`
