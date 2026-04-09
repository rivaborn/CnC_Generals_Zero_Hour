# Generals/Code/Libraries/Source/WWVegas/WWSaveLoad/simpleparameter.h

## Purpose
Defines parameter classes for game configuration and serialization, including simple and ranged parameter types.

## Responsibilities
- Provides templated `SimpleParameterClass` for basic parameter types
- Implements ranged parameter constraints via `RangedParameterClass`
- Defines specialized parameter classes for common types (bool, vectors, matrices, etc.)
- Supports value comparison, retrieval, and modification
- Manages parameter type identification and value copying

## Key Types
- **SimpleParameterClass<T, type> (Class)**: Base template for simple parameter types with value storage and access
- **RangedParameterClass<T, type> (Class)**: Extends `SimpleParameterClass` to enforce min/max value constraints
- **BoolParameterClass (Class)**: Typed parameter for boolean values
- **Vector2ParameterClass (Class)**: Typed parameter for 2D vectors
- **Vector3ParameterClass (Class)**: Typed parameter for 3D vectors
- **Matrix3DParameterClass (Class)**: Typed parameter for 3D matrices
- **RectParameterClass (Class)**: Typed parameter for rectangles
- **ColorParameterClass (Class)**: Typed parameter for color values (Vector3)
- **StringsDBEntryParameterClass (Class)**: Typed parameter for string database entries
- **IntParameterClass (Class)**: Integer parameter with default range [-1e9, 1e9]
- **FloatParameterClass (Class)**: Float parameter with default range [-1e5, 1e5]
- **AngleParameterClass (Class)**: Float parameter for angles with range [0, 2Ï]

## Key Functions
### SimpleParameterClass::operator==
- Purpose: Compares parameter values for equality
- Calls: `Get_Type()`, `SimpleParameterClass::m_Data` access

### SimpleParameterClass::Get_Value
- Purpose: Retrieves the stored parameter value
- Calls: None

### SimpleParameterClass::Set_Value
- Purpose: Updates the stored parameter value and marks as modified
- Calls: `Set_Modified()`

### SimpleParameterClass::Copy_Value
- Purpose: Copies parameter value from another parameter
- Calls: `Get_Type()`, `ParameterClass::Copy_Value()`

### RangedParameterClass::Set_Range
- Purpose: Sets minimum and maximum allowed values
- Calls: None

## Globals
None

## Dependencies
- `parameter.h` (base `ParameterClass`)
- `vector2.h`, `vector3.h`, `matrix3d.h`, `rect.h` (math types)
- `always.h` (utility macros)
- `<float.h>` (float constants)
