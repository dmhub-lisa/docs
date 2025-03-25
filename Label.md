---
title: Label
short_desc: Label type documentation
tags: api
path: lua_api/Label
uuid: 3f37660e-dc45-dd53-a561-51e519f7ee5e
public: true
private: false
---

 : [:Panel](/lua_api/Label)

### Properties

* **numeric** *boolean* (default=false) If set to true, this label is configured to accept only numeric input.
* **editable** *boolean* (default=false) If set to true, this label can be edited by clicking on it.
* **editableOnRightClick** *boolean* (default=false) If set to true, this label can be edited by right-clicking on it.
* **editableOnDoubleClick** *boolean* (default=false) If set to true, this label can be edited by double-clicking on it.
* **editing** *boolean* (read-only) True if the user is currently editing this label.
* **text** *string* The text displayed in this label.
* **markdown** *boolean* (default=false) If true, this label is formatted using markdown.
* **characterLimit** *number* The maximum number of characters this label can contain.
* **maxVisibleLines** *number* The maximum number of lines this label can display.
* **maxVisibleCharacters** *number* The maximum number of lines this label can display. Excess characters will still be stored, but won't be displayed. @see characterLimit to limit the length that text can be.
* **links** *boolean* If true, links can be displayed within this panel.
* **linkHovered** *nil|string* The id of the currently hovered link.

### Functions

function **Label:BeginEditing**()
Focus this label and begin editing it.
  return *nil*
