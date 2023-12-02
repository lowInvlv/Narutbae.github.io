

# \<xmp\>



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
:::

## Summary

::: section-content
The `<xmp>` [HTML](../index) element renders text between the start and
end tags without interpreting the HTML in between and using a monospaced
font. The HTML2 specification recommended that it should be rendered
wide enough to allow 80 characters per line.

::: {#sect2 .notecard .note}
**Note:** Do not use this element.

-   It has been deprecated since HTML3.2 and was not implemented in a
    consistent way. It was completely removed from current HTML.
-   Use the [`<pre>`](pre) element or, if semantically adequate, the
    [`<code>`](code) element instead. Note that you will need to escape
    the \'`<`\' character as \'`&lt;`\' and the \'`&`\' character as
    \'`&amp;`\' to make sure they are not interpreted as markup.
-   A monospaced font can also be obtained on any element, by applying
    an adequate [CSS](https://developer.mozilla.org/en-US/docs/Web/CSS)
    style using `monospace` as the generic-font value for the
    [`font-family`](https://developer.mozilla.org/en-US/docs/Web/CSS/font-family)
    property.
:::
:::

## Attributes

::: section-content
This element has no other attributes than the [global
attributes](../global_attributes), common to all elements.
:::

## DOM interface {#dom_interface}

::: section-content
This element implements the
[`HTMLElement`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement)
interface.
:::

## Specifications

::: _table
  -------------------------------------------------------------------------
  Specification
  -------------------------------------------------------------------------
  [HTML Standard\
  [\#
  xmp]{.small}](https://html.spec.whatwg.org/multipage/obsolete.html#xmp)

  -------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
  ----------------------------------------------------------------------------------------------------------------------------------------------
          Desktop                                                          Mobile                                                     
  ------- --------- ------ ------------------- ---------- ------- -------- --------- --------- ------------------- --------- -------- ----------
          Chrome    Edge   Firefox             Internet   Opera   Safari   WebView   Chrome    Firefox for Android Opera     Safari   Samsung
                                               Explorer                    Android   Android                       Android   on IOS   Internet

  `xmp`   1         12     1                   Yes        15      ≤4       4.4       18        4                   14        ≤3.2     1.0
                                                                                                                                      
                           Before Firefox 4,                                                   Before Firefox 4,                      
                           this element                                                        this element                           
                           implemented the                                                     implemented the                        
                           `HTMLSpanElement`                                                   `HTMLSpanElement`                      
                           interface instead                                                   interface instead                      
                           of the standard                                                     of the standard                        
                           `HTMLElement`                                                       `HTMLElement`                          
                           interface.                                                          interface.                             
  ----------------------------------------------------------------------------------------------------------------------------------------------
:::

## See also {#see_also}

::: section-content
-   The [`<pre>`](pre) and [`<code>`](code) elements to be used instead.
-   The [`<plaintext>`](plaintext) element, similar to
    [`<xmp>`](xmp){aria-current="page"} but also obsolete.
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Element/xmp](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/xmp){._attribution-link}
:::
