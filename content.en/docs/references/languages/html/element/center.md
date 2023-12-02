

# \<center\>: The Centered Text element



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

The `<center>` [HTML](../index) element is a [block-level
element](https://developer.mozilla.org/en-US/docs/Glossary/Block-level_content)
that displays its block-level or inline contents centered horizontally
within its containing element. The container is usually, but isn\'t
required to be, [`<body>`](body).

This tag has been deprecated in HTML 4 (and XHTML 1) in favor of the
[CSS](https://developer.mozilla.org/en-US/docs/Web/CSS)
[`text-align`](https://developer.mozilla.org/en-US/docs/Web/CSS/text-align)
property, which can be applied to the [``](div) element or to an
individual [`<p>`](p). For centering blocks, use other CSS properties
like
[`margin-left`](https://developer.mozilla.org/en-US/docs/Web/CSS/margin-left)
and
[`margin-right`](https://developer.mozilla.org/en-US/docs/Web/CSS/margin-right)
and set them to `auto` (or set
[`margin`](https://developer.mozilla.org/en-US/docs/Web/CSS/margin) to
`0 auto`).
:::

## DOM interface {#dom_interface}

::: section-content
This element implements the
[`HTMLElement`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement)
interface.
:::

## Example 1 {#example_1}

::: section-content
::: code-example
[html]{.language-name}

``` {signature="QAG/nhz6mxlS1q3vUQ32llBMluqIZzN5U7gV2Rrv84Q=" data-language="html"}
<center>
  This text will be centered.
  <p>So will this paragraph.</p>
</center>
```
:::
:::

## Example 2 (CSS alternative) {#example_2_css_alternative}

::: section-content
::: code-example
[html]{.language-name}

``` {signature="WHeCT8qPcYLDMCTLEy0OCLfDbANlWHiT+nCTYZN/T90=" data-language="html"}
<div style="text-align:center">
  This text will be centered.
  <p>So will this paragraph.</p>

```
:::
:::

## Example 3 (CSS alternative) {#example_3_css_alternative}

::: section-content
::: code-example
[html]{.language-name}

``` {signature="eVp61MLwR9WBeo9MPkSeLKyLE/DTSamLHKv1cgh8dLY=" data-language="html"}
<p style="text-align:center">
  This line will be centered.<br />
  And so will this line.
</p>
```
:::
:::

## Note

::: section-content
Applying
[`text-align`](https://developer.mozilla.org/en-US/docs/Web/CSS/text-align)`:center`
to a [``](div) or [`<p>`](p) element centers the *contents* of
those elements while leaving their overall dimensions unchanged.
:::

## Specifications

::: _table
  -------------------------------------------------------------------------------
  Specification
  -------------------------------------------------------------------------------
  [HTML Standard\
  [\#
  center]{.small}](https://html.spec.whatwg.org/multipage/obsolete.html#center)

  -------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
  -------------------------------------------------------------------------------------------------------------------------------------------------
             Desktop                                                          Mobile                                                     
  ---------- --------- ------ ------------------- ---------- ------- -------- --------- --------- ------------------- --------- -------- ----------
             Chrome    Edge   Firefox             Internet   Opera   Safari   WebView   Chrome    Firefox for Android Opera     Safari   Samsung
                                                  Explorer                    Android   Android                       Android   on IOS   Internet

  `center`   1         12     1                   Yes        15      ≤4       4.4       18        4                   14        ≤3.2     1.0
                                                                                                                                         
                              Before Firefox 4,                                                   Before Firefox 4,                      
                              this element                                                        this element                           
                              implemented the                                                     implemented the                        
                              `HTMLSpanElement`                                                   `HTMLSpanElement`                      
                              interface instead                                                   interface instead                      
                              of the standard                                                     of the standard                        
                              `HTMLElement`                                                       `HTMLElement`                          
                              interface.                                                          interface.                             
  -------------------------------------------------------------------------------------------------------------------------------------------------
:::

## See also {#see_also}

::: section-content
-   [`text-align`](https://developer.mozilla.org/en-US/docs/Web/CSS/text-align)
-   [`display`](https://developer.mozilla.org/en-US/docs/Web/CSS/display)
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Element/center](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/center){._attribution-link}
:::
