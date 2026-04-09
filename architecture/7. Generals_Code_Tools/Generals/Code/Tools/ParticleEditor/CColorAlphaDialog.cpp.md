# Generals/Code/Tools/ParticleEditor/CColorAlphaDialog.cpp

## Purpose
Handles color and alpha keyframe editing for particle systems in the Particle Editor tool.

## Responsibilities
- Manages color and alpha keyframe UI controls
- Synchronizes UI with particle system data
- Handles color picker dialogs and custom color persistence
- Updates parent dialog when particle system edits occur

## Key Types
- CColorAlphaDialog (Class): Main dialog class for color/alpha editing
- CButtonShowColor (Class): Custom color button control
- RGBColorKeyframe (Struct): Holds color and frame data
- ParticleSystemInfo::RandomKeyframe (Struct): Holds alpha range and frame data

## Key Functions
### CColorAlphaDialog::InitPanel
- Purpose: Loads custom colors from application settings
- Calls: AfxGetApp()->GetProfileString

### CColorAlphaDialog::performUpdate
- Purpose: Synchronizes UI with particle system data or vice versa
- Calls: GetParent(), getColorValueFromSystem, updateColorValueToSystem, getAlphaRangeFromSystem, updateAlphaRangeToSystem

### CColorAlphaDialog::onColorPress
- Purpose: Handles color button clicks and shows color picker
- Calls: CColorDialog constructor, DoModal, setColor, AfxGetApp()->WriteProfileString, OnParticleSystemEdit

### CColorAlphaDialog::OnParticleSystemEdit
- Purpose: Notifies parent dialog of particle system edits
- Calls: GetParent()->signalParticleSystemEdit

## Globals
- colorControls (const UINT[8][2]): Maps color button IDs to frame control IDs
- alphaControls (const UINT[8][3]): Maps alpha min/max/frame control IDs
- m_customColors (COLORREF[16]): Stores custom colors for color picker

## Dependencies
- StdAfx.h, Resource.h, CColorAlphaDialog.h
- GameClient/ParticleSys.h
- CParticleEditorPage.h, EmissionTypePanels.h, ParticleEditorDialog.h, ParticleEditorExport.h, ParticleTypePanels.h, VelocityTypePanels.h
- MFC classes (CDialog, CWnd, CButton, CColorDialog)
- DebugWindowDialog (parent class)
