

# HTML attribute: size



::: section-content
The `size` attribute defines the width of the
[`<input>`](../element/input) and the height of the
[`<select>`](../element/select) element. For the `input`, if the `type`
attribute is [text](../element/input/text) or
[password](../element/input/password) then it\'s the number of
characters. This must be an integer value of 0 or higher. If no `size`
is specified, or an invalid value is specified, the input has no size
declared, and the form control will be the default width based on the
user agent. If CSS targets the element with properties impacting the
width, CSS takes precedence.

The `size` attribute has no impact on constraint validation.
:::

## Try it {#try_it}

::: section-content
::: iframe
::: {.output-header .border-rounded-top}
#### HTML Demo: size {#html-demo-size .output-heading}

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
    <label for="firstName">First Name:</label>
    <input name="firstName" type="text" size="10" />

    <label for="lastName">Last Name:</label>
    <input name="lastName" type="text" size="20" />

    <label for="fruit">Favourite fruit:</label>
    <select name="fruit" size="2">
      <option>Orange</option>
      <option>Banana</option>
      <option>Apple</option>
    </select>
:::
:::

::: {#css-panel .section .hidden tabindex="0" role="tabpanel" aria-labelledby="css" aria-hidden="true"}
::: {#css-editor}
    label {
      display: block;
      margin-top: 1rem;
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

## Examples

::: section-content
By adding `size` on some input types, the width of the input can be
controlled. Adding size on a select changes the height, defining how
many options are visible in the closed state.

::: code-example
[html]{.language-name}

``` {signature="r3ovSDU1oAD4FwwBlp9VvDXcvm1fOpkn9p4iJIPtdLA=" data-language="html"}
<label for="fruit">Enter a fruit</label>
<input type="text" size="15" id="fruit" />
<label for="vegetable">Enter a vegetable</label>
<input type="text" id="vegetable" />

<select name="fruits" size="5">
  <option>banana</option>
  <option>cherry</option>
  <option>strawberry</option>
  <option>durian</option>
  <option>blueberry</option>
</select>

<select name="vegetables" size="5">
  <option>carrot</option>
  <option>cucumber</option>
  <option>cauliflower</option>
  <option>celery</option>
  <option>collard greens</option>
</select>
```
:::

::: {#sect1 .code-example}
::: iframe
:::
:::
:::

## Specifications

::: {.notecard .warning}
**No specification found**

No specification data found for `html.elements.attribute.size`.\
[Check for problems with this page](#on-github) or contribute a missing
`spec_url` to
[mdn/browser-compat-data](https://github.com/mdn/browser-compat-data).
Also make sure the specification is included in
[w3c/browser-specs](https://github.com/w3c/browser-specs).
:::

## Browser compatibility {#browser_compatibility}

## See also {#see_also}

::: section-content
-   [`maxlength`](maxlength)
-   [`minlength`](minlength)
-   [`pattern`](pattern)
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes/size](https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes/size){._attribution-link}
:::
