

# \<slot\>: The Web Component Slot element



::: section-content
The `<slot>` [HTML](../index) element---part of the [Web
Components](https://developer.mozilla.org/en-US/docs/Web/API/Web_components)
technology suite---is a placeholder inside a web component that you can
fill with your own markup, which lets you create separate DOM trees and
present them together.
:::

## Attributes

::: section-content
This element includes the [global attributes](../global_attributes).

[`name`](#name)

:   The slot\'s name.

    A ***named slot*** is a `<slot>` element with a `name` attribute.
:::

## Examples

::: section-content
::: code-example
[html]{.language-name}

``` {signature="EdmHcu4vr/mG3mZb9UbYS3bWpOcGqGLEvp/AfS718+U=" data-language="html"}
<template id="element-details-template">
  <style>
    details {
      font-family: "Open Sans Light", Helvetica, Arial, sans-serif;
    }
    .name {
      font-weight: bold;
      color: #217ac0;
      font-size: 120%;
    }
    h4 {
      margin: 10px 0 -8px 0;
      background: #217ac0;
      color: white;
      padding: 2px 6px;
      border: 1px solid #cee9f9;
      border-radius: 4px;
    }
    .attributes {
      margin-left: 22px;
      font-size: 90%;
    }
    .attributes p {
      margin-left: 16px;
      font-style: italic;
    }
  </style>
  <details>
    <summary>
      <code class="name">
        &lt;<slot name="element-name">NEED NAME</slot>&gt;
      </code>
      <span class="desc"><slot name="description">NEED DESCRIPTION</slot></span>
    </summary>
    <div class="attributes">
      <h4>Attributes</h4>
      <slot name="attributes"><p>None</p></slot>
    
  </details>
  <hr />
</template>
```
:::

::: {#sect1 .notecard .note}
**Note:** You can see this complete example in action at
[element-details](https://github.com/mdn/web-components-examples/tree/main/element-details){target="_blank"}
(see it [running
live](https://mdn.github.io/web-components-examples/element-details/){target="_blank"}).
In addition, you can find an explanation at [Using templates and
slots](https://developer.mozilla.org/en-US/docs/Web/API/Web_components/Using_templates_and_slots).
:::
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
<td><a href="../content_categories#flow_content">Flow content</a>, <a
href="../content_categories#phrasing_content">phrasing content</a></td>
</tr>
<tr class="even">
<th scope="row">Permitted content</th>
<td><a
href="../content_categories#transparent_content_model">Transparent</a></td>
</tr>
<tr class="odd">
<th scope="row">Events</th>
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLSlotElement/slotchange_event"><code>slotchange</code></a></td>
</tr>
<tr class="even">
<th scope="row">Tag omission</th>
<td>None, both the starting and ending tag are mandatory.</td>
</tr>
<tr class="odd">
<th scope="row">Permitted parents</th>
<td>Any element that accepts <a
href="../content_categories#phrasing_content">phrasing content</a></td>
</tr>
<tr class="even">
<th scope="row">Implicit ARIA role</th>
<td><a href="https://www.w3.org/TR/html-aria/#dfn-no-corresponding-role"
target="_blank">No corresponding role</a></td>
</tr>
<tr class="odd">
<th scope="row">Permitted ARIA roles</th>
<td>No <code>role</code> permitted</td>
</tr>
<tr class="even">
<th scope="row">DOM interface</th>
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLSlotElement"><code>HTMLSlotElement</code></a></td>
</tr>
</tbody>
</table>

</figure>
:::

## Specifications

::: _table
  ----------------------------------------------------------------------------------------------------
  Specification
  ----------------------------------------------------------------------------------------------------
  [HTML Standard\
  [\#
  the-slot-element]{.small}](https://html.spec.whatwg.org/multipage/scripting.html#the-slot-element)

  [DOM Standard\
  [\# shadow-tree-slots]{.small}](https://dom.spec.whatwg.org/#shadow-tree-slots)
  ----------------------------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
           Desktop                                                         Mobile                                                                                   
  -------- --------- ------ --------- ------------------- ------- -------- ----------------- ---------------- --------------------- --------------- --------------- ------------------
           Chrome    Edge   Firefox   Internet Explorer   Opera   Safari   WebView Android   Chrome Android   Firefox for Android   Opera Android   Safari on IOS   Samsung Internet
  `slot`   53        79     63        No                  40      10       53                53               63                    41              10              6.0
  `name`   53        79     63        No                  40      10       53                53               63                    41              10              6.0
:::

## See also {#see_also}

::: section-content
-   HTML [`<template>`](template) element
-   HTML [`slot`](../global_attributes/slot) attribute
-   CSS
    [`::slotted`](https://developer.mozilla.org/en-US/docs/Web/CSS/::slotted)
    pseudo-element
-   [CSS
    scoping](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_scoping)
    module
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Element/slot](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/slot){._attribution-link}
:::
