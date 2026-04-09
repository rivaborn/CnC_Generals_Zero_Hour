# Generals/Code/Tools/WW3D/max2w3d/bpick.h - Enhanced Analysis

## Architectural Role
This file defines the bone picking infrastructure for the W3D export pipeline, bridging 3DS Max's scene graph with the W3D asset pipeline. It enables artists to select skeletal hierarchy nodes during model preparation, critical for animation rigging and export validation.

## Cross-References
### Incoming
- **max2w3d.cpp**: Likely uses `TheBonePicker` singleton for bone selection during W3D export
- **Other Max plugin tools**: Any tool requiring bone selection would reference this interface

### Outgoing
- **Max SDK (Max.h)**: Inherits from Max's picking callback interfaces
- **W3D export pipeline**: Passes selected bones to asset processing tools

## Design Patterns
- **Callback Pattern**: Uses Max's callback system for viewport interaction
- **Strategy Pattern**: `BonePickerUserClass` abstracts the consumer of bone picks
- **Singleton**: `TheBonePicker` provides global access to the picker instance

*Not inferable*: No clear use of Observer or Factory patterns in this header.
