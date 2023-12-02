

# \<frameset\>



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

The `<frameset>` [HTML](../index) element is used to contain
[`<frame>`](frame) elements.

::: {#sect2 .notecard .note}
**Note:** Because the use of frames is now discouraged in favor of using
[`<iframe>`](iframe), this element is not typically used by modern
websites.
:::
:::

## Attributes

::: section-content
Like all other HTML elements, this element supports the [global
attributes](../global_attributes).

[`cols`](#cols) [Deprecated]{.visually-hidden}

:   This attribute specifies the number and size of horizontal spaces in
    a frameset.

[`rows`](#rows) [Deprecated]{.visually-hidden}

:   This attribute specifies the number and size of vertical spaces in a
    frameset.
:::

## Example

### A frameset document {#a_frameset_document}

::: section-content
A frameset document has a `<frameset>` element instead of a
[`<body>`](body) element. The [`<frame>`](frame) elements are placed
within the `<frameset>`.

::: code-example
[html]{.language-name}

``` {signature="AwmpgcEqEiowID+telj0ACRs1U1I9hau43QcctUtJgg=" data-language="html"}
<!doctype html>
<html lang="en-US">
  <head>
    <!-- Document metadata goes here -->
  </head>
  <frameset cols="50%, 50%">
    <frame src="https://developer.mozilla.org/en/HTML/Element/iframe" />
    <frame src="https://developer.mozilla.org/en/HTML/Element/frame" />
  </frameset>
</html>
```
:::

If you want to embed another HTML page into the [`<body>`](body) of a
document, use an [`<iframe>`](iframe) element.
:::

## Specifications

::: _table
  -----------------------------------------------------------------------------------
  Specification
  -----------------------------------------------------------------------------------
  [HTML Standard\
  [\#
  frameset]{.small}](https://html.spec.whatwg.org/multipage/obsolete.html#frameset)

  -----------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
               Desktop                                                         Mobile                                                                                   
  ------------ --------- ------ --------- ------------------- ------- -------- ----------------- ---------------- --------------------- --------------- --------------- ------------------
               Chrome    Edge   Firefox   Internet Explorer   Opera   Safari   WebView Android   Chrome Android   Firefox for Android   Opera Android   Safari on IOS   Samsung Internet
  `frameset`   1         12     1         Yes                 15      3        4.4               18               4                     14              2               1.0
  `cols`       1         12     1         Yes                 15      3        4.4               18               4                     14              2               1.0
  `rows`       1         12     1         Yes                 15      3        4.4               18               4                     14              2               1.0
:::

## See also {#see_also}

::: section-content
-   [`<frame>`](frame)
-   [`<iframe>`](iframe)
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Element/frameset](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/frameset){._attribution-link}
:::
