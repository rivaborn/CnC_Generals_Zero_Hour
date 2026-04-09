# Generals/Code/Tools/ParticleEditor/ParticleTypePanels.cpp

## Purpose
Implements UI panels for editing particle system properties in the Particle Editor tool.

## Responsibilities
- Manages particle type selection UI (textures)
- Handles drawable object selection UI (thing templates)
- Synchronizes UI state with the particle system backend
- Provides message handling for combo box changes

## Key Types
- **ParticlePanelParticle (class)**: Panel for particle texture selection.
- **ParticlePanelDrawable (class)**: Panel for drawable object selection.
- **ParticlePanelStreak (class)**: Panel for streak particle selection (inherits from ParticlePanelParticle).

## Key Functions
### ParticlePanelParticle::InitPanel
- Purpose: Populates particle texture combo box from filesystem.
- Calls: `CFileFind::FindFile`, `CFileFind::FindNextFile`, `CComboBox::AddString`

### ParticlePanelParticle::performUpdate
- Purpose: Synchronizes particle name between UI and system.
- Calls: `DebugWindowDialog::getParticleNameFromSystem`, `DebugWindowDialog::updateParticleNameToSystem`

### ParticlePanelDrawable::performUpdate
- Purpose: Synchronizes drawable name between UI and system.
- Calls: `DebugWindowDialog::getDrawableNameFromSystem`, `DebugWindowDialog::updateDrawableNameToSystem`

### ParticlePanelDrawable::clearAllThingTemplates
- Purpose: Clears the thing template combo box.
- Calls: `CComboBox::Clear`

## Globals
- **PATH (const char*)**: Base texture path ("Art\\Textures\\").
- **PREFIX (const char*)**: Texture filename prefix ("EX").
- **POSTFIX (const char*)**: Texture filename wildcard ("*.*").

## Dependencies
- `StdAfx.h`, `ParticleTypePanels.h`, `ParticleEditorDialog.h`
- MFC classes: `CWnd`, `CComboBox`, `CFileFind`
- `DebugWindowDialog` class methods
- Windows API: `_tfinddata_t` (via `<direct.h>`)
