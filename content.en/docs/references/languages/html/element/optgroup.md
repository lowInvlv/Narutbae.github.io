

# \<optgroup\>: The Option Group element



::: section-content
The `<optgroup>` [HTML](../index) element creates a grouping of options
within a [`<select>`](select) element.
:::

## Try it {#try_it}

::: section-content
::: iframe
::: {.output-header .border-rounded-top}
#### HTML Demo: \<optgroup\> {#html-demo-optgroup .output-heading}

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
    <label for="dino-select">Choose a dinosaur:</label>
    <select id="dino-select">
      <optgroup label="Theropods">
        <option>Tyrannosaurus</option>
        <option>Velociraptor</option>
        <option>Deinonychus</option>
      </optgroup>
      <optgroup label="Sauropods">
        <option>Diplodocus</option>
        <option>Saltasaurus</option>
        <option>Apatosaurus</option>
      </optgroup>
    </select>
:::
:::

::: {#css-panel .section .hidden tabindex="0" role="tabpanel" aria-labelledby="css" aria-hidden="true"}
::: {#css-editor}
    label {
      display: block;
      margin-bottom: 10px;
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

::: {#sect1 .notecard .note}
**Note:** Optgroup elements may not be nested.
:::
:::

## Attributes

::: section-content
This element includes the [global attributes](../global_attributes).

[`disabled`](#disabled)

:   If this Boolean attribute is set, none of the items in this option
    group is selectable. Often browsers grey out such control and it
    won\'t receive any browsing events, like mouse clicks or
    focus-related ones.

[`label`](#label)

:   The name of the group of options, which the browser can use when
    labeling the options in the user interface. This attribute is
    mandatory if this element is used.
:::

## Examples

::: section-content
::: code-example
[html]{.language-name}

``` {signature="8d6LzWimwabx5QLlOyOM1drlp2h1OtESJZZ77PRdMe8=" data-language="html"}
<select>
  <optgroup label="Group 1">
    <option>Option 1.1</option>
  </optgroup>
  <optgroup label="Group 2">
    <option>Option 2.1</option>
    <option>Option 2.2</option>
  </optgroup>
  <optgroup label="Group 3" disabled>
    <option>Option 3.1</option>
    <option>Option 3.2</option>
    <option>Option 3.3</option>
  </optgroup>
</select>
```
:::
:::

### Result

::: section-content
::: {#sect2 .code-example}
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
<th scope="row"><a href="../content_categories">Content
categories</a></th>
<td>None.</td>
</tr>
<tr class="even">
<th scope="row">Permitted content</th>
<td>Zero or more <a href="option"><code>&lt;option&gt;</code></a>
elements.</td>
</tr>
<tr class="odd">
<th scope="row">Tag omission</th>
<td>The start tag is mandatory. The end tag is optional if this element
is immediately followed by another <code>&lt;optgroup&gt;</code>
element, or if the parent element has no more content.</td>
</tr>
<tr class="even">
<th scope="row">Permitted parents</th>
<td>A <a href="select"><code>&lt;select&gt;</code></a> element.</td>
</tr>
<tr class="odd">
<th scope="row">Implicit ARIA role</th>
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/group_role"><code>group</code></a></td>
</tr>
<tr class="even">
<th scope="row">Permitted ARIA roles</th>
<td>No <code>role</code> permitted</td>
</tr>
<tr class="odd">
<th scope="row">DOM interface</th>
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLOptGroupElement"><code>HTMLOptGroupElement</code></a></td>
</tr>
</tbody>
</table>

</figure>
:::

## Specifications

::: _table
  ----------------------------------------------------------------------------------------------------------------
  Specification
  ----------------------------------------------------------------------------------------------------------------
  [HTML Standard\
  [\#
  the-optgroup-element]{.small}](https://html.spec.whatwg.org/multipage/form-elements.html#the-optgroup-element)

  ----------------------------------------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
               Desktop                                                         Mobile                                                                                   
  ------------ --------- ------ --------- ------------------- ------- -------- ----------------- ---------------- --------------------- --------------- --------------- ------------------
               Chrome    Edge   Firefox   Internet Explorer   Opera   Safari   WebView Android   Chrome Android   Firefox for Android   Opera Android   Safari on IOS   Samsung Internet
  `optgroup`   1         12     1         5.5                 15      ≤4       4.4               18               4                     14              ≤3.2            1.0
  `disabled`   1         12     1         8                   15      ≤4       4.4               18               4                     14              ≤3.2            1.0
  `label`      1         12     1         5.5                 15      ≤4       4.4               18               4                     14              ≤3.2            1.0
:::

## See also {#see_also}

::: section-content
-   Other form-related elements: [`<form>`](form), [`<legend>`](legend),
    [`<label>`](label), [`<button>`](button), [`<select>`](select),
    [`<datalist>`](datalist), [`<option>`](option),
    [`<fieldset>`](fieldset), [`<textarea>`](textarea),
    [`<input>`](input), [`<output>`](output), [`<progress>`](progress)
    and [`<meter>`](meter).
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Element/optgroup](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/optgroup){._attribution-link}
:::
