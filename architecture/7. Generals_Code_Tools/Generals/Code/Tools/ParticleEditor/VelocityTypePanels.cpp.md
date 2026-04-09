# Generals/Code/Tools/ParticleEditor/VelocityTypePanels.cpp

## Purpose
Implements UI panels for editing different particle velocity types in the Particle Editor tool.

## Responsibilities
- Manages orthogonal, spherical, hemispherical, cylindrical, and outward velocity parameter panels
- Synchronizes UI controls with particle system data
- Handles user input and updates particle system parameters accordingly
- Provides message handling for UI events

## Key Types
- VelocityPanelOrtho (Class): Handles orthogonal velocity parameters (X/Y/Z min/max)
- VelocityPanelSphere (Class): Manages spherical velocity parameters (radial min/max)
- VelocityPanelHemisphere (Class): Controls hemispherical velocity parameters (radial min/max)
- VelocityPanelCylinder (Class): Manages cylindrical velocity parameters (radial/normal min/max)
- VelocityPanelOutward (Class): Handles outward velocity parameters (speed/other min/max)

## Key Functions
### performUpdate
- Purpose: Synchronizes UI controls with particle system data or vice versa
- Calls: getVel*FromSystem, updateVel*ToSystem, sprintf, atof

### OnParticleSystemEdit
- Purpose: Notifies parent dialog about particle system edits
- Calls: signalParticleSystemEdit

## Globals
- None

## Dependencies
- VelocityTypePanels.h
- ParticleEditorDialog.h
- ISwapablePanel base class
- DebugWindowDialog parent class
- MFC framework (CWnd, BEGIN_MESSAGE_MAP, etc.)
