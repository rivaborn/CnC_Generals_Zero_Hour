# GeneralsMD/Code/GameEngineDevice/Source/W3DDevice/GameClient/W3DDisplayString.cpp

## Purpose
Implements W3DDisplayString class for rendering text in the game using W3D (Westwood 3D) engine.

## Responsibilities
- Manages text rendering with fonts, colors, and positioning
- Handles text changes, font changes, and hotkey display
- Computes text extents and handles word wrapping
- Maintains clipping regions for text rendering

## Key Types
- W3DDisplayString (Class): Main class for displaying text with W3D rendering
- FontCharsClass (Type): Font data structure used by the renderer

## Key Functions
### W3DDisplayString::draw
- Purpose: Renders text at specified position with given colors
- Calls: m_textRenderer.Build_Sentence, m_textRenderer.Draw_Sentence, m_textRenderer.Render

### W3DDisplayString::notifyTextChanged
- Purpose: Handles text change notifications and updates rendering state
- Calls: DisplayString::notifyTextChanged, m_textRenderer.Set_Use_Hard_Word_Wrap

### W3DDisplayString::setFont
- Purpose: Sets the font for text rendering
- Calls: DisplayString::setFont, m_textRenderer.Set_Font, computeExtents

### W3DDisplayString::computeExtents
- Purpose: Calculates text dimensions based on current font and text
- Calls: m_textRenderer.Get_Formatted_Text_Extents

### W3DDisplayString::setWordWrap
- Purpose: Configures word wrapping behavior
- Calls: m_textRenderer.Set_Wrapping_Width, notifyTextChanged

## Globals
- None

## Dependencies
- GameClient/GameClient.h
- W3DDevice/GameClient/W3DDisplayString.h
- GameClient/HotKey.h
- GameClient/GameFont.h
- GameClient/GlobalLanguage.h
