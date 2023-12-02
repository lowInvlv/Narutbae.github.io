

# \<legend\>: The Field Set Legend element



::: section-content
The `<legend>` [HTML](../index) element represents a caption for the
content of its parent [`<fieldset>`](fieldset).
:::

## Try it {#try_it}

::: section-content
::: iframe
::: {.output-header .border-rounded-top}
#### HTML Demo: \<legend\> {#html-demo-legend .output-heading}

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
    <fieldset>
      <legend>Choose your favorite monster</legend>

      <input type="radio" id="kraken" name="monster" value="K" />
      <label for="kraken">Kraken</label><br />

      <input type="radio" id="sasquatch" name="monster" value="S" />
      <label for="sasquatch">Sasquatch</label><br />

      <input type="radio" id="mothman" name="monster" value="M" />
      <label for="mothman">Mothman</label>
    </fieldset>
:::
:::

::: {#css-panel .section .hidden tabindex="0" role="tabpanel" aria-labelledby="css" aria-hidden="true"}
::: {#css-editor}
    legend {
      background-color: #000;
      color: #fff;
      padding: 3px 6px;
    }

    input {
      margin: 0.4rem;
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
See [`<form>`](form) for examples on `<legend>`.
:::

## Technical summary {#technical_summary}

::: section-content
<figure class="table-container">
<div class="_table">
<table class="properties">
<tbody>
<tr class="odd">
<th scope="row"><a href="../content_categories">Content
categories</a></th>
<td>None.</td>
</tr>
<tr class="even">
<th scope="row">Permitted content</th>
<td><a href="../content_categories#phrasing_content">Phrasing
content</a> and <a href="heading_elements">headings</a> (h1–h6
elements).</td>
</tr>
<tr class="odd">
<th scope="row">Tag omission</th>
<td>None, both the starting and ending tag are mandatory.</td>
</tr>
<tr class="even">
<th scope="row">Permitted parents</th>
<td>A <a href="fieldset"><code>&lt;fieldset&gt;</code></a> whose first
child is this <code>&lt;legend&gt;</code> element</td>
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
href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLLegendElement"><code>HTMLLegendElement</code></a></td>
</tr>
</tbody>
</table>

</figure>
:::

## Specifications

::: _table
  ------------------------------------------------------------------------------------------------------------
  Specification
  ------------------------------------------------------------------------------------------------------------
  [HTML Standard\
  [\#
  the-legend-element]{.small}](https://html.spec.whatwg.org/multipage/form-elements.html#the-legend-element)

  ------------------------------------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
             Desktop                                                         Mobile                                                                                   
  ---------- --------- ------ --------- ------------------- ------- -------- ----------------- ---------------- --------------------- --------------- --------------- ------------------
             Chrome    Edge   Firefox   Internet Explorer   Opera   Safari   WebView Android   Chrome Android   Firefox for Android   Opera Android   Safari on IOS   Samsung Internet
  `legend`   1         12     1         6                   ≤12.1   3        4.4               18               4                     ≤12.1           1               1.0
  `align`    1         12     1         6                   ≤12.1   ≤4       4.4               18               4                     ≤12.1           ≤3.2            1.0
:::

## See also {#see_also}

::: section-content
-   [ARIA: Form
    role](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/form_role)
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Element/legend](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/legend){._attribution-link}
:::
