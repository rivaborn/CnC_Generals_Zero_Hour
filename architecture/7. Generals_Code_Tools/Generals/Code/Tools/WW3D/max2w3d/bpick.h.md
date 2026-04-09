# Generals/Code/Tools/WW3D/max2w3d/bpick.h

## Purpose
Defines classes for bone picking functionality in 3DS Max plugin for W3D export.

## Responsibilities
- Provides interface for bone selection callbacks
- Implements bone picking mode for Max viewport
- Manages bone filtering and selection logic
- Handles dialog-based bone selection by name

## Key Types
- **BonePickerUserClass (Class)**: Abstract base for bone pick event handlers
- **BonePickerClass (Class)**: Main bone picker implementation with Max callbacks
- **None**: No enums/structs defined

## Key Functions
### BonePickerClass::Filter
- Purpose: Filter nodes for bone picking
- Calls: None

### BonePickerClass::HitTest
- Purpose: Handle hit testing during bone picking
- Calls: None

### BonePickerClass::Pick
- Purpose: Process bone selection
- Calls: None

### BonePickerClass::proc
- Purpose: Process selected bones via callback
- Calls: User_Picked_Bones

## Globals
- **TheBonePicker (BonePickerClass)**: Singleton instance for global access

## Dependencies
- Max.h (3DS Max SDK)
- INode, INodeTab, IObjParam, ViewExp (Max types)
- PickNodeCallback, PickModeCallback, HitByNameDlgCallback (Max callback interfaces)
