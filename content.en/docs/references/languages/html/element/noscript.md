

# \<noscript\>: The Noscript element



::: section-content
The `<noscript>` [HTML](../index) element defines a section of HTML to
be inserted if a script type on the page is unsupported or if scripting
is currently turned off in the browser.

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
<td><a href="../content_categories#metadata_content">Metadata
content</a>, <a href="../content_categories#flow_content">flow
content</a>, <a href="../content_categories#phrasing_content">phrasing
content</a>.</td>
</tr>
<tr class="even">
<th scope="row">Permitted content</th>
<td>When scripting is disabled and when it is a descendant of the <a
href="head"><code>&lt;head&gt;</code></a> element: in any order, zero or
more <a href="link"><code>&lt;link&gt;</code></a> elements, zero or more
<a href="style"><code>&lt;style&gt;</code></a> elements, and zero or
more <a href="meta"><code>&lt;meta&gt;</code></a> elements.<br />
When scripting is disabled and when it isn't a descendant of the <a
href="head"><code>&lt;head&gt;</code></a> element: any <a
href="../content_categories#transparent_content_model">transparent
content</a>, but no <code>&lt;noscript&gt;</code> element must be among
its descendants.<br />
Otherwise: flow content or phrasing content.</td>
</tr>
<tr class="odd">
<th scope="row">Tag omission</th>
<td>None, both the starting and ending tag are mandatory.</td>
</tr>
<tr class="even">
<th scope="row">Permitted parents</th>
<td>Any element that accepts <a
href="../content_categories#phrasing_content">phrasing content</a>, if
there are no ancestor <code>&lt;noscript&gt;</code> element, or in a <a
href="head"><code>&lt;head&gt;</code></a> element (but only for an HTML
document), here again if there are no ancestor
<code>&lt;noscript&gt;</code> element.</td>
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

## Attributes

::: section-content
This element only includes the [global
attributes](../global_attributes).
:::

## Examples

::: section-content
::: code-example
[html]{.language-name}

``` {signature="OOhJQl/3vn5jXTIZwHLqDDg9lfwwyY16x6xvY8+6LfE=" data-language="html"}
<noscript>
  <!-- anchor linking to external file -->
  <a href="https://www.mozilla.org/">External Link</a>
</noscript>
<p>Rocks!</p>
```
:::
:::

### Result with scripting enabled {#result_with_scripting_enabled}

::: section-content
Rocks!
:::

### Result with scripting disabled {#result_with_scripting_disabled}

::: section-content
[External Link](https://www.mozilla.org/){target="_blank"}

Rocks!
:::

## Specifications

::: _table
  ------------------------------------------------------------------------------------------------------------
  Specification
  ------------------------------------------------------------------------------------------------------------
  [HTML Standard\
  [\#
  the-noscript-element]{.small}](https://html.spec.whatwg.org/multipage/scripting.html#the-noscript-element)

  ------------------------------------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
               Desktop                                                         Mobile                                                                                   
  ------------ --------- ------ --------- ------------------- ------- -------- ----------------- ---------------- --------------------- --------------- --------------- ------------------
               Chrome    Edge   Firefox   Internet Explorer   Opera   Safari   WebView Android   Chrome Android   Firefox for Android   Opera Android   Safari on IOS   Samsung Internet
  `noscript`   1         12     1         Yes                 15      3        4.4               18               4                     14              2               1.0
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Element/noscript](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/noscript){._attribution-link}
:::
