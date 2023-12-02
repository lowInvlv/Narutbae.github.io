

# \<dt\>: The Description Term element



::: section-content
The `<dt>` [HTML](../index) element specifies a term in a description or
definition list, and as such must be used inside a [`<dl>`](dl) element.
It is usually followed by a [`<dd>`](dd) element; however, multiple
`<dt>` elements in a row indicate several terms that are all defined by
the immediate next [`<dd>`](dd) element.

The subsequent [`<dd>`](dd) (**Description Details**) element provides
the definition or other related text associated with the term specified
using `<dt>`.
:::

## Try it {#try_it}

::: section-content
::: iframe
::: {.output-header .border-rounded-top}
#### HTML Demo: \<dt\> {#html-demo-dt .output-heading}

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
    <p>Please use the following paint colors for the new house:</p>

    <dl>
      <dt>Denim (semigloss finish)</dt>
      <dd>Ceiling</dd>

      <dt>Denim (eggshell finish)</dt>
      <dt>Evening Sky (eggshell finish)</dt>
      <dd>Layered on the walls</dd>
    </dl>
:::
:::

::: {#css-panel .section .hidden tabindex="0" role="tabpanel" aria-labelledby="css" aria-hidden="true"}
::: {#css-editor}
    p,
    dl {
      font:
        1rem 'Fira Sans',
        sans-serif;
    }

    dl > dt {
      font-weight: normal;
      font-style: oblique;
    }

    dd {
      margin-bottom: 1rem;
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
This element only includes the [global
attributes](../global_attributes).
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
<td><a href="../content_categories#flow_content">Flow content</a>, but
with no <a href="header"><code>&lt;header&gt;</code></a>, <a
href="footer"><code>&lt;footer&gt;</code></a>, sectioning content or
heading content descendants.</td>
</tr>
<tr class="odd">
<th scope="row">Tag omission</th>
<td>The start tag is required. The end tag may be omitted if this
element is immediately followed by another <code>&lt;dt&gt;</code>
element or a <a href="dd"><code>&lt;dd&gt;</code></a> element, or if
there is no more content in the parent element.</td>
</tr>
<tr class="even">
<th scope="row">Permitted parents</th>
<td>A <a href="dl"><code>&lt;dl&gt;</code></a> or (in <a
href="https://developer.mozilla.org/en-US/docs/Glossary/WHATWG">WHATWG</a>
HTML, <a
href="https://developer.mozilla.org/en-US/docs/Glossary/W3C">W3C</a>
HTML 5.2 and later) a <a href="div"><code>&lt;div&gt;</code></a> that is
a child of a <a href="dl"><code>&lt;dl&gt;</code></a>.<br />
This element can be used before a <a
href="dd"><code>&lt;dd&gt;</code></a> or another <a href="dt"
aria-current="page"><code>&lt;dt&gt;</code></a> element.</td>
</tr>
<tr class="odd">
<th scope="row">Implicit ARIA role</th>
<td><a href="https://www.w3.org/TR/html-aria/#dfn-no-corresponding-role"
target="_blank">No corresponding role</a></td>
</tr>
<tr class="even">
<th scope="row">Permitted ARIA roles</th>
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/listitem_role"><code>listitem</code></a></td>
</tr>
<tr class="odd">
<th scope="row">DOM interface</th>
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement"><code>HTMLElement</code></a>
Up to Gecko 1.9.2 (Firefox 4) inclusive, Firefox implements the <a
href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLSpanElement"><code>HTMLSpanElement</code></a>
interface for this element.</td>
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
  the-dt-element]{.small}](https://html.spec.whatwg.org/multipage/grouping-content.html#the-dt-element)

  -------------------------------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
         Desktop                                                         Mobile                                                                                   
  ------ --------- ------ --------- ------------------- ------- -------- ----------------- ---------------- --------------------- --------------- --------------- ------------------
         Chrome    Edge   Firefox   Internet Explorer   Opera   Safari   WebView Android   Chrome Android   Firefox for Android   Opera Android   Safari on IOS   Samsung Internet
  `dt`   1         12     1         Yes                 15      ≤4       4.4               18               4                     14              ≤3.2            1.0
:::

## See also {#see_also}

::: section-content
-   [`<dl>`](dl)
-   [`<dd>`](dd)
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Element/dt](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/dt){._attribution-link}
:::
