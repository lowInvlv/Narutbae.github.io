

# virtualkeyboardpolicy



::: section-content
::: {#sect1 .notecard .experimental}
**Experimental:** **This is an [experimental
technology](https://developer.mozilla.org/en-US/docs/MDN/Writing_guidelines/Experimental_deprecated_obsolete#experimental)**\
Check the [Browser compatibility table](#browser_compatibility)
carefully before using this in production.
:::

The `virtualkeyboardpolicy` [global attribute](../global_attributes) is
an enumerated attribute. When specified on an element that also uses the
[`contenteditable`](../global_attributes#contenteditable) attribute, it
controls the on-screen virtual keyboard behavior on devices such as
tablets, mobile phones, or other devices where a hardware keyboard may
not be available.

The attribute must take one of the following values:

-   `auto` or an *empty string*, which automatically shows the virtual
    keyboard when the element is focused or tapped.
-   `manual`, which decouples focus and tap on the element from the
    virtual keyboard\'s state.
:::

## Specifications

::: _table
  ------------------------------------------------------------------------------------------------------------------------------------------------------
  Specification
  ------------------------------------------------------------------------------------------------------------------------------------------------------
  [VirtualKeyboard API\
  [\#
  dom-elementcontenteditable-virtualkeyboardpolicy]{.small}](https://w3c.github.io/virtual-keyboard/#dom-elementcontenteditable-virtualkeyboardpolicy)

  ------------------------------------------------------------------------------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
                            Desktop                                                         Mobile                                                                                   
  ------------------------- --------- ------ --------- ------------------- ------- -------- ----------------- ---------------- --------------------- --------------- --------------- ------------------
                            Chrome    Edge   Firefox   Internet Explorer   Opera   Safari   WebView Android   Chrome Android   Firefox for Android   Opera Android   Safari on IOS   Samsung Internet
  `virtualkeyboardpolicy`   94        94     No        No                  80      No       94                94               No                    66              No              17.0
:::

## See also {#see_also}

::: section-content
-   All [global attributes](../global_attributes)
-   [`HTMLElement.contentEditable`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/contentEditable)
    and
    [`HTMLElement.isContentEditable`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/isContentEditable)
-   [The VirtualKeyboard
    API](https://developer.mozilla.org/en-US/docs/Web/API/VirtualKeyboard_API)
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/virtualkeyboardpolicy](https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/virtualkeyboardpolicy){._attribution-link}
:::
