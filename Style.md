---
title: Style
short_desc: Style type documentation
tags: api
path: lua_api/Style
uuid: 4141747e-0eb4-5055-9412-e42c8b40fd0b
public: true
private: false
---



### Properties

* **id** *string* The id of the style.
* **classes** *string[]* An alias for @see selectors
* **selectors** *string[]* The selection criteria by which this style will be applied to panels. A value like {"hover"} means that the style will only apply to panels with the 'hover' class. The panel must match all selected criteria, so {"hover", "active"} means that the panel must have the hover and active classes. Using ~ in front of a class name means the panel must NOT have the class. Using # references a panel's id instead of its class. putting parent: in front of a class means that the panel's parent must have that class. {'parent:hover', 'active', '~icon'} means we only match a panel if the parent has hover, if the panel has the active class and the panel does not have the icon class.
* **borderImage** *string* (write-only) the image to use for the panel's border.
* **bgimageReadable** *boolean* Set this to true if the bgimage specified in this style must be readable. This should be used for panels that have alphaHitTest set to true. Avoid setting this since it has performance implications.
* **bgimage** *string|boolean* The image to set as the background of this panel. May set to true to be a white square (same as 'panels/square.png') or false to make no bgimage. If left unset the panel will not have a background image. Note that the background image is the main display of most panels, so if this is not set the panel will be invisible, though its children may still be visible. This can be set to 'panels/square.png' to set to a plain white square image (which can then have further styling set to it). It can also be set to an image uploaded in a mod, e.g. bgimage = mod.images.myicon
* **blend** *"blend"|"add"* The blend mode used when drawing the panel.
* **inherit_selectors** *boolean* (Default=false) If set to true, selectors match if they match any parent. If false, the selectors must match the panel itself, and parent panels are not considered.
* **setting** *nil|string* (write-only) if this is set to the id of a setting, then that setting must be true for this style to apply. Otherwise it will be ignored.
* **priority** *number* (Default=0) the priority of the style compared to other styles. Higher priority styles will be prioritized over lower-priority styles. Note that selfStyle set on a panel is always the highest priority.
* **transitionTime** *number* (Default=0) When this is set to a non zero value, class changes that cause this style to be applied or removed from the panel will transition over this amount of time. For example, if a style is applied that sets opacity = 0 with transitionTime = 1, the panel will fade over the period of a second.
* **easing** *Easing* The easing this panel will use when applying @see transitionTime
* **hidden** *number* When set to 1, the panel will be hidden. A hidden panel is completely non-interactive and invisible. All its children will also be hidden. It can still receive programmatic events. A hidden panel still takes up space in the flow.
* **collapsed** *number* When set to 1, the panel will be collapsed. A collapsed panel is completely non-interactive and invisible. All its children will also be hidden. It can still receive programmatic events. A collapsed panel differs from a hidden panel in that it does not take up any space.
* **fontFace** *FontFace* The font face that will be used for any text displayed on the panel.
* **fontSize** *number* (write-only) The font size to use when displaying text on this label. @see minFontSize
* **minFontSize** *nil|number* (write-only) If set, the font size used when displaying text will automatically be reduced to make the text fit in the available area. It will be as small as minFontSize if necessary to make all the text display.
* **textAlignment** *TextAlignment* The alignment of the text displayed in this panel.
* **textOverflow** *TextOverflowMode* The behavior to use when the text cannot fit in the available area of the panel.
* **fontWeight** *FontWeight* The weight of the font to use when displaying text in this panel.
* **bgcolor** *string|Color|NamedColor* The color used when rendering the bgimage when displaying this panel. This color will be combined with any color in the bgimage. If you set the color to "white" the bgimage will be drawn without modification. Accepts HTML-style colors, e.g. "#ff0000" -- draw in flat red. "#00ff0088" -- draw in green with partial transparency.
* **borderColor** *string|Color|NamedColor* The color of the panel's border.
* **textOutlineColor** *string|Color|NamedColor* The color of the panel's text outline. @see textOutlineWidth
* **color** *string|Color|NamedColor* The color of text drawn on the panel.
* **highlightedColor** *string|Color|NamedColor* The color of text highlighting on the panel.
* **scrollHandleColor** *NamedColor|string|Color* The color of the scroll handle.
* **halign** *"left"|"center"|"right"* The horizontal alignment of the panel within its parent.
* **valign** *"top"|"center"|"bottom"* The vertical alignment of the panel within its parent.
* **flow** *"none"|"horizontal"|"vertical"* The method used to position this panel's children. none = the children will be positioned within this panel, based on their @see halign and @see valign. @see hmargin and @see vmargin will be used to keep them away from the edges of the panel. No attempt will be made to stop the child panels from overlapping. horizontal = the panels will be placed in order, left to right. @see valign will be used to control how children are positioned vertically. @see hmargin will be used to decide how much space to place between panels. If @see wrap is true, then if there is not enough space the children will wrap to a new row, otherwise they will overflow the area unless hscroll is set on the panel. Flow of vertical is similar to horizontal except the panels are arranged vertically, top to bottom instead of left to right. Floating child panels will all be placed as though flow = none.
* **textWrap** *boolean* If true, text that cannot fit will be wrapped to a new line. If false, text will never be wrapped across multiple lines and @see textOverflow will be used to handle text that doesn't fit in the panel's area.
* **wrap** *boolean* If true, then if child panels when @see flow is horizontal or vertical don't fit in the available space, they will be wrapped into columns or rows.
* **pad** *number* The padding, in pixels to place round the edge of the panel. Padding is considered part of the panel.
* **hpad** *number* The horizontal padding, in pixels to place round the edge of the panel. Padding is considered part of the panel.
* **vpad** *number* The vertical padding, in pixels to place round the edge of the panel. Padding is considered part of the panel.
* **margin** *number* The margin, in pixels to place round the edge of the panel. This is the space between the panel and the edge of the parent, as well as the distance from sibling panels when the parent has a @see flow of horizontal or vertical.
* **hmargin** *number* The horizontal margin, in pixels to place round the edge of the panel. This is the space between the panel and the edge of the parent, as well as the distance from sibling panels when the parent has a @see flow of horizontal.
* **vmargin** *number* The vertical margin, in pixels to place round the edge of the panel. This is the space between the panel and the edge of the parent, as well as the distance from sibling panels when the parent has a @see flow of vertical.
* **tmargin** *number* The vertical (top) margin, in pixels to place round the edge of the panel. This is the space between the panel and the edge of the parent, as well as the distance from sibling panels when the parent has a @see flow of vertical.
* **bmargin** *number* The vertical (bottom) margin, in pixels to place round the edge of the panel. This is the space between the panel and the edge of the parent, as well as the distance from sibling panels when the parent has a @see flow of vertical.
* **lmargin** *number* The horizontal (left) margin, in pixels to place round the edge of the panel. This is the space between the panel and the edge of the parent, as well as the distance from sibling panels when the parent has a @see flow of horizontal.
* **rmargin** *number* The horizontal (right) margin, in pixels to place round the edge of the panel. This is the space between the panel and the edge of the parent, as well as the distance from sibling panels when the parent has a @see flow of horizontal.
* **width** *"auto"|string|number* The width of the panel. If a number, it represents the width in pixels. 'auto' will calculated the width based on any child panels as well as text. A string may also be used, giving the width as a percentage, such as "40%" in which case it is 40% of the width of its parent. A percentage may have a fixed pixel value subtracted from it, such as "100%-40" in which case the width is 100% of the parent width minus 40 pixels. You can also set to a value based on the height, like "50% height" to set the width of the panel to half the height of the panel. "100% height" is a common way to make a panel square. Also (experimental) you may use a width such as "80% available" to consume 80% of the space that is available after other panels have been placed. This should only be used if the parent has a flow of horizontal. Note that @see minWidth and @see maxWidth are numeric values that can be used to place lower and upper bounds on width.
* **height** *"auto"|string|number* The height of the panel. @see width for details on usage.
* **minWidth** *number* The minimum possible width in pixels for this panel.
* **maxWidth** *number* The maximum possible width in pixels for this panel.
* **minHeight** *number* The minimum possible height in pixels for this panel.
* **maxHeight** *number* The maximum possible height in pixels for this panel.
* **brightness** *number* (default=1) The brightness of the panel. A value of above 1 can cause the panel to 'shine' brightly and spill light out over the nearby area.
* **hueshift** *number* (default=0) the amount to shift the hue of this panel.
* **saturation** *number* (default=1) the saturation to apply to this panel.
* **contrast** *number* (default=1) the contrast to apply to this panel.
* **inversion** *number* (default=1) the color inversion to apply to this panel.
* **opacity** *number* (default=1) the opacity of this panel. Setting this to 1 makes the panel fully opaque, to 0 makes it fully transparent.
* **alphaThreshold** *nil|number* (default=nil) If set, when drawing this panel the alpha won't be used to fade the panel, but rather, pixels below this threshold will be fully transparent, and pixels above it will be fully opaque.
* **alphaThresholdFade** *number* (default=0) When using @see alphaThreshold, this value determines the alpha range where pixels fade from being fully opaque to fully transparent.
* **textOutlineWidth** *number* The width of the outline around text. @see textOutlineColor
* **imageRect** *nil|Vector4Arg* (default=nil) when nil, the entire bgimage is drawn. When set to a vector, it specifies the normalized vector (going from (0,0) to (1,1)) within the image that will be drawn.
* **rotate** *nil|number* The rotation to apply to this panel, in degrees. Panels will be rotated around their @see pivot.
* **edgeFade** *nil|number* The number of pixels at the edge of the panel that the panel fades out.
* **x** *nil|number* The amount to translate the panel on the x axis. This happens after calculating the panel's normal placement and does not alter the placement calculation of other panels.
* **y** *nil|number* The amount to translate the panel on the y axis. This happens after calculating the panel's normal placement and does not alter the placement calculation of other panels.
* **translate** *nil|Vector2* The amount to translate the panel. This happens after calculating the panel's normal placement and does not alter the placement calculation of other panels.
* **scale** *number|Vector2Arg* The amount to scale the panel. This does not affect layout or positioning of other panels.
* **uiscale** *number|Vector2Arg* The amount to scale the panel. This DOES affect the panel's calculated size for layout purposes and thus the position of other panels.
* **pivot** *Vector2Arg* (default=0.5,0.5) the position around which the panel 
* **bold** *boolean* Whether to display text as bold. @see fontWeight for more control over a font's weight.
* **underline** *boolean* Whether to display text as underlined.
* **italics** *boolean* Whether to display text as italics.
* **border** *number|Vector4* (default=0) When set to a Vector4, the widths of each side are represented. When set to a number, all wides have that width border. @see borderColor
* **stretch** *nil|Vector4* (experimental!) A stretch to apply to the panel, deforming it.
* **bgslice** *nil|Vector4* When set to a Vector4, a rectangle within the normalized coordinates of the bgimage is specified. This inner rectangle will be stretched to fill the panel, while the edges will maintain their width and height.
* **cornerRadius** *number|string|Vector4* (default=0) When set to a number, this controls the rounding of corners when drawing the panel. As an example, if you have a 64x64 panel and set cornerRadius to 32, a perfect circle will be drawn. Setting to a Vector4 will make each corner have a different radius. You can also set to a string with a dimension calculation similar to @see width and @see height. For instance if you have a rectangular panel which is much widget than it is tall, "50% height" will make it perfectly rounded at each end.
* **borderWidth** *number* The width of the border. A simpler way of writing @see border.
* **gradient** *nil|Gradient* The gradient that will be used when rendering the bgimage for this panel.
* **strikethrough** *boolean* Draws text with strikethrough.
* **notranslation** *boolean* Will suppress translation of text into other languages for this panel.
* **uppercase** *boolean* Text on this panel will be rendered as uppercase.
* **lowercase** *boolean* Text on this panel will be rendered as lowercase.
* **smallcaps** *boolean* Text on this panel will be rendered as uppercase, with lower case letters displayed in a smaller font size but still uppercase.
* **beveledcorners** *boolean* Corners on this panel will be beveled rather than rounded according to cornerRadius.
* **autosizeimage** *boolean* @see width and @see height should both be set to auto to use this field. When set, the size of the panel will be set to the size of the bgimage. @see minWidth, @see maxWidth, @see minHeight, @see maxHeight will all still be respected, and the dimensions of the image will be changed to maintain the aspect ratio of the bgimage. Without this setting the bgimage's dimensions and aspect ratio are ignored and it is made to stretch across the panel.
* **borderFade** *boolean* (Default=false) When set, the border will fade out along its dimensions.
* **nostretch** *boolean* (Default=false) When set, the bgimage will not be stretched across the panel. Instead, if the aspect ratio of the panel and the bgimage don't match, only part of the bgimage will be displayed, but it won't be stretched.
* **worldspace** *boolean* (Experimental!) If set, the panel is placed in world space rather than in UI space.
