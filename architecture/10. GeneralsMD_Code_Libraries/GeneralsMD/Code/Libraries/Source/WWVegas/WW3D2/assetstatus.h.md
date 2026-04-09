# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/assetstatus.h

## Purpose
Manages reporting of asset loading status and missing assets in the W3D engine.

## Responsibilities
- Tracks load-on-demand and missing assets (RObj, HAnim, HTree).
- Provides singleton access via `Peek_Instance()`.
- Stores reports in hash tables for each asset type.
- Enables/disables reporting globally.

## Key Types
- **AssetStatusClass (Class)**: Singleton manager for asset status reporting.
- **(anonymous enum) (Enum)**: Defines report types (load-on-demand/missing for RObj/HAnim/HTree).
- **REPORT_LOAD_ON_DEMAND_ROBJ (Enum)**: Report type for load-on-demand RObj.
- **REPORT_LOAD_ON_DEMAND_HANIM (Enum)**: Report type for load-on-demand HAnim.
- **REPORT_LOAD_ON_DEMAND_HTREE (Enum)**: Report type for load-on-demand HTree.
- **REPORT_MISSING_ROBJ (Enum)**: Report type for missing RObj.
- **REPORT_MISSING_HANIM (Enum)**: Report type for missing HAnim.
- **REPORT_MISSING_HTREE (Enum)**: Report type for missing HTree.
- **REPORT_COUNT (Enum)**: Total number of report types.

## Key Functions
### `Enable_Reporting`
- Purpose: Enables/disables all reporting.
- Calls: None.

### `Enable_Load_On_Demand_Reporting`
- Purpose: Enables/disables load-on-demand reporting.
- Calls: None.

### `Report_Load_On_Demand_RObj`
- Purpose: Reports a load-on-demand RObj asset.
- Calls: `Add_To_Report`.

### `Report_Load_On_Demand_HAnim`
- Purpose: Reports a load-on-demand H
