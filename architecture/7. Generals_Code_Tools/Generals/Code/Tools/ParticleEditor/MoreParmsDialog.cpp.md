# Generals/Code/Tools/ParticleEditor/MoreParmsDialog.cpp

## Purpose
Handles the UI for advanced particle system parameters in the Particle Editor tool.

## Responsibilities
- Manages dialog controls for particle system parameters
- Synchronizes UI with particle system data
- Handles user input and updates the particle system accordingly
- Populates dropdown lists with available particle systems

## Key Types
- **MoreParmsDialog (class)**: Main dialog class for advanced particle parameters
- **ParticleSystemInfo::WindMotion (enum)**: Wind motion types for particles

## Key Functions
### MoreParmsDialog::InitPanel
- Purpose: Initializes the wind motion dropdown list
- Calls: None

### MoreParmsDialog::performUpdate
- Purpose: Synchronizes particle system data with UI controls
- Calls: Various `get*FromSystem` and `update*ToSystem` methods from parent

### MoreParmsDialog::OnParticleSystemEdit
- Purpose: Notifies parent when particle system parameters are edited
- Calls: `signalParticleSystemEdit()` on parent

## Globals
- **ARBITRARY_BUFF_SIZE (const int)**: Buffer size for text operations
- **WindMotionNames (const char**)**: Array of wind motion type names

## Dependencies
- `StdAfx.h`, `MoreParmsDialog.h`, `ParticleEditorDialog.h`
- `CDialog`, `CComboBox`, `CWnd` from MFC
- `DebugWindowDialog` (parent class)
- `ParticleSystemInfo` (for wind motion enum)
