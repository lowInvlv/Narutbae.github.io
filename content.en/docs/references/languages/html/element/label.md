

# \<label\>: The Label element



::: section-content
The `<label>` [HTML](../index) element represents a caption for an item
in a user interface.
:::

## Try it {#try_it}

::: section-content
::: iframe
::: {.output-header .border-rounded-top}
#### HTML Demo: \<label\> {#html-demo-label .output-heading}

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
    <div class="preference">
      <label for="cheese">Do you like cheese?</label>
      <input type="checkbox" name="cheese" id="cheese" />
    

    <div class="preference">
      <label for="peas">Do you like peas?</label>
      <input type="checkbox" name="peas" id="peas" />
    
:::
:::

::: {#css-panel .section .hidden tabindex="0" role="tabpanel" aria-labelledby="css" aria-hidden="true"}
::: {#css-editor}
    .preference {
      display: flex;
      justify-content: space-between;
      width: 60%;
      margin: 0.5rem;
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

Associating a `<label>` with a form control, such as [`<input>`](input)
or [`<textarea>`](textarea) offers some major advantages:

-   The label text is not only visually associated with its
    corresponding text input; it is programmatically associated with it
    too. This means that, for example, a screen reader will read out the
    label when the user is focused on the form input, making it easier
    for an assistive technology user to understand what data should be
    entered.
-   When a user clicks or touches/taps a label, the browser passes the
    focus to its associated input (the resulting event is also raised
    for the input). That increased hit area for focusing the input
    provides an advantage to anyone trying to activate it --- including
    those using a touch-screen device.

To explicitly associate a `<label>` element with an `<input>` element,
you first need to add the `id` attribute to the `<input>` element. Next,
you add the `for` attribute to the `<label>` element, where the value of
`for` is the same as the `id` in the `<input>` element.

Alternatively, you can nest the `<input>` directly inside the `<label>`,
in which case the `for` and `id` attributes are not needed because the
association is implicit:

::: code-example
[html]{.language-name}

``` {signature="AhbN4XMmwVUdlXr/epl2ZoZtkoH6Z/oLycoxC/M9Cdk=" data-language="html"}
<label>
  Do you like peas?
  <input type="checkbox" name="peas" />
</label>
```
:::

The form control that a label is labeling is called the *labeled
control* of the label element. Multiple labels can be associated with
the same form control:

::: code-example
[html]{.language-name}

``` {signature="p/y8SAuSdhvsGlGe0d09441fqspimX5+IxypUUshDSs=" data-language="html"}
<label for="username">Enter your username:</label>
<input id="username" name="username" type="text" />
<label for="username">Forgot your username?</label>
```
:::

Elements that can be associated with a `<label>` element include
[`<button>`](button), [`<input>`](input) (except for `type="hidden"`),
[`<meter>`](meter), [`<output>`](output), [`<progress>`](progress),
[`<select>`](select) and [`<textarea>`](textarea).
:::

## Attributes

::: section-content
This element includes the [global attributes](../global_attributes).

[`for`](#for)

:   The value of the `for` attribute must be a single
    [`id`](../global_attributes#id) for a
    [labelable](../content_categories#labelable) form-related element in
    the same document as the `<label>` element. So, any given `label`
    element can be associated with only one form control.

    ::: {#sect1 .notecard .note}
    **Note:** To programmatically set the `for` attribute, use
    [`htmlFor`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLLabelElement/htmlFor).
    :::

    The first element in the document with an `id` attribute matching
    the value of the `for` attribute is the *labeled control* for this
    `label` element --- if the element with that `id` is actually a
    [labelable
    element](https://html.spec.whatwg.org/multipage/forms.html#category-label){target="_blank"}.
    If it is *not* a labelable element, then the `for` attribute has no
    effect. If there are other elements that also match the `id` value,
    later in the document, they are not considered.

    Multiple `label` elements can be given the same value for their
    `for` attribute; doing so causes the associated form control (the
    form control that `for` value references) to have multiple labels.

    ::: {#sect2 .notecard .note}
    **Note:** A `<label>` element can have both a `for` attribute and a
    contained control element, as long as the `for` attribute points to
    the contained control element.
    :::
:::

## Styling with CSS {#styling_with_css}

::: section-content
There are no special styling considerations for `<label>` elements ---
structurally they are simple inline elements, and so can be styled in
much the same way as a [`<span>`](span) or [`<a>`](a) element. You can
apply styling to them in any way you want, as long as you don\'t cause
the text to become difficult to read.
:::

## Examples

### Defining an implicit label {#defining_an_implicit_label}

::: section-content
::: code-example
[html]{.language-name}

``` {signature="zW3MmaUYroG77TWJSIxrKzZE4RkU5OJPPqJ/KgNIGD0=" data-language="html"}
<label>Click me <input type="text" /></label>
```
:::

::: {#sect3 .code-example}
::: iframe
:::
:::
:::

### Defining an explicit label with the \"for\" attribute {#defining_an_explicit_label_with_the_for_attribute}

::: section-content
::: code-example
[html]{.language-name}

``` {signature="FJoTP/pDVUzrBSJlEQZHU1RkCfAqfIAuPO9IejzEm24=" data-language="html"}
<label for="username">Click me to focus on the input field</label>
<input type="text" id="username" />
```
:::

::: {#sect4 .code-example}
::: iframe
:::
:::
:::

## Accessibility concerns {#accessibility_concerns}

### Interactive content {#interactive_content}

::: section-content
Don\'t place interactive elements such as [anchors](a) or
[buttons](button) inside a `label`. Doing so makes it difficult for
people to activate the form input associated with the `label`.

**Don\'t do this:**

::: code-example
[html]{.language-name}

``` {signature="epJVCPTN1DLAdZwplkXthSuVyiJoerAoyIqtRGfE8LA=" data-language="html"}
<label for="tac">
  <input id="tac" type="checkbox" name="terms-and-conditions" />
  I agree to the <a href="terms-and-conditions.html">Terms and Conditions</a>
</label>
```
:::

**Prefer this:**

::: code-example
[html]{.language-name}

``` {signature="gFBBDE3RMFHvSVSD+vt0qoHK+7QzrnZZXmtlFJ0wT6Q=" data-language="html"}
<label for="tac">
  <input id="tac" type="checkbox" name="terms-and-conditions" />
  I agree to the Terms and Conditions
</label>
<p>
  <a href="terms-and-conditions.html">Read our Terms and Conditions</a>
</p>
```
:::
:::

### Headings

::: section-content
Placing [heading elements](heading_elements) within a `<label>`
interferes with many kinds of assistive technology, because headings are
commonly used as [a navigation aid](heading_elements#navigation). If the
label\'s text needs to be adjusted visually, use CSS classes applied to
the `<label>` element instead.

If a [form](form), or a section of a form needs a title, use the
[`<legend>`](legend) element placed within a [`<fieldset>`](fieldset).

**Don\'t do this:**

::: code-example
[html]{.language-name}

``` {signature="Nncfx6JqBjmvXGwg6eqjkitN3xmJQx91CUrovtNpnoc=" data-language="html"}
<label for="your-name">
  <h3>Your name</h3>
  <input id="your-name" name="your-name" type="text" />
</label>
```
:::

**Prefer this:**

::: code-example
[html]{.language-name}

``` {signature="FXaFdhbRkL6arJ2NGvxQFIb+GBqLOh7pk37rLHUiiCI=" data-language="html"}
<label class="large-label" for="your-name">
  Your name
  <input id="your-name" name="your-name" type="text" />
</label>
```
:::
:::

### Buttons

::: section-content
An [`<input>`](input) element with a `type="button"` declaration and a
valid `value` attribute does not need a label associated with it. Doing
so may actually interfere with how assistive technology parses the
button input. The same applies for the [`<button>`](button) element.
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
href="../content_categories#phrasing_content">phrasing content</a>, <a
href="../content_categories#interactive_content">interactive
content</a>, <a
href="../content_categories#form-associated_content">form-associated
element</a>, palpable content.</td>
</tr>
<tr class="even">
<th scope="row">Permitted content</th>
<td><a href="../content_categories#phrasing_content">Phrasing
content</a>, but no descendant <code>label</code> elements. No <a
href="../content_categories#labelable">labelable</a> elements other than
the labeled control are allowed.</td>
</tr>
<tr class="odd">
<th scope="row">Tag omission</th>
<td>None, both the starting and ending tag are mandatory.</td>
</tr>
<tr class="even">
<th scope="row">Permitted parents</th>
<td>Any element that accepts <a
href="../content_categories#phrasing_content">phrasing content</a>.</td>
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
href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLLabelElement"><code>HTMLLabelElement</code></a></td>
</tr>
</tbody>
</table>

</figure>
:::

## Specifications

::: _table
  --------------------------------------------------------------------------------------------------
  Specification
  --------------------------------------------------------------------------------------------------
  [HTML Standard\
  [\#
  the-label-element]{.small}](https://html.spec.whatwg.org/multipage/forms.html#the-label-element)

  --------------------------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
            Desktop                                                         Mobile                                                                                   
  --------- --------- ------ --------- ------------------- ------- -------- ----------------- ---------------- --------------------- --------------- --------------- ------------------
            Chrome    Edge   Firefox   Internet Explorer   Opera   Safari   WebView Android   Chrome Android   Firefox for Android   Opera Android   Safari on IOS   Samsung Internet
  `label`   1         12     1         Yes                 15      ≤4       4.4               18               4                     14              ≤3.2            1.0
  `for`     1         12     1         Yes                 15      ≤4       4.4               18               4                     14              ≤3.2            1.0
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Element/label](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/label){._attribution-link}
:::
