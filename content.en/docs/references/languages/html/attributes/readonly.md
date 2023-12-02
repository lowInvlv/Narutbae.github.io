

# HTML attribute: readonly



::: section-content
The Boolean `readonly` attribute, when present, makes the element not
mutable, meaning the user can not edit the control.
:::

## Try it {#try_it}

::: section-content
::: iframe
::: {.output-header .border-rounded-top}
#### HTML Demo: readonly {#html-demo-readonly .output-heading}

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

::: {#editor-container .editor-container .tabbed-shorter .hidden .border-rounded-bottom editor-type="tabbed"}
::: {#tab-container .section .tabs}
::: {#tablist .tab-list role="tablist"}
HTML

CSS

JavaScript
:::

::: {#html-panel .section .hidden tabindex="0" role="tabpanel" aria-labelledby="html" aria-hidden="true"}
::: {#html-editor}
    <label for="firstName">First Name:</label>
    <input name="firstName" type="text" value="Adam" />

    <label for="age">Age:</label>
    <input name="age" type="number" value="42" readonly />

    <label for="hobbies">Hobbies:</label>
    <textarea name="hobbies" readonly>Baseball</textarea>
:::
:::

::: {#css-panel .section .hidden tabindex="0" role="tabpanel" aria-labelledby="css" aria-hidden="true"}
::: {#css-editor}
    label {
      display: block;
      margin-top: 1em;
    }

    input:read-only,
    textarea:read-only {
      background-color: silver;
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

## Overview

::: section-content
If the `readonly` attribute is specified on an input element, because
the user can not edit the input, the element does not participate in
constraint validation.

The `readonly` attribute is supported by
[`text`](../element/input/text), [`search`](../element/input/search),
[`url`](../element/input/url), [`tel`](../element/input/tel),
[`email`](../element/input/email),
[`password`](../element/input/password),
[`date`](../element/input/date), [`month`](../element/input/month),
[`week`](../element/input/week), [`time`](../element/input/time),
[`datetime-local`](../element/input/datetime-local), and
[`number`](../element/input/number) [`<input>`](../element/input) types
and the [`<textarea>`](../element/textarea) form control elements. If
present on any of these input types and elements, the
[`:read-only`](https://developer.mozilla.org/en-US/docs/Web/CSS/:read-only)
pseudo class will match. If the attribute is not included, the
[`:read-write`](https://developer.mozilla.org/en-US/docs/Web/CSS/:read-write)
pseudo class will match.

The attribute is not supported or relevant to
[`<select>`](../element/select) or input types that are already not
mutable, such as [checkbox](../element/input/checkbox) and
[radio](../element/input/radio) or cannot, by definition, start with a
value, such as the [file](../element/input/file) input type.
[range](../element/input/range) and [color](../element/input/color), as
both have default values. It is also not supported on
[hidden](../element/input/hidden) as it can not be expected that a user
to fill out a form that is hidden. Nor is it supported on any of the
button types, including `image`.

::: {#sect1 .notecard .note}
**Note:** Only text controls can be made read-only, since for other
controls (such as checkboxes and buttons) there is no useful distinction
between being read-only and being disabled, so the `readonly` attribute
does not apply.
:::

When an input has the `readonly` attribute, the
[`:read-only`](https://developer.mozilla.org/en-US/docs/Web/CSS/:read-only)
pseudo-class also applies to it. Conversely, inputs that support the
`readonly` attribute but don\'t have the attribute set match the
[`:read-write`](https://developer.mozilla.org/en-US/docs/Web/CSS/:read-write)
pseudo-class.
:::

### Attribute interactions {#attribute_interactions}

::: section-content
The difference between [`disabled`](disabled) and `readonly` is that
read-only controls can still function and are still focusable, whereas
disabled controls can not receive focus and are not submitted with the
form and generally do not function as controls until they are enabled.

Because a read-only field cannot have its value changed by a user
interaction, [`required`](required) does not have any effect on inputs
with the `readonly` attribute also specified.

The only way to modify dynamically the value of the readonly attribute
is through a script.

::: {#sect2 .notecard .note}
**Note:** The `required` attribute is not permitted on inputs with the
`readonly` attribute specified.
:::
:::

### Usability

::: section-content
Browsers display the `readonly` attribute.
:::

### Constraint validation {#constraint_validation}

::: section-content
If the element is read-only, then the element\'s value can not be
updated by the user, and does not participate in constraint validation.
:::

## Example

### HTML

::: section-content
::: code-example
[html]{.language-name}

``` {signature="RJCuRfbiBrnq5z4Kdk+qq+xa9m0RIyhhUiI4LLrqoZw=" data-language="html"}
<div class="group">
  <input type="text" value="Some value" readonly="readonly" id="text" />
  <label for="text">Text box</label>

<div class="group">
  <input type="date" value="2020-01-01" readonly="readonly" id="date" />
  <label for="date">Date</label>

<div class="group">
  <input type="email" value="Some value" readonly="readonly" id="email" />
  <label for="email">Email</label>

<div class="group">
  <input type="password" value="Some value" readonly="readonly" id="pwd" />
  <label for="pwd">Password</label>

<div class="group">
  <textarea readonly="readonly" id="ta">Some value</textarea>
  <label for="ta">Message</label>

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

## Specifications

::: _table
  ------------------------------------------------------------------------------------------------------------
  Specification
  ------------------------------------------------------------------------------------------------------------
  [HTML Standard\
  [\#
  the-readonly-attribute]{.small}](https://html.spec.whatwg.org/multipage/input.html#the-readonly-attribute)

  ------------------------------------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
               Desktop                                                         Mobile                                                                                   
  ------------ --------- ------ --------- ------------------- ------- -------- ----------------- ---------------- --------------------- --------------- --------------- ------------------
               Chrome    Edge   Firefox   Internet Explorer   Opera   Safari   WebView Android   Chrome Android   Firefox for Android   Opera Android   Safari on IOS   Samsung Internet
  `readonly`   1         12     1         ≤6                  ≤12.1   ≤4       4.4               18               4                     ≤12.1           ≤3.2            1.0
:::

::: _table
               Desktop                                                         Mobile                                                                                   
  ------------ --------- ------ --------- ------------------- ------- -------- ----------------- ---------------- --------------------- --------------- --------------- ------------------
               Chrome    Edge   Firefox   Internet Explorer   Opera   Safari   WebView Android   Chrome Android   Firefox for Android   Opera Android   Safari on IOS   Samsung Internet
  `readonly`   1         12     1         5.5                 ≤12.1   1        4.4               18               4                     ≤12.1           1               1.0
:::

### html.elements.input.readonly

BCD tables only load in the browser with JavaScript enabled. Enable
JavaScript to view data.

### html.elements.textarea.readonly

BCD tables only load in the browser with JavaScript enabled. Enable
JavaScript to view data.

## See also {#see_also}

::: section-content
-   [`:read-only`](https://developer.mozilla.org/en-US/docs/Web/CSS/:read-only)
    and
    [`:read-write`](https://developer.mozilla.org/en-US/docs/Web/CSS/:read-write)
-   [`<input>`](../element/input)
-   [`<select>`](../element/select)
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes/readonly](https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes/readonly){._attribution-link}
:::
