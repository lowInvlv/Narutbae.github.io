

# \<dd\>: The Description Details element



::: section-content
The `<dd>` [HTML](../index) element provides the description,
definition, or value for the preceding term ([`<dt>`](dt)) in a
description list ([`<dl>`](dl)).
:::

## Try it {#try_it}

::: section-content
::: iframe
::: {.output-header .border-rounded-top}
#### HTML Demo: \<dd\> {#html-demo-dd .output-heading}

Reset
:::

::: {#warning-no-script .warning-container}
::: warning
The interactive example cannot be shown because JavaScript is disabled.
:::
:::

::: {#warning-mathml-not-supported .warning-container .hidden}
::: warning
The interactive example cannot be shown because MathML is not supported
by your browser.
:::
:::

::: {#editor-container .editor-container .tabbed-standard .hidden .border-rounded-bottom editor-type="tabbed"}
::: {#tab-container .section .tabs}
::: {#tablist .tab-list role="tablist"}
HTML

CSS

JavaScript
:::

::: {#html-panel .section .hidden tabindex="0" role="tabpanel" aria-labelledby="html" aria-hidden="true"}
::: {#html-editor}
    <p>Cryptids of Cornwall:</p>

    <dl>
      <dt>Beast of Bodmin</dt>
      <dd>A large feline inhabiting Bodmin Moor.</dd>

      <dt>Morgawr</dt>
      <dd>A sea serpent.</dd>

      <dt>Owlman</dt>
      <dd>A giant owl-like creature.</dd>
    </dl>
:::
:::

::: {#css-panel .section .hidden tabindex="0" role="tabpanel" aria-labelledby="css" aria-hidden="true"}
::: {#css-editor}
    p,
    dt {
      font-weight: bold;
    }

    dl,
    dd {
      font-size: 0.9rem;
    }

    dd {
      margin-bottom: 1em;
    }
:::
:::

::: {#js-panel .section .hidden tabindex="0" role="tabpanel" aria-labelledby="js" aria-hidden="true"}
::: {#js-editor}
:::
:::
:::

::: {#output .output-container}
#### Output {.output-label}
:::
:::

::: {.section .console-container .hidden aria-hidden="true"}
#### Console Output {#console-output .console-label}

![]
clear console

::: {#console .console}
:::
:::

::: {#html-output .output .editor-tabbed}
%html-content%
:::
:::
:::

## Attributes

::: section-content
This element\'s attributes include the [global
attributes](../global_attributes).

[`nowrap`](#nowrap) [Non-standard]{.visually-hidden} [Deprecated]{.visually-hidden}

:   If the value of this attribute is set to `yes`, the definition text
    will not wrap. The default value is `no`.
:::

## Examples

::: section-content
For examples, see the [examples provided for the `<dl>`
element](dl#examples).
:::

## Technical summary {#technical_summary}

::: section-content
<figure class="table-container">
<div class="_table">
<table class="properties">
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<th scope="row"><a href="../content_categories">Content
categories</a></th>
<td>None.</td>
</tr>
<tr class="even">
<th scope="row">Permitted content</th>
<td><a href="../content_categories#flow_content">Flow content</a>.</td>
</tr>
<tr class="odd">
<th scope="row">Tag omission</th>
<td>The start tag is required. The end tag may be omitted if this
element is immediately followed by another <code>&lt;dd&gt;</code>
element or a <a href="dt"><code>&lt;dt&gt;</code></a> element, or if
there is no more content in the parent element.</td>
</tr>
<tr class="even">
<th scope="row">Permitted parents</th>
<td>A <a href="dl"><code>&lt;dl&gt;</code></a> or a <a
href="div"><code>&lt;div&gt;</code></a> that is a child of a <a
href="dl"><code>&lt;dl&gt;</code></a>.<br />
This element can be used after a <a
href="dt"><code>&lt;dt&gt;</code></a> or another <a href="dd"
aria-current="page"><code>&lt;dd&gt;</code></a> element.</td>
</tr>
<tr class="odd">
<th scope="row">Implicit ARIA role</th>
<td><a href="https://www.w3.org/TR/html-aria/#dfn-no-corresponding-role"
target="_blank">No corresponding role</a></td>
</tr>
<tr class="even">
<th scope="row">Permitted ARIA roles</th>
<td>No <code>role</code> permitted</td>
</tr>
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
  -------------------------------------------------------------------------------------------------------
  Specification
  -------------------------------------------------------------------------------------------------------
  [HTML Standard\
  [\#
  the-dd-element]{.small}](https://html.spec.whatwg.org/multipage/grouping-content.html#the-dd-element)

  -------------------------------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
  ---------------------------------------------------------------------------------------------------------------------------------------
             Desktop                                                          Mobile                                           
  ---------- --------- ------ ------------------- ---------- ------- -------- --------- --------- --------- --------- -------- ----------
             Chrome    Edge   Firefox             Internet   Opera   Safari   WebView   Chrome    Firefox   Opera     Safari   Samsung
                                                  Explorer                    Android   Android   for       Android   on IOS   Internet
                                                                                                  Android                      

  `dd`       1         12     1                   Yes        15      ≤4       4.4       18        4         14        ≤3.2     1.0
                                                                                                                               
                              Before Firefox 4,                                                                                
                              this element was                                                                                 
                              implemented using                                                                                
                              the                                                                                              
                              `HTMLSpanElement`                                                                                
                              interface instead                                                                                
                              of `HTMLElement`.                                                                                

  `nowrap`   1         12     1                   Yes        15      ≤4       4.4       18        4         14        ≤3.2     1.0
  ---------------------------------------------------------------------------------------------------------------------------------------
:::

## See also {#see_also}

::: section-content
-   [`<dl>`](dl)
-   [`<dt>`](dt)
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Element/dd](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/dd){._attribution-link}
:::
