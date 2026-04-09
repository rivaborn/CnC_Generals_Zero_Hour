# Generals/Code/Tools/WorldBuilder/src/ContourOptions.cpp

## Purpose
Handles the UI dialog for contour options in WorldBuilder, managing slider controls for step, offset, and width settings.

## Responsibilities
- Manages slider controls for contour step, offset, and width
- Updates contour settings in the active view
- Toggles contour visibility
- Initializes dialog UI with current settings

## Key Types
- `ContourOptions` (Class): Dialog for contour settings
- `m_contourStepSlider`/`m_contourOffsetSlider`/`m_contourWidthSlider` (CSliderCtrl): Slider controls for contour parameters
- `m_updating` (Bool): Flag to prevent recursive updates

## Key Functions
### `OnInitDialog`
- Purpose: Initializes slider controls and sets initial values
- Calls: `CDialog::OnInitDialog`, `CWnd::GetWindowRect`, `CSliderCtrl::Create`, `CSliderCtrl::SetRange`, `CSliderCtrl::SetTicFreq`, `CSliderCtrl::SetPos`, `CSliderCtrl::ShowWindow`, `CButton::SetCheck`, `CWorldBuilderDoc::GetActive2DView`

### `OnHScroll`
- Purpose: Handles slider value changes and updates settings
- Calls: `CSliderCtrl::GetPos`, `CWorldBuilderDoc::GetActive2DView`, `CWorldBuilderView::setCellSize`

### `OnShowContours`
- Purpose: Toggles contour visibility in the active view
- Calls: `CWorldBuilderDoc::GetActive2DView`, `CButton::SetCheck`, `CWorldBuilderView::setShowContours`

## Globals
- `m_contourStep` (Int): Current contour step value
- `m_contourOffset` (Int): Current contour offset value
- `m_contourWidth
