

# \<input type=\"text\"\>



::: section-content
[`<input>`](../input) elements of type `text` create basic single-line
text fields.
:::

## Try it {#try_it}

::: section-content
::: iframe
::: {.output-header .border-rounded-top}
#### HTML Demo: \<input type=\"text\"\> {#html-demo-input-typetext .output-heading}

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
    <label for="name">Name (4 to 8 characters):</label>

    <input type="text" id="name" name="name" required minlength="4" maxlength="8" size="10" />
:::
:::

::: {#css-panel .section .hidden tabindex="0" role="tabpanel" aria-labelledby="css" aria-hidden="true"}
::: {#css-editor}
    label {
      display: block;
      font:
        1rem 'Fira Sans',
        sans-serif;
    }

    input,
    label {
      margin: 0.4rem 0;
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

## Value

::: section-content
The [`value`](../input#value) attribute is a string that contains the
current value of the text entered into the text field. You can retrieve
this using the
[`HTMLInputElement`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLInputElement)
`value` property in JavaScript.

::: code-example
[js]{.language-name}

``` {signature="ciqYD73jKCiYcivNNXrD0P6XGtokku4U/WyEAzlzXWk=" data-language="js"}
let theText = myTextInput.value;
```
:::

If no validation constraints are in place for the input (see
[Validation](#validation) for more details), the value may be an empty
string (`""`).
:::

## Additional attributes {#additional_attributes}

::: section-content
In addition to the attributes that operate on all [`<input>`](../input)
elements regardless of their type, text inputs support the following
attributes.
:::

### `list`

::: section-content
The values of the list attribute is the
[`id`](https://developer.mozilla.org/en-US/docs/Web/API/Element/id) of a
[`<datalist>`](../datalist) element located in the same document. The
[`<datalist>`](../datalist) provides a list of predefined values to
suggest to the user for this input. Any values in the list that are not
compatible with the [`type`](../input#type) are not included in the
suggested options. The values provided are suggestions, not
requirements: users can select from this predefined list or provide a
different value.
:::

### `maxlength`

::: section-content
The maximum string length (measured in UTF-16 code units) that the user
can enter into the `text` input. This must be an integer value of 0 or
higher. If no `maxlength` is specified, or an invalid value is
specified, the `text` input has no maximum length. This value must also
be greater than or equal to the value of `minlength`.

The input will fail [constraint validation](../../constraint_validation)
if the length of the text value of the field is greater than `maxlength`
UTF-16 code units long. Constraint validation is only applied when the
value is changed by the user.
:::

### `minlength`

::: section-content
The minimum string length (measured in UTF-16 code units) that the user
can enter into the `text` input. This must be a non-negative integer
value smaller than or equal to the value specified by `maxlength`. If no
`minlength` is specified, or an invalid value is specified, the `text`
input has no minimum length.

The input will fail [constraint validation](../../constraint_validation)
if the length of the text entered into the field is fewer than
`minlength` UTF-16 code units long. Constraint validation is only
applied when the value is changed by the user.
:::

### `pattern`

::: section-content
The `pattern` attribute, when specified, is a regular expression that
the input\'s [`value`](../input#value) must match for the value to pass
[constraint validation](../../constraint_validation). It must be a valid
JavaScript regular expression, as used by the
[`RegExp`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/RegExp)
type, and as documented in our [guide on regular
expressions](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Regular_expressions);
the `'u'` flag is specified when compiling the regular expression so
that the pattern is treated as a sequence of Unicode code points,
instead of as
[ASCII](https://developer.mozilla.org/en-US/docs/Glossary/ASCII). No
forward slashes should be specified around the pattern text.

If the specified pattern is not specified or is invalid, no regular
expression is applied and this attribute is ignored completely.

::: {#sect1 .notecard .note}
**Note:** Use the [`title`](../input#title) attribute to specify text
that most browsers will display as a tooltip to explain what the
requirements are to match the pattern. You should also include other
explanatory text nearby.
:::

See [Specifying a pattern](#specifying_a_pattern) for further details
and an example.
:::

### `placeholder`

::: section-content
The `placeholder` attribute is a string that provides a brief hint to
the user as to what kind of information is expected in the field. It
should be a word or short phrase that demonstrates the expected type of
data, rather than an explanatory message. The text *must not* include
carriage returns or line feeds.

If the control\'s content has one directionality
([LTR](https://developer.mozilla.org/en-US/docs/Glossary/LTR) or
[RTL](https://developer.mozilla.org/en-US/docs/Glossary/RTL)) but needs
to present the placeholder in the opposite directionality, you can use
Unicode bidirectional algorithm formatting characters to override
directionality within the placeholder; see [How to use Unicode controls
for bidi
text](https://www.w3.org/International/questions/qa-bidi-unicode-controls){target="_blank"}
for more information.

::: {#sect2 .notecard .note}
**Note:** Avoid using the `placeholder` attribute if you can. It is not
as semantically useful as other ways to explain your form, and can cause
unexpected technical issues with your content. See [`<input>`
accessibility concerns](../input#accessibility_concerns) for more
information.
:::
:::

### `readonly`

::: section-content
A Boolean attribute which, if present, means this field cannot be edited
by the user. Its `value` can, however, still be changed by JavaScript
code directly setting the
[`HTMLInputElement`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLInputElement)
`value` property.

::: {#sect3 .notecard .note}
**Note:** Because a read-only field cannot have a value, `required` does
not have any effect on inputs with the `readonly` attribute also
specified.
:::
:::

### `size`

::: section-content
The `size` attribute is a numeric value indicating how many characters
wide the input field should be. The value must be a number greater than
zero, and the default value is 20. Since character widths vary, this may
or may not be exact and should not be relied upon to be so; the
resulting input may be narrower or wider than the specified number of
characters, depending on the characters and the font
([`font`](https://developer.mozilla.org/en-US/docs/Web/CSS/font)
settings in use).

This does *not* set a limit on how many characters the user can enter
into the field. It only specifies approximately how many can be seen at
a time. To set an upper limit on the length of the input data, use the
[`maxlength`](#maxlength) attribute.
:::

### `spellcheck`

::: section-content
`spellcheck` is a global attribute which is used to indicate whether to
enable spell checking for an element. It can be used on any editable
content, but here we consider specifics related to the use of
`spellcheck` on [`<input>`](../input) elements. The permitted values for
`spellcheck` are:

[`false`](#false)

:   Disable spell checking for this element.

[`true`](#true)

:   Enable spell checking for this element.

[`""`](#sect4) (empty string) or no value

:   Follow the element\'s default behavior for spell checking. This may
    be based upon a parent\'s `spellcheck` setting or other factors.

An input field can have spell checking enabled if it doesn\'t have the
[readonly](#readonly) attribute set and is not disabled.

The value returned by reading `spellcheck` may not reflect the actual
state of spell checking within a control, if the [user
agent\'s](https://developer.mozilla.org/en-US/docs/Glossary/User_agent)
preferences override the setting.
:::

## Non-standard attributes {#non-standard_attributes}

::: section-content
The following non-standard attributes are also available on some
browsers. As a general rule, you should avoid using them unless it
can\'t be helped.
:::

### `autocorrect`

::: section-content
A Safari extension, the `autocorrect` attribute is a string which
indicates whether to activate automatic correction while the user is
editing this field. Permitted values are:

[`on`](#on)

:   Enable automatic correction of typos, as well as processing of text
    substitutions if any are configured.

[`off`](#off)

:   Disable automatic correction and text substitutions.
:::

### `mozactionhint` [Deprecated]{.visually-hidden} {#mozactionhint_deprecated}

::: section-content
A Mozilla extension, which provides a hint as to what sort of action
will be taken if the user presses the [Enter]{.kbd} or [Return]{.kbd}
key while editing the field.

**Deprecated: Use [`enterkeyhint`](../../global_attributes#enterkeyhint)
instead.**
:::

## Using text inputs {#using_text_inputs}

::: section-content
`<input>` elements of type `text` create basic, single-line inputs. You
should use them anywhere you want the user to enter a single-line value
and there isn\'t a more specific input type available for collecting
that value (for example, if it\'s a [date](datetime-local), [URL](url),
[email](email), or [search term](search), you\'ve got better options
available).
:::

### Basic example {#basic_example}

::: section-content
::: code-example
[html]{.language-name}

``` {signature="2mZtMk9LkXhKuqt6EKqNkwldq5HVLGZCb2FyAXrE4kg=" data-language="html"}
<form>
  
    <label for="uname">Choose a username: </label>
    <input type="text" id="uname" name="name" />
  
  
    <button>Submit</button>
  
</form>
```
:::

This renders like so:

::: {#sect5 .code-example}
::: iframe
:::
:::

When submitted, the data name/value pair sent to the server will be
`name=Chris` (if \"Chris\" was entered as the input value before
submission). You must remember to include [`name`](../input#name)
attribute on the [`<input>`](../input) element, otherwise the text
field\'s value won\'t be included with the submitted data.
:::

### Setting placeholders {#setting_placeholders}

::: section-content
You can provide a useful placeholder inside your text input that can
provide a hint as to what to enter by including using the
[`placeholder`](../input#placeholder) attribute. Look at the following
example:

::: code-example
[html]{.language-name}

``` {signature="S/EmtmL79parGRMKmXC0hVBIZERD2CwLpuZ7t6NYz7Q=" data-language="html"}
<form>
  
    <label for="uname">Choose a username: </label>
    <input
      type="text"
      id="uname"
      name="name"
      placeholder="Lower case, all one word" />
  
  
    <button>Submit</button>
  
</form>
```
:::

You can see how the placeholder is rendered below:

::: {#sect6 .code-example}
::: iframe
:::
:::

The placeholder is typically rendered in a lighter color than the
element\'s foreground color, and automatically vanishes when the user
begins to enter text into the field (or whenever the field has a value
set programmatically by setting its `value` attribute).
:::

### Physical input element size {#physical_input_element_size}

::: section-content
The physical size of the input box can be controlled using the
[`size`](../input#size) attribute. With it, you can specify the number
of characters the text input can display at a time. This affects the
width of the element, letting you specify the width in terms of
characters rather than pixels. In this example, for instance, the input
is 30 characters wide:

::: code-example
[html]{.language-name}

``` {signature="yTxH/vBGby2kUnckQuqFQoqNwLkOu9V1F8tApy+0WCU=" data-language="html"}
<form>
  
    <label for="uname">Choose a username: </label>
    <input
      type="text"
      id="uname"
      name="name"
      placeholder="Lower case, all one word"
      size="30" />
  
  
    <button>Submit</button>
  
</form>
```
:::

::: {#sect7 .code-example}
::: iframe
:::
:::
:::

## Validation

::: section-content
`<input>` elements of type `text` have no automatic validation applied
to them (since a basic text input needs to be capable of accepting any
arbitrary string), but there are some client-side validation options
available, which we\'ll discuss below.

::: {#sect8 .notecard .note}
**Note:** HTML form validation is *not* a substitute for server-scripts
that ensure the entered data is in the proper format. It\'s far too easy
for someone to make adjustments to the HTML that allow them to bypass
the validation, or to remove it entirely. It\'s also possible for
someone to bypass your HTML entirely and submit the data directly to
your server. If your server-side code fails to validate the data it
receives, disaster could strike when improperly-formatted data (or data
which is too large, is of the wrong type, and so forth) is entered into
your database.
:::
:::

### A note on styling {#a_note_on_styling}

::: section-content
There are useful pseudo-classes available for styling form elements to
help the user see when their values are valid or invalid. These are
[`:valid`](https://developer.mozilla.org/en-US/docs/Web/CSS/:valid) and
[`:invalid`](https://developer.mozilla.org/en-US/docs/Web/CSS/:invalid).
In this section, we\'ll use the following CSS, which will place a check
(tick) mark next to inputs containing valid values, and a cross (X) next
to inputs containing invalid values.

::: code-example
[css]{.language-name}

``` {signature="uCANFVtNFhqGK3c0avL/HKgAZEQ0bMn5S7/Ox57sQp4=" data-language="css"}
div {
  margin-bottom: 10px;
  position: relative;
}

input + span {
  padding-right: 30px;
}

input:invalid + span::after {
  position: absolute;
  content: "✖";
  padding-left: 5px;
}

input:valid + span::after {
  position: absolute;
  content: "✓";
  padding-left: 5px;
}
```
:::

The technique also requires a [`<span>`](../span) element to be placed
after the form element, which acts as a holder for the icons. This was
necessary because some input types on some browsers don\'t display icons
placed directly after them very well.
:::

### Making input required {#making_input_required}

::: section-content
You can use the [`required`](../input#required) attribute as an easy way
of making entering a value required before form submission is allowed:

::: code-example
[html]{.language-name}

``` {signature="+S2Y9Oiwz+5cHZkwtWQrQ93IT4gaY1d38vYQOaKu64w=" data-language="html"}
<form>
  
    <label for="uname">Choose a username: </label>
    <input type="text" id="uname" name="name" required />
    <span class="validity"></span>
  
  
    <button>Submit</button>
  
</form>
```
:::

This renders like so:

::: {#sect9 .code-example}
::: iframe
:::
:::

If you try to submit the form with no search term entered into it, the
browser will show an error message.
:::

### Input value length {#input_value_length}

::: section-content
You can specify a minimum length (in characters) for the entered value
using the [`minlength`](../input#minlength) attribute; similarly, use
[`maxlength`](../input#maxlength) to set the maximum length of the
entered value, in characters.

The example below requires that the entered value be 4--8 characters in
length.

::: code-example
[html]{.language-name}

``` {signature="FiOzCvAMSBGpKiMP6qVQKJMdnwJG7TUvH148AhXpq1w=" data-language="html"}
<form>
  
    <label for="uname">Choose a username: </label>
    <input
      type="text"
      id="uname"
      name="name"
      required
      size="10"
      placeholder="Username"
      minlength="4"
      maxlength="8" />
    <span class="validity"></span>
  
  
    <button>Submit</button>
  
</form>
```
:::

This renders like so:

::: {#sect10 .code-example}
::: iframe
:::
:::

If you try to submit the form with less than 4 characters, you\'ll be
given an appropriate error message (which differs between browsers). If
you try to enter more than 8 characters, the browser won\'t let you.

::: {#sect11 .notecard .note}
**Note:** If you specify a `minlength` but do not specify `required`,
the input is considered valid, since the user is not required to specify
a value.
:::
:::

### Specifying a pattern {#specifying_a_pattern}

::: section-content
You can use the [`pattern`](../input#pattern) attribute to specify a
regular expression that the inputted value must match in order to be
considered valid (see [Validating against a regular
expression](https://developer.mozilla.org/en-US/docs/Learn/Forms/Form_validation#validating_against_a_regular_expression)
for a simple crash course on using regular expressions to validate
inputs).

The example below restricts the value to 4-8 characters and requires
that it contain only lower-case letters.

::: code-example
[html]{.language-name}

``` {signature="QEV1+Nw6ATDQfdA5yWG5lQ2afw/l3/BUZaEzidb2CSE=" data-language="html"}
<form>
  
    <label for="uname">Choose a username: </label>
    <input
      type="text"
      id="uname"
      name="name"
      required
      size="45"
      pattern="[a-z]{4,8}" />
    <span class="validity"></span>
    <p>Usernames must be lowercase and 4-8 characters in length.</p>
  
  
    <button>Submit</button>
  
</form>
```
:::

This renders like so:

::: {#sect12 .code-example}
::: iframe
:::
:::
:::

## Examples

::: section-content
You can see good examples of text inputs used in context in our [Your
first HTML
form](https://developer.mozilla.org/en-US/docs/Learn/Forms/Your_first_form)
and [How to structure an HTML
form](https://developer.mozilla.org/en-US/docs/Learn/Forms/How_to_structure_a_web_form)
articles.
:::

## Technical summary {#technical_summary}

::: section-content
<figure class="table-container">
<div class="_table">
<table class="properties">
<tbody>
<tr class="odd">
<td><strong><a href="#value">Value</a></strong></td>
<td>A string representing the text contained in the text field.</td>
<td></td>
</tr>
<tr class="even">
<td><strong>Events</strong></td>
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/change_event"><code>change</code></a>
and <a
href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/input_event"><code>input</code></a></td>
<td></td>
</tr>
<tr class="odd">
<td><strong>Supported Common Attributes</strong></td>
<td><a href="../input#autocomplete"><code>autocomplete</code></a>, <a
href="../input#list"><code>list</code></a>, <a
href="../input#maxlength"><code>maxlength</code></a>, <a
href="../input#minlength"><code>minlength</code></a>, <a
href="../input#pattern"><code>pattern</code></a>, <a
href="../input#placeholder"><code>placeholder</code></a>, <a
href="../input#readonly"><code>readonly</code></a>, <a
href="../input#required"><code>required</code></a> and <a
href="../input#size"><code>size</code></a></td>
<td></td>
</tr>
<tr class="even">
<td><strong>IDL attributes</strong></td>
<td><a href="../input#list"><code>list</code></a>,
<code>value</code></td>
<td></td>
</tr>
<tr class="odd">
<td><strong>DOM interface</strong></td>
<td><p><a
href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLInputElement"><code>HTMLInputElement</code></a></p></td>
<td></td>
</tr>
<tr class="even">
<td><strong>Methods</strong></td>
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLInputElement/select"><code>select()</code></a>,
<a
href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLInputElement/setRangeText"><code>setRangeText()</code></a>
and <a
href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLInputElement/setSelectionRange"><code>setSelectionRange()</code></a>.</td>
<td></td>
</tr>
<tr class="odd">
<td><strong>Implicit ARIA Role</strong></td>
<td>with no <code>list</code> attribute: <a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/textbox_role"><code>textbox</code></a></td>
<td>with <code>list</code> attribute: <a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/combobox_role"><code>combobox</code></a></td>
</tr>
</tbody>
</table>

</figure>
:::

## Specifications

::: _table
  --------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  Specification
  --------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  [HTML Standard\
  [\#
  text-(type=text)-state-and-search-state-(type=search)]{.small}](https://html.spec.whatwg.org/multipage/input.html#text-(type=text)-state-and-search-state-(type=search))

  --------------------------------------------------------------------------------------------------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
           Desktop                                                         Mobile                                                                                   
  -------- --------- ------ --------- ------------------- ------- -------- ----------------- ---------------- --------------------- --------------- --------------- ------------------
           Chrome    Edge   Firefox   Internet Explorer   Opera   Safari   WebView Android   Chrome Android   Firefox for Android   Opera Android   Safari on IOS   Samsung Internet
  `text`   1         12     1         Yes                 15      1        4.4               18               4                     14              1               1.0
:::

## See also {#see_also}

::: section-content
-   [HTML Forms](https://developer.mozilla.org/en-US/docs/Learn/Forms)
-   [`<input>`](../input) and the
    [`HTMLInputElement`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLInputElement)
    interface it\'s based upon.
-   [`<input type="search">`](search)
-   [`<textarea>`](../textarea): Multi-line text input
-   [Compatibility of CSS
    properties](https://developer.mozilla.org/en-US/docs/Learn/Forms/Property_compatibility_table_for_form_controls)
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/text](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/text){._attribution-link}
:::
