# Generals/Code/Tools/WW3D/max2w3d/SkinCopy.cpp

## Purpose
Handles skinning operations in 3DS Max for W3D export, including copying skin bindings and duplicating WWSkin WSM objects.

## Responsibilities
- Finds and manipulates WWSkin Binding modifiers
- Duplicates WWSkin WSM objects with bone remapping
- Copies skin information between objects
- Provides MAXScript interface for skin operations

## Key Types
- **SkinModifierClass**: WWSkin Binding modifier class
- **SkinWSMObjectClass**: WWSkin WSM object class
- **ModContext**: Modifier context data structure

## Key Functions
### find_skin_binding
- Purpose: Locates the WWSkin Binding modifier on a node
- Calls: GetWSMDerivedObject, GetModifier, ClassID

### find_skin_wsm
- Purpose: Finds the WWSkin WSM node referenced by a skinned object
- Calls: find_skin_binding, GetReference

### duplicate_wsm
- Purpose: Creates a copy of a WWSkin WSM with remapped bones
- Calls: get_skin_wsm_obj, CreateInstance, find_equivalent_node

### copy_skin_info
- Purpose: Copies skin binding from source to target object
- Calls: find_skin_binding, setup_wsm_derived_obj, find_skin_mod_context

## Globals
- **def_visible_primitive** (3 instances): MAXScript function declarations

## Dependencies
- MAXScript API (MaxScrpt.h, MaxObj.h)
- 3DS Max SDK (Max.h, modstack.h)
- Project-specific headers (skin.h, util.h, w3d_file.h)
