---
title: Input
short_desc: Input type documentation
tags: api
path: lua_api/Input
uuid: f8b4ec36-9166-ce53-b44c-21982ba4abe2
public: true
private: false
---

 : [:Panel](/lua_api/Input)

### Properties

* **text** *string* The text held in this input.
* **textNoNotify** *string* An alias of @see text, but if set, no events will fire on the panel, such as the change event which normally fires when the text is changed.
* **editlag** *number* When the text is edited, the lag before calling the 'edit' event, all keypresses during this time will be coalesced into one. Use this to make it so a user typing very fast doesn't cause an excessive number of edit events.
* **placeholderText** *string* The grayed text to display when the input field is empty.
* **editable** *boolean* (default=true) If the input is editable by the user.
* **multiline** *boolean* (default=false) If the input displays multiple lines.
* **lineType** *"SingleLine"|"MultiLineSubmit"|"MultiLineNewLine"* When this is SingleLine, the input is a single line. Pressing enter will fire the 'submit' event. When MultiLineSubmit, the input is multiple lines but pressing enter will still fire 'submit'. The user can press shift+enter to enter a new line. MultiLineNewLine will be multiple lines. Pressing enter will create a new line, rather than firing submit.
* **characterLimit** *number* The maximum number of characters this input can contain.
* **hasInputFocus** *boolean* True if this input has the input focus.
* **selectAllOnFocus** *boolean* If set to true, the text will be selected when the input clicks on the input. This is useful to turn on for inputs the user is very likely to want to change in their entirety.
* **caretPosition** *number* The position of the cursor within the input.
* **selectionAnchorPosition** *number* The bounds of the selection. The @caretPosition is the opposite bounds of the selection. If this is equal to @see caretPosition the user has no text selected.
* **password** *boolean* If set to true, this input will not display the text that is being typed on-screen to keep it secret and safe.
* **restoreOriginalTextOnEscape** *boolean* If set to true, all edits will be canceled, and the text will be restored if the user presses escape while editing.
* **blockChangesWhenEditing** *boolean* If set to true, setting @see text in code will fail if the user is editing the text.
* **placeholderAlpha** *number* The alpha value of placeholder text. (default=0.6)
