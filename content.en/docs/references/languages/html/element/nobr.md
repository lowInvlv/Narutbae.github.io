

# \<nobr\>: The Non-Breaking Text element



::: section-content
::: {#sect1 .notecard .deprecated}
**Deprecated:** This feature is no longer recommended. Though some
browsers might still support it, it may have already been removed from
the relevant web standards, may be in the process of being dropped, or
may only be kept for compatibility purposes. Avoid using it, and update
existing code if possible; see the [compatibility
table](#browser_compatibility) at the bottom of this page to guide your
decision. Be aware that this feature may cease to work at any time.
:::

The `<nobr>` [HTML](../index) element prevents the text it contains from
automatically wrapping across multiple lines, potentially resulting in
the user having to scroll horizontally to see the entire width of the
text.

::: {#sect2 .notecard .warning}
**Warning:** Although this element is widely supported, it was *never*
standard HTML, so you shouldn\'t use it. Instead, use the CSS property
[`white-space`](https://developer.mozilla.org/en-US/docs/Web/CSS/white-space)
like this:
:::

::: code-example
[html]{.language-name}

``` {signature="ojJQqBHOsvuFfGOUqwPzOXxvw3vyGh4KH/An+Lwh1yY=" data-language="html"}
<span style="white-space: nowrap;">Long line with no breaks</span>
```
:::
:::

## Specifications

::: _table
  ---------------------------------------------------------------------------
  Specification
  ---------------------------------------------------------------------------
  [HTML Standard\
  [\#
  nobr]{.small}](https://html.spec.whatwg.org/multipage/obsolete.html#nobr)

  ---------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
           Desktop                                                         Mobile                                                                                   
  -------- --------- ------ --------- ------------------- ------- -------- ----------------- ---------------- --------------------- --------------- --------------- ------------------
           Chrome    Edge   Firefox   Internet Explorer   Opera   Safari   WebView Android   Chrome Android   Firefox for Android   Opera Android   Safari on IOS   Samsung Internet
  `nobr`   1         12     1         Yes                 15      ≤4       4.4               18               4                     14              ≤3.2            1.0
:::

## See also {#see_also}

::: section-content
-   [`white-space`](https://developer.mozilla.org/en-US/docs/Web/CSS/white-space)
-   [`overflow`](https://developer.mozilla.org/en-US/docs/Web/CSS/overflow)
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Element/nobr](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/nobr){._attribution-link}
:::
