# Generals/Code/Tools/WorldBuilder/src/ScriptProperties.cpp

## Purpose
Handles the UI and logic for editing script properties in the WorldBuilder tool.

## Responsibilities
- Manages script property page UI (name, comment, active status, etc.)
- Syncs UI controls with script object state
- Handles user input for script configuration
- Updates script object when properties change

## Key Types
- ScriptProperties (CPropertyPage): Property page for script editing
- Script (Not inferable): Script object being edited

## Key Functions
### OnSetActive
- Purpose: Initializes UI controls with script data when page becomes active
- Calls: CPropertyPage::OnSetActive, m_script->getComment, m_script->getName, enableControls

### enableControls
- Purpose: Updates UI controls to reflect script state
- Calls: m_script->isSubroutine, m_script->isActive, m_script->isOneShot, m_script->isEasy, m_script->isNormal, m_script->isHard, m_script->getDelayEvalSeconds

### OnChangeScriptComment/OnChangeScriptName/OnScriptActive/OnOneShot/OnEasy/OnHard/OnNormal/OnScriptSubroutine
- Purpose: Handler for each property change, updates script object
- Calls: m_script->setComment/setName/setActive/setOneShot/setEasy/setNormal/setSubroutine

### OnEveryFrame/OnEverySecond/OnChangeSecondsEdit
- Purpose: Handles delay evaluation timing controls
- Calls: m_script->setDelayEvalSeconds

## Globals
- None

## Dependencies
- "stdafx.h", "worldbuilder.h", "ScriptProperties.h", "GameLogic/Scripts.h"
- CPropertyPage, CButton, CWnd, CString, AsciiString, Bool, Int
- MFC message map macros (BEGIN_MESSAGE_MAP, ON_EN_CHANGE, ON_BN_CLICKED)
