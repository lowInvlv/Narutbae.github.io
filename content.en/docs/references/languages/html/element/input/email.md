

# \<input type=\"email\"\>



::: section-content
[`<input>`](../input) elements of type `email` are used to let the user
enter and edit an email address, or, if the
[`multiple`](../../attributes/multiple) attribute is specified, a list
of email addresses.
:::

## Try it {#try_it}

::: section-content
::: iframe
::: {.output-header .border-rounded-top}
#### HTML Demo: \<input type=\"email\"\> {#html-demo-input-typeemail .output-heading}

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
    <label for="email">Enter your globex.com email:</label>

    <input type="email" id="email" pattern=".+@globex\.com" size="30" required />
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

The input value is automatically validated to ensure that it\'s either
empty or a properly-formatted email address (or list of addresses)
before the form can be submitted. The
[`:valid`](https://developer.mozilla.org/en-US/docs/Web/CSS/:valid) and
[`:invalid`](https://developer.mozilla.org/en-US/docs/Web/CSS/:invalid)
CSS pseudo-classes are automatically applied as appropriate to visually
denote whether the current value of the field is a valid email address
or not.
:::

## Value

::: section-content
The [`<input>`](../input) element\'s [`value`](../input#value) attribute
contains a string which is automatically validated as conforming to
email syntax. More specifically, there are three possible value formats
that will pass validation:

1.  An empty string (\"\") indicating that the user did not enter a
    value or that the value was removed.
2.  A single properly-formed email address. This doesn\'t necessarily
    mean the email address exists, but it is at least formatted
    correctly. In simple terms, this means `username@domain` or
    `username@domain.tld`. There\'s more to it than that, of course; see
    [Validation](#validation) for a [regular
    expression](https://developer.mozilla.org/en-US/docs/Glossary/Regular_expression)
    that matches the email address validation algorithm.
3.  If and only if the [`multiple`](../input#multiple) attribute is
    specified, the value can be a list of properly-formed
    comma-separated email addresses. Any trailing and leading whitespace
    is removed from each address in the list.

See [Validation](#validation) for details on how email addresses are
validated to ensure that they\'re formatted properly.
:::

## Additional attributes {#additional_attributes}

::: section-content
In addition to the attributes that operate on all [`<input>`](../input)
elements regardless of their type, `email` inputs support the following
attributes.
:::

### list

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

### maxlength

::: section-content
The maximum string length (measured in UTF-16 code units) that the user
can enter into the `email` input. This must be an integer value of 0 or
higher. If no `maxlength` is specified, or an invalid value is
specified, the `email` input has no maximum length. This value must also
be greater than or equal to the value of `minlength`.

The input will fail [constraint validation](../../constraint_validation)
if the length of the text value of the field is greater than `maxlength`
UTF-16 code units long. Constraint validation is only applied when the
value is changed by the user.
:::

### minlength

::: section-content
The minimum string length (measured in UTF-16 code units) that the user
can enter into the `email` input. This must be a non-negative integer
value smaller than or equal to the value specified by `maxlength`. If no
`minlength` is specified, or an invalid value is specified, the `email`
input has no minimum length.

The input will fail [constraint validation](../../constraint_validation)
if the length of the text entered into the field is fewer than
`minlength` UTF-16 code units long. Constraint validation is only
applied when the value is changed by the user.
:::

### multiple

::: section-content
A Boolean attribute which, if present, indicates that the user can enter
a list of multiple email addresses, separated by commas and, optionally,
whitespace characters. See [Allowing multiple email
addresses](#allowing_multiple_email_addresses) for an example, or [HTML
attribute: multiple](../../attributes/multiple) for more details.

::: {#sect1 .notecard .note}
**Note:** Normally, if you specify the [`required`](../input#required)
attribute, the user must enter a valid email address for the field to be
considered valid. However, if you add the `multiple` attribute, a list
of zero email addresses (an empty string, or one which is entirely
whitespace) is a valid value. In other words, the user does not have to
enter even one email address when `multiple` is specified, regardless of
the value of `required`.
:::
:::

### pattern

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

::: {#sect2 .notecard .note}
**Note:** Use the [`title`](../input#title) attribute to specify text
that most browsers will display as a tooltip to explain what the
requirements are to match the pattern. You should also include other
explanatory text nearby.
:::

See the section [Pattern validation](#pattern_validation) for details
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

::: {#sect3 .notecard .note}
**Note:** Avoid using the `placeholder` attribute if you can. It is not
as semantically useful as other ways to explain your form, and can cause
unexpected technical issues with your content. See [`<input>`
labels](../input#labels) for more information.
:::
:::

### `readonly`

::: section-content
A Boolean attribute which, if present, means this field cannot be edited
by the user. Its `value` can, however, still be changed by JavaScript
code directly setting the
[`HTMLInputElement`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLInputElement)
`value` property.

::: {#sect4 .notecard .note}
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

## Using email inputs {#using_email_inputs}

::: section-content
Email addresses are among the most frequently-inputted textual data
forms on the web; they\'re used when logging into websites, when
requesting information, to allow order confirmation, for webmail, and so
forth. As such, the `email` input type can make your job as a web
developer much easier since it can help simplify your work when building
the user interface and logic for email addresses. When you create an
email input with the proper `type` value, `email`, you get automatic
validation that the entered text is at least in the correct form to
potentially be a legitimate email address. This can help avoid cases in
which the user mistypes their address, or provides an invalid address.

It\'s important, however, to note that this is not enough to ensure that
the specified text is an email address which actually exists,
corresponds to the user of the site, or is acceptable in any other way.
It ensures that the value of the field is properly formatted to be an
email address.

::: {#sect5 .notecard .note}
**Note:** It\'s also crucial to remember that a user can tinker with
your HTML behind the scenes, so your site *must not* use this validation
for any security purposes. You *must* verify the email address on the
server side of any transaction in which the provided text may have any
security implications of any kind.
:::
:::

### A simple email input {#a_simple_email_input}

::: section-content
Currently, all browsers which implement this element implement it as a
standard text input field with basic validation features. The
specification does, however, allow browsers latitude on this. For
example, the element could be integrated with the user\'s device\'s
built-in address book to allow picking email addresses from that list.
In its most basic form, an `email` input can be implemented like this:

::: code-example
[html]{.language-name}

``` {signature="Al9b1EOyvRpkJSHlloiBnPysLjDDsDzSaqwxanCynpg=" data-language="html"}
<input id="emailAddress" type="email" />
```
:::

::: {#sect6 .code-example}
::: iframe
:::
:::

Notice that it\'s considered valid when empty and when a single
validly-formatted email address is entered, but is otherwise not
considered valid. By adding the [`required`](../input#required)
attribute, only validly-formed email addresses are allowed; the input is
no longer considered valid when empty.
:::

### Allowing multiple email addresses {#allowing_multiple_email_addresses}

::: section-content
By adding the [`multiple`](../../attributes/multiple) Boolean attribute,
the input can be configured to accept multiple email addresses.

::: code-example
[html]{.language-name}

``` {signature="Hh5OQxz0INBP+DsAt5hy34Cg71iKOLp6z95sYhiOoxA=" data-language="html"}
<input id="emailAddress" type="email" multiple />
```
:::

::: {#sect7 .code-example}
::: iframe
:::
:::

The input is now considered valid when a single email address is
entered, or when any number of email addresses separated by commas and,
optionally, some number of whitespace characters are present.

::: {#sect8 .notecard .note}
**Note:** When `multiple` is used, the value *is* allowed to be empty.
:::

Some examples of valid strings when `multiple` is specified:

-   `""`
-   `"me@example"`
-   `"me@example.org"`
-   `"me@example.org,you@example.org"`
-   `"me@example.org, you@example.org"`
-   `"me@example.org,you@example.org, us@example.org"`

Some examples of invalid strings:

-   `","`
-   `"me"`
-   `"me@example.org you@example.org"`
:::

### Placeholders

::: section-content
Sometimes it\'s helpful to offer an in-context hint as to what form the
input data should take. This can be especially important if the page
design doesn\'t offer descriptive labels for each [`<input>`](../input).
This is where **placeholders** come in. A placeholder is a value that
demonstrates the form the `value` should take by presenting an example
of a valid value, which is displayed inside the edit box when the
element\'s `value` is \"\". Once data is entered into the box, the
placeholder disappears; if the box is emptied, the placeholder
reappears.

Here, we have an `email` input with the placeholder
`sophie@example.com`. Note how the placeholder disappears and reappears
as you manipulate the contents of the edit field.

::: code-example
[html]{.language-name}

``` {signature="fZppfPNBIvlrJzsM8mwpNi8ZdKymiGsjqlHfvqGgtSg=" data-language="html"}
<input type="email" placeholder="sophie@example.com" />
```
:::

::: {#sect9 .code-example}
::: iframe
:::
:::
:::

### Controlling the input size {#controlling_the_input_size}

::: section-content
You can control not only the physical length of the input box, but also
the minimum and maximum lengths allowed for the input text itself.

#### Physical input element size {#physical_input_element_size}

The physical size of the input box can be controlled using the
[`size`](../input#size) attribute. With it, you can specify the number
of characters the input box can display at a time. In this example the
`email` edit box is 15 characters wide:

::: code-example
[html]{.language-name}

``` {signature="RjUBA7iApOL26b1ZYoehdt4lqvkJtj5rTMEqfnWkLsA=" data-language="html"}
<input type="email" size="15" />
```
:::

::: {#sect10 .code-example}
::: iframe
:::
:::

#### Element value length {#element_value_length}

The `size` is separate from the length limitation on the entered email
address itself so that you can have fields fit in a small space while
still allowing longer email address strings to be entered. You can
specify a minimum length, in characters, for the entered email address
using the [`minlength`](../input#minlength) attribute; similarly, use
[`maxlength`](../input#maxlength) to set the maximum length of the
entered email address.

The example below creates a 32 character-wide email address entry box,
requiring that the contents be no shorter than 3 characters and no
longer than 64 characters.

::: code-example
[html]{.language-name}

``` {signature="7nmyLiLQaqq+H/OF8w7lMAEuf7VGtyCiV6W0EQwmJtg=" data-language="html"}
<input type="email" size="32" minlength="3" maxlength="64" />
```
:::

::: {#sect11 .code-example}
::: iframe
:::
:::
:::

### Providing default options {#providing_default_options}

::: section-content
#### Providing a single default using the value attribute {#providing_a_single_default_using_the_value_attribute}

As always, you can provide a default value for an `email` input box by
setting its [`value`](../input#value) attribute:

::: code-example
[html]{.language-name}

``` {signature="KnGmkt9UMpzBxPwvMqqQMbGvkmridtYGhIsQlfuzsEc=" data-language="html"}
<input type="email" value="default@example.com" />
```
:::

::: {#sect12 .code-example}
::: iframe
:::
:::

#### Offering suggested values {#offering_suggested_values}

Taking it a step further, you can provide a list of default options from
which the user can select by specifying the [`list`](../input#list)
attribute. This doesn\'t limit the user to those options, but does allow
them to select commonly-used email addresses more quickly. This also
offers hints to [`autocomplete`](../input#autocomplete). The `list`
attribute specifies the ID of a [`<datalist>`](../datalist), which in
turn contains one [`<option>`](../option) element per suggested value;
each `option`\'s `value` is the corresponding suggested value for the
email entry box.

::: code-example
[html]{.language-name}

``` {signature="BJ6VjNrRFCHLEiy6QHSdPpHIXr/84mKlng9CPfHm/g4=" data-language="html"}
<input type="email" size="40" list="defaultEmails" />

<datalist id="defaultEmails">
  <option value="jbond007@mi6.defence.gov.uk"></option>
  <option value="jbourne@unknown.net"></option>
  <option value="nfury@shield.org"></option>
  <option value="tony@starkindustries.com"></option>
  <option value="hulk@grrrrrrrr.arg"></option>
</datalist>
```
:::

::: {#sect13 .code-example}
::: iframe
:::
:::

With the [`<datalist>`](../datalist) element and its
[`<option>`](../option)s in place, the browser will offer the specified
values as potential values for the email address; this is typically
presented as a popup or drop-down menu containing the suggestions. While
the specific user experience may vary from one browser to another,
typically clicking in the edit box presents a drop-down of the suggested
email addresses. Then, as the user types, the list is filtered to show
only matching values. Each typed character narrows down the list until
the user makes a selection or types a custom value.
:::

## Validation

::: section-content
There are two levels of content validation available for `email` inputs.
First, there\'s the standard level of validation offered to all
[`<input>`](../input)s, which automatically ensures that the contents
meet the requirements to be a valid email address. But there\'s also the
option to add additional filtering to ensure that your own specialized
needs are met, if you have any.

::: {#sect14 .notecard .warning}
**Warning:** HTML form validation is *not* a substitute for scripts that
ensure that the entered data is in the proper format.It\'s far too easy
for someone to make adjustments to the HTML that allow them to bypass
the validation, or to remove it completely. It\'s also possible for
someone to bypass your HTML entirely and submit the data directly to
your server. If your server-side code fails to validate the data it
receives, disaster could strike when improperly-formatted data (or data
which is too large, is of the wrong type, and so forth) is entered into
your database.
:::
:::

### Basic validation {#basic_validation}

::: section-content
Browsers automatically provide validation to ensure that only text that
matches the standard format for Internet email addresses is entered into
the input box. Browsers use an algorithm equivalent to the following
regular expression:

::: code-example
[js]{.language-name}

``` {signature="GMNgi6tkfmZa7pnP23eey7eUgtkNgju5zaUhdV1rzK0=" data-language="js"}
/^[a-zA-Z0-9.!#$%&'*+/=?^_`{|}~-]+@[a-zA-Z0-9](?:[a-zA-Z0-9-]{0,61}[a-zA-Z0-9])?(?:\.[a-zA-Z0-9](?:[a-zA-Z0-9-]{0,61}[a-zA-Z0-9])?)*$/;
```
:::

To learn more about how form validation works and how to take advantage
of the
[`:valid`](https://developer.mozilla.org/en-US/docs/Web/CSS/:valid) and
[`:invalid`](https://developer.mozilla.org/en-US/docs/Web/CSS/:invalid)
CSS properties to style the input based on whether the current value is
valid, see [Form data
validation](https://developer.mozilla.org/en-US/docs/Learn/Forms/Form_validation).

::: {#sect15 .notecard .note}
**Note:** There are known specification issues related to international
domain names and the validation of email addresses in HTML. See [W3C bug
15489](https://www.w3.org/Bugs/Public/show_bug.cgi?id=15489){target="_blank"}
for details.
:::
:::

### Pattern validation {#pattern_validation}

::: section-content
If you need the entered email address to be restricted further than just
\"any string that looks like an email address,\" you can use the
[`pattern`](../input#pattern) attribute to specify a [regular
expression](https://developer.mozilla.org/en-US/docs/Glossary/Regular_expression)
the value must match for it to be valid. If the
[`multiple`](../input#multiple) attribute is specified, each individual
item in the comma-delineated list of values must match the [regular
expression](https://developer.mozilla.org/en-US/docs/Glossary/Regular_expression).

For example, let\'s say you\'re building a page for employees of Best
Startup Ever, Inc. which will let them contact their IT department for
help. In our simplified form, the user needs to enter their email
address and a message describing the problem they need help with. We
want to ensure that not only does the user provide a valid email
address, but for security purposes, we require that the address be an
internal corporate email address.

Since inputs of type `email` validate against both the standard email
address validation *and* the specified [`pattern`](../input#pattern),
you can implement this easily. Let\'s see how:

::: code-example
[html]{.language-name}

``` {signature="mdOuiQfhct7xxxfmERsbf3T1y/bCqwaWISo8r6cjKco=" data-language="html"}
<form>
  <div class="emailBox">
    <label for="emailAddress">Your email address</label><br />
    <input
      id="emailAddress"
      type="email"
      size="64"
      maxlength="64"
      required
      placeholder="username@beststartupever.com"
      pattern=".+@beststartupever\.com"
      title="Please provide only a Best Startup Ever corporate email address" />
  

  <div class="messageBox">
    <label for="message">Request</label><br />
    <textarea
      id="message"
      cols="80"
      rows="8"
      required
      placeholder="My shoes are too tight, and I have forgotten how to dance."></textarea>
  
  <input type="submit" value="Send Request" />
</form>
```
:::

::: {#sect16 .code-example}
::: iframe
:::
:::

Our [`<form>`](../form) contains one [`<input>`](../input) of type
`email` for the user\'s email address, a [`<textarea>`](../textarea) to
enter their message for IT into, and an `<input>` of type
[`"submit"`](submit), which creates a button to submit the form. Each
text entry box has a [`<label>`](../label) associated with it to let the
user know what\'s expected of them.

Let\'s take a closer look at the email address entry box. Its
[`size`](../input#size) and [`maxlength`](../input#maxlength) attributes
are both set to 64 in order to show room for 64 characters worth of
email address, and to limit the number of characters actually entered to
a maximum of 64. The [`required`](../input#required) attribute is
specified, making it mandatory that a valid email address be provided.

An appropriate [`placeholder`](../input#placeholder) is
provided---`username@beststartupever.com`---to demonstrate what
constitutes a valid entry. This string demonstrates both that an email
address should be entered, and suggests that it should be a corporate
beststartupever.com account. This is in addition to the fact that using
type `email` will validate the text to ensure that it\'s formatted like
an email address. If the text in the input box isn\'t an email address,
you\'ll get an error message that looks something like this:

![Invalid email address in error state with a popout from the input
reading \'please enter an email
address\'.]
height="125" loading="lazy"}

If we left things at that, we would at least be validating on legitimate
email addresses. But we want to go one step farther: we want to make
sure that the email address is in fact in the form
\"<_username_@beststartupever.com>\". This is where we\'ll use
[`pattern`](../input#pattern). We set `pattern` to
`.+@beststartupever.com`. This simple regular expression requests a
string that consists of at least one character of any kind, then an
\"@\" followed by the domain name \"beststartupever.com\".

Note that this is not even close to an adequate filter for valid email
addresses; it would allow things such as \" \@beststartupever.com\"
(note the leading space) or \"@@beststartupever.com\", neither of which
is valid. However, the browser runs both the standard email address
filter *and* our custom pattern against the specified text. As a result,
we wind up with a validation which says \"make sure this resembles a
valid email address, and if it is, make sure it\'s also a
beststartupever.com address.\"

It\'s advisable to use the [`title`](../../global_attributes#title)
attribute along with `pattern`. If you do, the `title` *must* describe
the pattern. That is, it should explain what format the data should take
on, rather than any other information. That\'s because the `title` may
be displayed or spoken as part of a validation error message. For
example, the browser might present the message \"The entered text
doesn\'t match the required pattern.\" followed by your specified
`title`. If your `title` is something like \"Email address\", the result
would be the message \"The entered text doesn\'t match the required
pattern. Email address\", which isn\'t very good.

That\'s why, instead, we specify the string \"Please provide only a Best
Startup Ever corporate email address\" By doing that, the resulting full
error message might be something like \"The entered text doesn\'t match
the required pattern. Please provide only a Best Startup Ever corporate
email address.\"

![A valid email address, but the input is in error state with a popout
from the input reading \'The entered text doesn\'t match the required
pattern. Please provide only a Best Startup Ever corporate email
address.\']
height="140" loading="lazy"}

::: {#sect17 .notecard .note}
**Note:** If you run into trouble while writing your validation regular
expressions and they\'re not working properly, check your browser\'s
console; there may be helpful error messages there to aid you in solving
the problem.
:::
:::

## Examples

::: section-content
Here we have an email input with the ID `emailAddress` which is allowed
to be up to a maximum of 256 characters long. The input box itself is
physically 64 characters wide, and displays the text `user@example.gov`
as a placeholder anytime the field is empty. In addition, by using the
[`multiple`](../../attributes/multiple) attribute, the box is configured
to allow the user to enter zero or more email addresses, separated by
commas, as described in [Allowing multiple email
addresses](#allowing_multiple_email_addresses). As a final touch, the
[`list`](../input#list) attribute contains the ID of a
[`<datalist>`](../datalist) whose [`<option>`](../option)s specify a set
of suggested values the user can choose from.

As an added touch, the [`<label>`](../label) element is used to
establish a label for the email entry box, with its
[`for`](../label#for) attribute referencing the `emailAddress` ID of the
[`<input>`](../input) element. By associating the two elements in this
way, clicking on the label will focus the input element.

::: code-example
[html]{.language-name}

``` {signature="GEcPJmEt70+HN5kqWVMpUGX0NXfbcZP5lD/+mREKCH4=" data-language="html"}
<label for="emailAddress">Email</label><br />
<input
  id="emailAddress"
  type="email"
  placeholder="user@example.gov"
  list="defaultEmails"
  size="64"
  maxlength="256"
  multiple />

<datalist id="defaultEmails">
  <option value="jbond007@mi6.defence.gov.uk"></option>
  <option value="jbourne@unknown.net"></option>
  <option value="nfury@shield.org"></option>
  <option value="tony@starkindustries.com"></option>
  <option value="hulk@grrrrrrrr.arg"></option>
</datalist>
```
:::

::: {#sect18 .code-example}
::: iframe
:::
:::
:::

## Technical summary {#technical_summary}

::: section-content
<figure class="table-container">
<div class="_table">
<table class="properties">
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong><a href="#value">Value</a></strong></td>
<td>A string representing an email address, or empty</td>
</tr>
<tr class="even">
<td><strong>Events</strong></td>
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/change_event"><code>change</code></a>
and <a
href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/input_event"><code>input</code></a></td>
</tr>
<tr class="odd">
<td><strong>Supported Common Attributes</strong></td>
<td><a href="../input#autocomplete"><code>autocomplete</code></a>, <a
href="../input#list"><code>list</code></a>, <a
href="../input#maxlength"><code>maxlength</code></a>, <a
href="../input#minlength"><code>minlength</code></a>, <a
href="../input#multiple"><code>multiple</code></a>, <a
href="../input#name"><code>name</code></a>, <a
href="../input#pattern"><code>pattern</code></a>, <a
href="../input#placeholder"><code>placeholder</code></a>, <a
href="../input#readonly"><code>readonly</code></a>, <a
href="../input#required"><code>required</code></a>, <a
href="../input#size"><code>size</code></a>, and <a
href="../input#type"><code>type</code></a></td>
</tr>
<tr class="even">
<td><strong>IDL attributes</strong></td>
<td><code>list</code> and <code>value</code></td>
</tr>
<tr class="odd">
<td><strong>DOM interface</strong></td>
<td><p><a
href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLInputElement"><code>HTMLInputElement</code></a></p></td>
</tr>
<tr class="even">
<td><strong>Methods</strong></td>
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLInputElement/select"><code>select()</code></a></td>
</tr>
<tr class="odd">
<td><strong>Implicit ARIA Role</strong></td>
<td>with no <code>list</code> attribute: <a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/textbox_role"><code>textbox</code></a><br />
with <code>list</code> attribute: <a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/combobox_role"><code>combobox</code></a></td>
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
  email-state-(type=email)]{.small}](https://html.spec.whatwg.org/multipage/input.html#email-state-(type=email))

  ----------------------------------------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
  -------------------------------------------------------------------------------------------------------------------------------------
            Desktop                                                Mobile                                                    
  --------- --------- ------ --------- ---------- ------- -------- --------- --------- --------- --------- ----------------- ----------
            Chrome    Edge   Firefox   Internet   Opera   Safari   WebView   Chrome    Firefox   Opera     Safari on IOS     Samsung
                                       Explorer                    Android   Android   for       Android                     Internet
                                                                                       Android                               

  `email`   5         12     1         10         11      5        4.4       18        4         11        3                 1.0
                                                                                                                             
                                                                                                           \[\"Doesn\'t do   
                                                                                                           validation, but   
                                                                                                           instead offers a  
                                                                                                           custom \'email\'  
                                                                                                           keyboard, which   
                                                                                                           is designed to    
                                                                                                           make entering     
                                                                                                           email addresses   
                                                                                                           easier.\", \"The  
                                                                                                           custom \'email\'  
                                                                                                           keyboard does not 
                                                                                                           provide a comma   
                                                                                                           key, so users     
                                                                                                           cannot enter      
                                                                                                           multiple email    
                                                                                                           addresses.\",     
                                                                                                           \"Automatically   
                                                                                                           applies a default 
                                                                                                           style of          
                                                                                                           `opacity: 0.4` to 
                                                                                                           disable textual   
                                                                                                           `<input>`         
                                                                                                           elements,         
                                                                                                           including those   
                                                                                                           of type           
                                                                                                           \'email\'. Other  
                                                                                                           major browsers    
                                                                                                           don\'t currently  
                                                                                                           share this        
                                                                                                           particular        
                                                                                                           default           
                                                                                                           style.\"\]        
  -------------------------------------------------------------------------------------------------------------------------------------
:::

## See also {#see_also}

::: section-content
-   [HTML forms
    guide](https://developer.mozilla.org/en-US/docs/Learn/Forms)
-   [`<input>`](../input)
-   [`<input type="tel">`](tel)
-   [`<input type="url">`](url)
-   Attributes:
    -   [`list`](../input#list)
    -   [`minlength`](../../attributes/minlength)
    -   [`maxlength`](../../attributes/maxlength)
    -   [`multiple`](../../attributes/multiple)
    -   [`pattern`](../../attributes/pattern)
    -   [`placeholder`](../input#placeholder)
    -   [`readonly`](../../attributes/readonly)
    -   [`size`](../../attributes/size)
-   [Compatibility of CSS
    properties](https://developer.mozilla.org/en-US/docs/Learn/Forms/Property_compatibility_table_for_form_controls)
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/email](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/email){._attribution-link}
:::
