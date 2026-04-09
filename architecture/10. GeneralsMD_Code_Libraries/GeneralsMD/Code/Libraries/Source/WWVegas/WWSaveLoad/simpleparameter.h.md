# GeneralsMD/Code/Libraries/Source/WWVegas/WWSaveLoad/simpleparameter.h

## Purpose
Defines parameter classes for game configuration and serialization, including simple and ranged parameter types.

## Responsibilities
- Provides templated `SimpleParameterClass` for basic parameter types
- Implements ranged parameter variants for numeric types
- Defines type-specific parameter classes (bool, vector, matrix, etc.)
- Supports value comparison and modification tracking

## Key Types
- **SimpleParameterClass<T, type> (Class)**: Base template for simple parameters with value storage
- **RangedParameterClass<T, type> (Class)**: Extends `SimpleParameterClass` with min/max range support
- **BoolParameterClass (Class)**: Boolean parameter type
- **Vector2ParameterClass (Class)**: 2D vector parameter
- **Vector3ParameterClass (Class)**: 3D vector parameter
- **Matrix3DParameterClass (Class)**: 3D matrix parameter
- **RectParameterClass (Class)**: Rectangle parameter
- **ColorParameterClass (Class)**: Color parameter (Vector3)
- **StringsDBEntryParameterClass (Class)**: Strings database ID parameter
- **IntParameterClass (Class)**: Integer parameter with default range
- **FloatParameterClass (Class)**: Float parameter with default range
- **AngleParameterClass (Class)**: Angle parameter (0-2Ï radians)

## Key Functions
### SimpleParameterClass::operator==
- Purpose: Compares parameter values for equality
- Calls: `Get_Type()`, `SimpleParameterClass::m_Data` access

### SimpleParameterClass::Get_Value
- Purpose: Returns the stored parameter value
- Calls: `SimpleParameterClass::m_Data` access

### SimpleParameterClass::Set_Value
- Purpose: Updates the parameter value and marks as modified
- Calls: `Set_Modified()`

### SimpleParameterClass::Copy_Value
- Purpose: Copies parameter value from another parameter
- Calls: `Get_Type()`, `ParameterClass::Copy_Value()`

### RangedParameterClass::Set_Range
- Purpose: Sets minimum and maximum values for the parameter
- Calls: None

### IntParameterClass::IntParameterClass
- Purpose: Constructs integer parameter with default range
- Calls: `RangedParameterClass::Set_Range()`

### FloatParameterClass::FloatParameterClass
- Purpose: Constructs float parameter with default range
- Calls: `RangedParameterClass::Set_Range()`

### AngleParameterClass::AngleParameterClass
- Purpose: Constructs angle parameter with 0-2Ï range
- Calls: `RangedParameterClass::Set_Range()`

## Globals
None

## Dependencies
- `parameter.h` (ParameterClass base)
- `vector2.h` (Vector2)
- `vector3.h` (Vector3
