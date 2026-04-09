# Generals/Code/Tools/ParticleEditor/ParticleEditor.cpp

## Purpose
This file implements a DLL for a particle system editor tool, providing functions to manage particle systems and their templates in the game.

## Responsibilities
- Manages creation/destruction of the particle editor dialog
- Handles particle system and template operations (add/remove/update)
- Provides state queries for the editor (selection changes, reload requests, etc.)
- Coordinates with the main game engine via exported functions

## Key Types
- CDebugWindowApp (Class): Main application class for the editor DLL
- DebugWindowDialog (Class): The actual editor dialog window

## Key Functions
### CreateParticleSystemDialog
- Purpose: Creates and initializes the particle editor dialog window
- Calls: DebugWindowDialog constructor, InitPanel, ShowWindow

### DestroyParticleSystemDialog
- Purpose: Destroys the particle editor dialog window
- Calls: DebugWindowDialog::DestroyWindow

### NextParticleEditorBehavior
- Purpose: Determines the next action the editor should take based on current state
- Calls: HasUpdatedSelectedParticleSystem, ShouldWriteINI, HasRequestedReload, ShouldBusyWait, ShouldUpdateParticleCap, ShouldReloadTextures, HasRequestedKillAllSystems

### UpdateCurrentParticleSystem
- Purpose: Updates the currently selected particle system with new template data
- Calls: DebugWindowDialog::updateCurrentParticleSystem

## Globals
- theApp (CDebugWindowApp): The single instance of the application class

## Dependencies
- "ParticleEditor.h"
- "ParticleEditorDialog.h"
- MFC framework (CWinApp, CDialog, etc.)
- ParticleSystemTemplate (external type)
