

# HTML attribute: multiple



::: section-content
The Boolean `multiple` attribute, if set, means the form control accepts
one or more values. Valid for the [email](../element/input/email) and
[file](../element/input/file) input types and the
[`<select>`](../element/select), the manner by which the user opts for
multiple values depends on the form control.
:::

## Try it {#try_it}

::: section-content
::: iframe
::: {.output-header .border-rounded-top}
#### HTML Demo: multiple {#html-demo-multiple .output-heading}

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
    <label for="recipients">Where should we send the receipt?</label>
    <input name="recipients" type="email" multiple />

    <label for="shakes">Which shakes would you like to order?</label>
    <select name="shakes" multiple>
      <option>Vanilla Shake</option>
      <option>Strawberry Shake</option>
      <option>Chocolate Shake</option>
    </select>

    <label for="payment">How would you like to pay?</label>
    <select name="payment">
      <option>Credit card</option>
      <option>Bank Transfer</option>
    </select>
:::
:::

::: {#css-panel .section .hidden tabindex="0" role="tabpanel" aria-labelledby="css" aria-hidden="true"}
::: {#css-editor}
    label {
      display: block;
      margin-top: 1em;
    }

    input,
    select {
      width: 100%;
    }

    input:invalid {
      background-color: lightpink;
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
Depending on the type, the form control may have a different appearance
if the `multiple` attribute is set. For the file input type, the native
messaging the browser provides differs. In Firefox, the file input reads
\"No files selected\" when the attribute is present and \"No file
selected\" when it is not. Most browsers display a scrolling list box
for a [`<select>`](../element/select) control with the `multiple`
attribute set and a single line dropdown when the attribute is omitted.
The [email](../element/input/email) input displays the same whether or
not the `multiple` attribute is included, but will match the
[`:invalid`](https://developer.mozilla.org/en-US/docs/Web/CSS/:invalid)
pseudo-class if more than one comma-separated email address is included
if the attribute is not present.

When `multiple` is set on the [email](../element/input/email) input
type, the user can include zero (if not also [`required`](required)),
one or more comma-separated email addresses.

::: code-example
[html]{.language-name}

``` {signature="QowIHGkNqAEjNj5jyMQlwp5DksSgSSL0ducELPGZ2RI=" data-language="html"}
<input type="email" multiple name="emails" id="emails" />
```
:::

If and only if the `multiple` attribute is specified, the value can be a
list of properly-formed comma-separated email addresses. Any trailing
and leading whitespace is removed from each address in the list.

When `multiple` is set on the [file](../element/input/file) input type,
the user can select one or more files. The user can choose multiple
files from the file picker in any way that their chosen platform allows
(e.g. by holding down [Shift]{.kbd} or [Control]{.kbd}, and then
clicking).

::: code-example
[html]{.language-name}

``` {signature="7pVAeg/iHHqeuZ2FApeNxEZCWcuo9y8UV5gYehGqdX8=" data-language="html"}
<input type="file" multiple name="uploads" id="uploads" />
```
:::

When the attribute is omitted, the user can only select a single file
per `<input>`.

The `multiple` attribute on the [`<select>`](../element/select) element
represents a control for selecting zero or more options from the list of
options. Otherwise, the [`<select>`](../element/select) element
represents a control for selecting a single
[`<option>`](../element/option) from the list of options.

::: code-example
[html]{.language-name}

``` {signature="MJvJ40YWZuMl7QG2AycZ95PtrNyveY9xoun2UN1Qnik=" data-language="html"}
<select multiple name="dwarfs" id="dwarfs">
  <option>Grumpy</option>
  <option>Happy</option>
  <option>Sleepy</option>
  <option>Bashful</option>
  <option>Sneezy</option>
  <option>Dopey</option>
  <option>Doc</option>
</select>
```
:::

When `multiple` is specified, most browsers will show a scrolling list
box instead of a single line dropdown.
:::

## Accessibility concerns {#accessibility_concerns}

::: section-content
Provide instructions to help users understand how to complete the form
and use individual form controls. Indicate any required and optional
input, data formats, and other relevant information. When using the
`multiple` attribute, inform the user that multiple values are allowed
and provide directions on how to provide multiple values, such as
\"separate email addresses with a comma.\"

Setting `size="1"` on a multiple select can make it appear as a single
select in some browsers, but then it doesn\'t expand on focus, harming
usability. Don\'t do that. If you do change the appearance of a select,
and even if you don\'t, make sure to inform the user that more than one
option can be selected by another method.
:::

## Examples

### email input {#email_input}

::: section-content
::: code-example
[html]{.language-name}

``` {signature="4EZ7EWsBKMVDrj29KMx6Q7S1iMZu9kUt2xrGNMS/Gh4=" data-language="html"}
<label for="emails">Who do you want to email?</label>
<input
  type="email"
  multiple
  name="emails"
  id="emails"
  list="dwarf-emails"
  required
  size="64" />

<datalist id="dwarf-emails">
  <option value="grumpy@woodworkers.com">Grumpy</option>
  <option value="happy@woodworkers.com">Happy</option>
  <option value="sleepy@woodworkers.com">Sleepy</option>
  <option value="bashful@woodworkers.com">Bashful</option>
  <option value="sneezy@woodworkers.com">Sneezy</option>
  <option value="dopey@woodworkers.com">Dopey</option>
  <option value="doc@woodworkers.com">Doc</option>
</datalist>
```
:::

If and only if the `multiple` attribute is specified, the value can be a
list of properly-formed comma-separated email addresses. Any trailing
and leading whitespace is removed from each address in the list. If the
[`required`](required) attribute is present, at least one email address
is required.

Some browsers support the appearance of the
[`list`](https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes/list){.page-not-created}
of options from the associated [`<datalist>`](../element/datalist) for
subsequent email addresses when `multiple` is present. Others do not.

::: {#sect1 .code-example}
::: iframe
:::
:::
:::

### file input {#file_input}

::: section-content
When `multiple` is set on the [file](../element/input/file) input type,
the user can select one or more files:

::: code-example
[html]{.language-name}

``` {signature="flenzpLLVWJHxnY36hMSf9XVAvMa1djslUqW8vxU/h8=" data-language="html"}
<form method="post" enctype="multipart/form-data">
  <p>
    <label for="uploads"> Choose the images you want to upload: </label>
    <input
      type="file"
      id="uploads"
      name="uploads"
      accept=".jpg, .jpeg, .png, .svg, .gif"
      multiple />
  </p>
  <p>
    <label for="text">Pick a text file to upload: </label>
    <input type="file" id="text" name="text" accept=".txt" />
  </p>
  <p>
    <input type="submit" value="Submit" />
  </p>
</form>
```
:::

::: {#sect2 .code-example}
::: iframe
:::
:::

Note the difference in appearance between the example with `multiple`
set and the other `file` input without.

When the form is submitted, had we used
[`method="get"`](../element/form) each selected file\'s name would have
been added to URL parameters as`?uploads=img1.jpg&uploads=img2.svg`.
However, since we are submitting
[multipart](https://developer.mozilla.org/en-US/docs/Web/API/XMLHttpRequest/multipart){.page-not-created}
form data, we much use post. See the [`<form>`](../element/form) element
and [sending form
data](https://developer.mozilla.org/en-US/docs/Learn/Forms/Sending_and_retrieving_form_data#the_method_attribute)
for more information.
:::

### select

::: section-content
The `multiple` attribute on the [`<select>`](../element/select) element
represents a control for selecting zero or more options from the list of
options. Otherwise, the [`<select>`](../element/select) element
represents a control for selecting a single
[`<option>`](../element/option) from the list of options. The control
generally has a different appearance based on the presence of the
multiple attribute, with most browsers displaying a scrolling list box
instead of a single line dropdown when the attribute is present.

::: code-example
[html]{.language-name}

``` {signature="WBZK5MxF9qVM8MmECfKYaPM6QQ7JASifA23YPkwUkt0=" data-language="html"}
<form method="get" action="#">
  <p>
    <label for="dwarfs">Select the dwarf woodsman you like:</label>
    <select multiple name="dwarfs" id="dwarfs">
      <option>grumpy@woodworkers.com</option>
      <option>happy@woodworkers.com</option>
      <option>sleepy@woodworkers.com</option>
      <option>bashful@woodworkers.com</option>
      <option>sneezy@woodworkers.com</option>
      <option>dopey@woodworkers.com</option>
      <option>doc@woodworkers.com</option>
    </select>
  </p>
  <p>
    <label for="favoriteOnly">Select your favorite:</label>
    <select name="favoriteOnly" id="favoriteOnly">
      <option>grumpy@woodworkers.com</option>
      <option>happy@woodworkers.com</option>
      <option>sleepy@woodworkers.com</option>
      <option>bashful@woodworkers.com</option>
      <option>sneezy@woodworkers.com</option>
      <option>dopey@woodworkers.com</option>
      <option>doc@woodworkers.com</option>
    </select>
  </p>
  <p>
    <input type="submit" value="Submit" />
  </p>
</form>
```
:::

::: {#sect3 .code-example}
::: iframe
:::
:::

Note the difference in appearance between the two form controls.

::: code-example
[css]{.language-name}

``` {signature="O6N6BoahQy8qGs8UrZIrX7dv1pQPKQx9/f9KyMcQeD8=" data-language="css"}
/* uncomment this CSS to make the multiple the same height as the single */

/*
select[multiple] {
  height: 1.5em;
  vertical-align: top;
}
select[multiple]:focus,
select[multiple]:active {
  height: auto;
}
*/
```
:::

There are a few ways to select multiple options in a `<select>` element
with a `multiple` attribute. Depending on the operating system, mouse
users can hold the [Ctrl]{.kbd}, [Command]{.kbd}, or [Shift]{.kbd} keys
and then click multiple options to select/deselect them. Keyboard users
can select multiple contiguous items by focusing on the `<select>`
element, selecting an item at the top or bottom of the range they want
to select using the [Up]{.kbd} and [Down]{.kbd} cursor keys to go up and
down the options. The selection of non-contiguous is not as
well-supported: items should be able to be selected and deselected by
pressing [Space]{.kbd}, but support varies between browsers.
:::

## Specifications

::: _table
  ------------------------------------------------------------------------------------------------------
  Specification
  ------------------------------------------------------------------------------------------------------
  [HTML Standard\
  [\#
  attr-input-multiple]{.small}](https://html.spec.whatwg.org/multipage/input.html#attr-input-multiple)

  ------------------------------------------------------------------------------------------------------
:::

## See also {#see_also}

::: section-content
-   [`<input>`](../element/input)
-   [`<select>`](../element/select)
-   [Allowing multiple email
    addresses](../element/input/email#allowing_multiple_email_addresses)
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes/multiple](https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes/multiple){._attribution-link}
:::
