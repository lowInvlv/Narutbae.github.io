

# \<strike\>



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

The `<strike>` [HTML](../index) element places a strikethrough
(horizontal line) over text.

::: {#sect2 .notecard .warning}
**Warning:** This element is deprecated in HTML 4 and XHTML 1, and
obsoleted in the [HTML Living
Standard](https://html.spec.whatwg.org/multipage/obsolete.html#strike){target="_blank"}.
If semantically appropriate, i.e., if it represents *deleted* content,
use [`<del>`](del) instead. In all other cases use [`<s>`](s).
:::
:::

## Attributes

::: section-content
This element includes the [global attributes](../global_attributes).
:::

## Examples

::: section-content
::: code-example
[html]{.language-name}

``` {signature="+06vveLhj+8oJeCPAhwcMpJos94tBc5ZOhZfsgUW8vU=" data-language="html"}
&lt;strike&gt;: <strike>Today's Special: Salmon</strike> SOLD OUT<br />
&lt;s&gt;: <s>Today's Special: Salmon</s> SOLD OUT
```
:::
:::

### Result

::: section-content
::: {#sect3 .code-example}
::: iframe
:::
:::
:::

## Technical summary {#technical_summary}

::: section-content
<figure class="table-container">
<div class="_table">
<table class="properties">
<tbody>
<tr class="odd">
<th scope="row">DOM interface</th>
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement"><code>HTMLElement</code></a></td>
</tr>
</tbody>
</table>

</figure>
:::

## Specifications

::: _table
  -------------------------------------------------------------------------------
  Specification
  -------------------------------------------------------------------------------
  [HTML Standard\
  [\#
  strike]{.small}](https://html.spec.whatwg.org/multipage/obsolete.html#strike)

  -------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
  -------------------------------------------------------------------------------------------------------------------------------------------------
             Desktop                                                          Mobile                                                     
  ---------- --------- ------ ------------------- ---------- ------- -------- --------- --------- ------------------- --------- -------- ----------
             Chrome    Edge   Firefox             Internet   Opera   Safari   WebView   Chrome    Firefox for Android Opera     Safari   Samsung
                                                  Explorer                    Android   Android                       Android   on IOS   Internet

  `strike`   1         12     1                   Yes        15      ≤4       4.4       18        4                   14        ≤3.2     1.0
                                                                                                                                         
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
-   The [`<s>`](s) element.
-   The [`<del>`](del) element should be used if the data has been
    *deleted*.
-   The CSS
    [`text-decoration`](https://developer.mozilla.org/en-US/docs/Web/CSS/text-decoration)
    property can be used to style text with a strikethrough.
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Element/strike](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/strike){._attribution-link}
:::
