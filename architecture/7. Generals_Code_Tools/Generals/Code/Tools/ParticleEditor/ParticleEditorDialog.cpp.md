# Generals/Code/Tools/ParticleEditor/ParticleEditorDialog.cpp

## Purpose
This file implements the `DebugWindowDialog` class, which provides a UI for editing particle systems in the game.

## Responsibilities
- Manages particle system editing UI panels
- Handles user input for particle system parameters
- Coordinates updates between UI and particle system data
- Manages sub-dialogs for color, switches, and additional parameters

## Key Types
- `DebugWindowDialog` (Class): Main dialog class for particle system editing
- `EmissionPanelPoint`, `EmissionPanelLine`, etc. (Classes): Specific emission type panels
- `VelocityPanelOrtho`, `VelocityPanelSphere`, etc. (Classes): Specific velocity type panels
- `ParticlePanelParticle`, `ParticlePanelDrawable`, etc. (Classes): Specific particle type panels

## Key Functions
### `InitPanel`
- Purpose: Initializes all UI panels and combo boxes
- Calls: `Create`, `InitPanel` on sub-dialogs and panels

### `performUpdate`
- Purpose: Synchronizes particle system data with UI controls
- Calls: `performUpdate` on sub-dialogs and panels

### `OnParticleSystemEdit`
- Purpose: Handles particle system parameter edits
- Calls: `signalParticleSystemEdit`

### `shouldWriteINI`
- Purpose: Checks if particle system should be saved
- Calls: None

## Globals
- `mMainWndHWND` (HWND): Handle to main game window
- `m_particleSystem` (ParticleSystem*): Current particle system being edited
- `m_changeHasOcurred` (Bool): Flag for UI changes
- `m_listOfParticleSystems` (std::list<std::string>): List of available particle systems

## Dependencies
- `CParticleEditorPage.h`
- `EmissionTypePanels.h`
- `GameClient/ParticleSys.h`
- `ParticleEditorExport.h`
- `ParticleTypePanels.h`
- `VelocityTypePanels.h`
- MFC classes (`CDialog`, `CComboBox`, etc.)
