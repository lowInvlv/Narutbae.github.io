

# HTML attribute: disabled



::: section-content
The Boolean `disabled` attribute, when present, makes the element not
mutable, focusable, or even submitted with the form. The user can
neither edit nor focus on the control, nor its form control descendants.
:::

## Try it {#try_it}

::: section-content
::: iframe
::: {.output-header .border-rounded-top}
#### HTML Demo: disabled {#html-demo-disabled .output-heading}

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
    <form>
      <label for="name">Name:</label>
      <input name="name" type="text" />

      <label for="emp">Employed:</label>
      <select name="emp" disabled>
        <option>No</option>
        <option>Yes</option>
      </select>

      <label for="empDate">Employment Date:</label>
      <input name="empDate" type="date" disabled />

      <label for="resume">Resume:</label>
      <input name="resume" type="file" />
    </form>
:::
:::

::: {#css-panel .section .hidden tabindex="0" role="tabpanel" aria-labelledby="css" aria-hidden="true"}
::: {#css-editor}
    label {
      display: block;
      margin-top: 1em;
    }

    *:disabled {
      background-color: dimgrey;
      color: linen;
      opacity: 1;
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
If the `disabled` attribute is specified on a form control, the element
and its form control descendants do not participate in constraint
validation. Often browsers grey out such controls and it won\'t receive
any browsing events, like mouse clicks or focus-related ones.

The `disabled` attribute is supported by
[`<button>`](../element/button), [`<fieldset>`](../element/fieldset),
[`<optgroup>`](../element/optgroup), [`<option>`](../element/option),
[`<select>`](../element/select), [`<textarea>`](../element/textarea) and
[`<input>`](../element/input).

This Boolean disabled attribute indicates that the user cannot interact
with the control or its descendant controls. If this attribute is not
specified, the control inherits its setting from the containing element,
for example `fieldset`; if there is no containing element with the
`disabled` attribute set, and the control itself does not have the
attribute, then the control is enabled. If declared on an
[`<optgroup>`](../element/optgroup), the select is still interactive
(unless otherwise disabled), but none of the items in the option group
are selectable.

::: {#sect1 .notecard .note}
**Note:** If a [`<fieldset>`](../element/fieldset) is disabled, the
descendant form controls are all disabled, with the exception of form
controls within the [`<legend>`](../element/legend).
:::

When a supporting element has the `disabled` attribute applied, the
[`:disabled`](https://developer.mozilla.org/en-US/docs/Web/CSS/:disabled)
pseudo-class also applies to it. Conversely, elements that support the
`disabled` attribute but don\'t have the attribute set match the
[`:enabled`](https://developer.mozilla.org/en-US/docs/Web/CSS/:enabled)
pseudo-class.

This Boolean attribute prevents the user from interacting with the
button. If this attribute isn\'t set, the button can still be disabled
from a containing element, for example
[`<fieldset>`](../element/fieldset); if there is no containing element
with the `disabled` attribute set, then the button is enabled.

Firefox will, unlike other browsers, persist the dynamic disabled state
of a [`<button>`](../element/button) across page loads. Use the
[`autocomplete`](autocomplete) attribute to control this feature.
:::

### Attribute interactions {#attribute_interactions}

::: section-content
The difference between `disabled` and [`readonly`](readonly) is that
read-only controls can still function and are still focusable, whereas
disabled controls can not receive focus and are not submitted with the
form and generally do not function as controls until they are enabled.

Because a disabled field cannot have its value changed,
[`required`](required) does not have any effect on inputs with the
`disabled` attribute also specified. Additionally, since the elements
become immutable, most other attributes, such as [`pattern`](pattern),
have no effect, until the control is enabled.

::: {#sect2 .notecard .note}
**Note:** The `required` attribute is not permitted on inputs with the
`disabled` attribute specified.
:::
:::

### Usability

::: section-content
Browsers display disabled form controls greyed as disabled form controls
are immutable, won\'t receive focus or any browsing events, like mouse
clicks or focus-related ones, and aren\'t submitted with the form.

If present on a supporting elements, the
[`:disabled`](https://developer.mozilla.org/en-US/docs/Web/CSS/:disabled)
pseudo class will match. If the attribute is not included, the
[`:enabled`](https://developer.mozilla.org/en-US/docs/Web/CSS/:enabled)
pseudo class will match. If the element doesn\'t support the disabled
attribute, the attribute will have no effect, including not leading to
being matched by the `:disabled` and `:enabled` pseudo classes.
:::

### Constraint validation {#constraint_validation}

::: section-content
If the element is `disabled`, then the element\'s value can not receive
focus and cannot be updated by the user, and does not participate in
constraint validation.
:::

## Examples

::: section-content
When form controls are disabled, many browsers will display them in a
lighter, greyed-out color by default. Here are examples of a disabled
checkbox, radio button, [`<option>`](../element/option) and
[`<optgroup>`](../element/optgroup), as well as some form controls that
are disabled via the disabled attribute set on the ancestor
[`<fieldset>`](../element/fieldset) element. The
[`<option>`](../element/option)s are disabled, but the
[`<select>`](../element/select) itself is not. We could have disable the
entire [`<select>`](../element/select) by adding the attribute to that
element rather than its descendants.

::: code-example
[html]{.language-name}

``` {signature="EOsEK3sitO2qLwgsbHG5V2CfWpfRgmmb/kb/Ue92lto=" data-language="html"}
<fieldset>
  <legend>Checkboxes</legend>
  <p>
    <label>
      <input type="checkbox" name="chbox" value="regular" /> Regular
    </label>
  </p>
  <p>
    <label>
      <input type="checkbox" name="chbox" value="disabled" disabled /> disabled
    </label>
  </p>
</fieldset>

<fieldset>
  <legend>Radio buttons</legend>
  <p>
    <label> <input type="radio" name="radio" value="regular" /> Regular </label>
  </p>
  <p>
    <label>
      <input type="radio" name="radio" value="disabled" disabled /> disabled
    </label>
  </p>
</fieldset>

<p>
  <label
    >Select an option:
    <select>
      <optgroup label="Group 1">
        <option>Option 1.1</option>
      </optgroup>
      <optgroup label="Group 2">
        <option>Option 2.1</option>
        <option disabled>Option 2.2</option>
        <option>Option 2.3</option>
      </optgroup>
      <optgroup label="Group 3" disabled>
        <option>Disabled 3.1</option>
        <option>Disabled 3.2</option>
        <option>Disabled 3.3</option>
      </optgroup>
    </select>
  </label>
</p>

<fieldset disabled>
  <legend>Disabled fieldset</legend>
  <p>
    <label>
      Name: <input type="name" name="radio" value="regular" /> Regular
    </label>
  </p>
  <p>
    <label>Number: <input type="number" /></label>
  </p>
</fieldset>
```
:::

::: {#sect3 .code-example}
::: iframe
:::
:::
:::

## Specifications

::: _table
  ----------------------------------------------------------------------------------------------------------------------
  Specification
  ----------------------------------------------------------------------------------------------------------------------
  [HTML Standard\
  [\#
  attr-fe-disabled]{.small}](https://html.spec.whatwg.org/multipage/form-control-infrastructure.html#attr-fe-disabled)

  [HTML Standard\
  [\# attr-optgroup-disabled]{.small}](https://html.spec.whatwg.org/multipage/form-elements.html#attr-optgroup-disabled)

  [HTML Standard\
  [\# attr-option-disabled]{.small}](https://html.spec.whatwg.org/multipage/form-elements.html#attr-option-disabled)
  ----------------------------------------------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
               Desktop                                                         Mobile                                                                                   
  ------------ --------- ------ --------- ------------------- ------- -------- ----------------- ---------------- --------------------- --------------- --------------- ------------------
               Chrome    Edge   Firefox   Internet Explorer   Opera   Safari   WebView Android   Chrome Android   Firefox for Android   Opera Android   Safari on IOS   Samsung Internet
  `disabled`   1         12     1         ≤6                  ≤12.1   ≤4       4.4               18               4                     ≤12.1           ≤3.2            1.0
:::

::: _table
               Desktop                                                         Mobile                                                                                   
  ------------ --------- ------ --------- ------------------- ------- -------- ----------------- ---------------- --------------------- --------------- --------------- ------------------
               Chrome    Edge   Firefox   Internet Explorer   Opera   Safari   WebView Android   Chrome Android   Firefox for Android   Opera Android   Safari on IOS   Samsung Internet
  `disabled`   1         12     1         Yes                 15      3        4.4               18               4                     14              2               1.0
:::

::: _table
               Desktop                                                         Mobile                                                                                   
  ------------ --------- ------ --------- ------------------- ------- -------- ----------------- ---------------- --------------------- --------------- --------------- ------------------
               Chrome    Edge   Firefox   Internet Explorer   Opera   Safari   WebView Android   Chrome Android   Firefox for Android   Opera Android   Safari on IOS   Samsung Internet
  `disabled`   1         12     1         Yes                 15      ≤4       4.4               18               4                     14              ≤3.2            1.0
:::

::: _table
               Desktop                                                         Mobile                                                                                   
  ------------ --------- ------ --------- ------------------- ------- -------- ----------------- ---------------- --------------------- --------------- --------------- ------------------
               Chrome    Edge   Firefox   Internet Explorer   Opera   Safari   WebView Android   Chrome Android   Firefox for Android   Opera Android   Safari on IOS   Samsung Internet
  `disabled`   1         12     1         8                   15      ≤4       4.4               18               4                     14              ≤3.2            1.0
:::

::: _table
               Desktop                                                         Mobile                                                                                   
  ------------ --------- ------ --------- ------------------- ------- -------- ----------------- ---------------- --------------------- --------------- --------------- ------------------
               Chrome    Edge   Firefox   Internet Explorer   Opera   Safari   WebView Android   Chrome Android   Firefox for Android   Opera Android   Safari on IOS   Samsung Internet
  `disabled`   1         12     1         5.5                 ≤12.1   1        4.4               18               4                     ≤12.1           1               1.0
:::

::: _table
  ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
               Desktop                                                                                                                                                                                                                                                        Mobile                                           
  ------------ --------- --------------------------------------------------------------------------- --------- --------------------------------------------------------------------------------------------------------------------------------------------- ------- -------- --------- --------- --------- --------- -------- ----------
               Chrome    Edge                                                                        Firefox   Internet Explorer                                                                                                                             Opera   Safari   WebView   Chrome    Firefox   Opera     Safari   Samsung
                                                                                                                                                                                                                                                                              Android   Android   for       Android   on IOS   Internet
                                                                                                                                                                                                                                                                                                  Android                      

  `disabled`   20        12                                                                          4         Yes                                                                                                                                           12      6        4.4       25        4         12        6        1.5
                                                                                                                                                                                                                                                                                                                               
                         Does not work with nested fieldsets. For example:                                     Not all form control descendants of a disabled fieldset are properly disabled in IE11; see IE [bug 817488: input\[type=\'file\'\] not                                                                           
                         `<fieldset disabled><fieldset><!--Still enabled--></fieldset></fieldset>`             disabled inside disabled fieldset](https://connect.microsoft.com/IE/feedbackdetail/view/817488) and IE [bug 962368: Can still edit                                                                              
                                                                                                               input\[type=\'text\'\] within                                                                                                                                                                                   
                                                                                                               fieldset\[disabled\]](https://connect.microsoft.com/IE/feedbackdetail/view/962368/can-still-edit-input-type-text-within-fieldset-disabled).                                                                     
  ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
:::

::: _table
               Desktop                                                         Mobile                                                                                   
  ------------ --------- ------ --------- ------------------- ------- -------- ----------------- ---------------- --------------------- --------------- --------------- ------------------
               Chrome    Edge   Firefox   Internet Explorer   Opera   Safari   WebView Android   Chrome Android   Firefox for Android   Opera Android   Safari on IOS   Samsung Internet
  `disabled`   1         12     1         Yes                 15      ≤4       4.4               18               4                     14              ≤3.2            1.0
:::

### html.elements.button.disabled

BCD tables only load in the browser with JavaScript enabled. Enable
JavaScript to view data.

### html.elements.fieldset.disabled

BCD tables only load in the browser with JavaScript enabled. Enable
JavaScript to view data.

### html.elements.input.disabled

BCD tables only load in the browser with JavaScript enabled. Enable
JavaScript to view data.

### html.elements.optgroup.disabled

BCD tables only load in the browser with JavaScript enabled. Enable
JavaScript to view data.

### html.elements.option.disabled

BCD tables only load in the browser with JavaScript enabled. Enable
JavaScript to view data.

### html.elements.select.disabled

BCD tables only load in the browser with JavaScript enabled. Enable
JavaScript to view data.

### html.elements.textarea.disabled

BCD tables only load in the browser with JavaScript enabled. Enable
JavaScript to view data.

## See also {#see_also}

::: section-content
-   [`:disabled`](https://developer.mozilla.org/en-US/docs/Web/CSS/:disabled)
    and
    [`:enabled`](https://developer.mozilla.org/en-US/docs/Web/CSS/:enabled)
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes/disabled](https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes/disabled){._attribution-link}
:::
