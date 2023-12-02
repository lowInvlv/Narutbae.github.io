

# \<input type=\"search\"\>



::: section-content
[`<input>`](../input) elements of type `search` are text fields designed
for the user to enter search queries into. These are functionally
identical to [`text`](text) inputs, but may be styled differently by the
[user
agent](https://developer.mozilla.org/en-US/docs/Glossary/User_agent).
:::

## Try it {#try_it}

::: section-content
::: iframe
::: {.output-header .border-rounded-top}
#### HTML Demo: \<input type=\"search\"\> {#html-demo-input-typesearch .output-heading}

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
    <label for="site-search">Search the site:</label>
    <input type="search" id="site-search" name="q" />

    <button>Search</button>
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
The [`value`](../input#value) attribute contains a string representing
the value contained in the search field. You can retrieve this using the
[`HTMLInputElement.value`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLInputElement#value)
property in JavaScript.

::: code-example
[js]{.language-name}

``` {signature="qxctvJ13g/WMY4Gp2AY41+L06WjBxLoJsh2Kc+rwbuM=" data-language="js"}
searchTerms = mySearch.value;
```
:::

If no validation constraints are in place for the input (see
[Validation](#validation) for more details), the value can be any text
string or an empty string (`""`).
:::

## Additional attributes {#additional_attributes}

::: section-content
In addition to the attributes that operate on all [`<input>`](../input)
elements regardless of their type, search field inputs support the
following attributes.
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
can enter into the search field. This must be an integer value of 0 or
higher. If no `maxlength` is specified, or an invalid value is
specified, the search field has no maximum length. This value must also
be greater than or equal to the value of `minlength`.

The input will fail [constraint validation](../../constraint_validation)
if the length of the text entered into the field is greater than
`maxlength` UTF-16 code units long.
:::

### minlength

::: section-content
The minimum string length (measured in UTF-16 code units) that the user
can enter into the search field. This must be a non-negative integer
value smaller than or equal to the value specified by `maxlength`. If no
`minlength` is specified, or an invalid value is specified, the search
input has no minimum length.

The search field will fail [constraint
validation](../../constraint_validation) if the length of the text
entered into the field is fewer than `minlength` UTF-16 code units long.
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

::: {#sect1 .notecard .note}
**Note:** Use the [`title`](../input#title) attribute to specify text
that most browsers will display as a tooltip to explain what the
requirements are to match the pattern. You should also include other
explanatory text nearby.
:::

See the section [Specifying a pattern](#specifying_a_pattern) for
details and an example.
:::

### placeholder

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
labels](../input#labels) for more information.
:::
:::

### readonly

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

### size

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

### spellcheck

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

[\"\" (empty string) or no value](#_empty_string_or_no_value)

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
The following non-standard attributes are available to search input
fields. As a general rule, you should avoid using them unless it can\'t
be helped.
:::

### autocorrect

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

### incremental

::: section-content
The Boolean attribute `incremental` is a WebKit and Blink extension (so
supported by Safari, Opera, Chrome, etc.) which, if present, tells the
[user
agent](https://developer.mozilla.org/en-US/docs/Glossary/User_agent) to
process the input as a live search. As the user edits the value of the
field, the user agent sends
[`search`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLInputElement/search_event)
events to the
[`HTMLInputElement`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLInputElement)
object representing the search box. This allows your code to update the
search results in real time as the user edits the search.

If `incremental` is not specified, the
[`search`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLInputElement/search_event)
event is only sent when the user explicitly initiates a search (such as
by pressing the [Enter]{.kbd} or [Return]{.kbd} key while editing the
field).

The `search` event is rate-limited so that it is not sent more
frequently than an implementation-defined interval.
:::

### mozactionhint [Deprecated]{.visually-hidden} {#mozactionhint_deprecated}

::: section-content
A Mozilla extension, which provides a hint as to what sort of action
will be taken if the user presses the [Enter]{.kbd} or [Return]{.kbd}
key while editing the field.

**Deprecated: Use [`enterkeyhint`](../../global_attributes#enterkeyhint)
instead.**
:::

### results

::: section-content
The `results` attribute---supported only by Safari---is a numeric value
that lets you override the maximum number of entries to be displayed in
the [`<input>`](../input) element\'s natively-provided drop-down menu of
previous search queries.

The value must be a non-negative decimal number. If not provided, or an
invalid value is given, the browser\'s default maximum number of entries
is used.
:::

## Using search inputs {#using_search_inputs}

::: section-content
`<input>` elements of type `search` are very similar to those of type
`text`, except that they are specifically intended for handling search
terms. They are basically equivalent in behavior, but user agents may
choose to style them differently by default (and, of course, sites may
use stylesheets to apply custom styles to them).
:::

### Basic example {#basic_example}

::: section-content
::: code-example
[html]{.language-name}

``` {signature="NAQqmdLIV0CJzTz0A4Ir4GCprLf2Ef2o6X11v7wDVjo=" data-language="html"}
<form>
  
    <input type="search" id="mySearch" name="q" />
    <button>Search</button>
  
</form>
```
:::

This renders like so:

::: {#sect4 .code-example}
::: iframe
:::
:::

`q` is the most common `name` given to search inputs, although it\'s not
mandatory. When submitted, the data name/value pair sent to the server
will be `q=searchterm`.

::: {#sect5 .notecard .note}
**Note:** You must remember to set a [`name`](../input#name) for your
input, otherwise nothing will be submitted.
:::
:::

### Differences between search and text types {#differences_between_search_and_text_types}

::: section-content
The main basic differences come in the way browsers handle them. The
first thing to note is that some browsers show a cross icon that can be
clicked on to remove the search term instantly if desired, in Chrome
this action is also triggered when pressing escape. The following
screenshot comes from Chrome:

![Focused search input, with focus ring, with the text \'cats\'. There
is an x icon in the input abutting the right
side.]
height="31" loading="lazy"}

In addition, modern browsers also tend to automatically store search
terms previously entered across domains, which then come up as
autocomplete options when subsequent searches are performed in search
inputs on that domain. This helps users who tend to do searches on the
same or similar search queries over time. This screenshot is from
Firefox:

![An input in error state with a red focus ring. The user has entered
the letter \'h\'. A pop-up selection list is open directly under the
input box with two options: hello and
hermansje.]
height="83" loading="lazy"}At this point, let\'s look at some useful
techniques you can apply to your search forms.
:::

### Setting placeholders {#setting_placeholders}

::: section-content
You can provide a useful placeholder inside your search input that could
give a hint on what to do using the
[`placeholder`](../input#placeholder) attribute. Look at the following
example:

::: code-example
[html]{.language-name}

``` {signature="E4kIkFAXgyJyTEg2+c5DZGZhsOYLadNJbePvlgYbwYs=" data-language="html"}
<form>
  
    <input
      type="search"
      id="mySearch"
      name="q"
      placeholder="Search the site…" />
    <button>Search</button>
  
</form>
```
:::

You can see how the placeholder is rendered below:

::: {#sect6 .code-example}
::: iframe
:::
:::
:::

### Search form labels and accessibility {#search_form_labels_and_accessibility}

::: section-content
One problem with search forms is their accessibility; a common design
practice is not to provide a label for the search field (although there
might be a magnifying glass icon or similar), as the purpose of a search
form is normally fairly obvious for sighted users due to placement
([this example shows a typical
pattern](https://mdn.github.io/learning-area/accessibility/aria/website-aria-roles/){target="_blank"}).

This could, however, cause confusion for screen reader users, since they
will not have any verbal indication of what the search input is. One way
around this that won\'t impact on your visual design is to use
[WAI-ARIA](https://developer.mozilla.org/en-US/docs/Learn/Accessibility/WAI-ARIA_basics)
features:

-   A `role` attribute of value `search` on the `<form>` element will
    cause screen readers to announce that the form is a search form.
-   If that isn\'t enough, you can use an
    [`aria-label`](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Attributes/aria-label)
    attribute on the [`<input>`](../input) itself. This should be a
    descriptive text label that will be read out by the screen reader;
    it\'s used as a non-visual equivalent to `<label>`.

Let\'s have a look at an example:

::: code-example
[html]{.language-name}

``` {signature="z+WPM2cqyaueYg00nAB0Wo4IwM6GjIQ2kRoP0WnJyRw=" data-language="html"}
<form role="search">
  
    <input
      type="search"
      id="mySearch"
      name="q"
      placeholder="Search the site…"
      aria-label="Search through site content" />
    <button>Search</button>
  
</form>
```
:::

You can see how this is rendered below:

::: {#sect7 .code-example}
::: iframe
:::
:::

There is no visual difference from the previous example, but screen
reader users have way more information available to them.

::: {#sect8 .notecard .note}
**Note:** See
[Signposts/Landmarks](https://developer.mozilla.org/en-US/docs/Learn/Accessibility/WAI-ARIA_basics#signpostslandmarks)
for more information about such accessibility features.
:::
:::

### Physical input element size {#physical_input_element_size}

::: section-content
The physical size of the input box can be controlled using the
[`size`](../input#size) attribute. With it, you can specify the number
of characters the input box can display at a time. In this example, for
instance, the search box is 30 characters wide:

::: code-example
[html]{.language-name}

``` {signature="iw6lObmkzq4stssnZKn6gv3ei3pvRs3pw6D0FUSXFHE=" data-language="html"}
<form>
  
    <input
      type="search"
      id="mySearch"
      name="q"
      placeholder="Search the site…"
      size="30" />
    <button>Search</button>
  
</form>
```
:::

The result is this wider input box:

::: {#sect9 .code-example}
::: iframe
:::
:::
:::

## Validation

::: section-content
`<input>` elements of type `search` have the same validation features
available to them as regular `text` inputs. It is less likely that
you\'d want to use validation features in general for search boxes. In
many cases, users should just be allowed to search for anything, but
there are a few cases to consider, such as searches against data of a
known format.

::: {#sect10 .notecard .note}
**Note:** HTML form validation is *not* a substitute for scripts that
ensure that the entered data is in the proper format. It\'s far too easy
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
There are useful pseudo-classes available for styling valid/invalid form
elements:
[`:valid`](https://developer.mozilla.org/en-US/docs/Web/CSS/:valid) and
[`:invalid`](https://developer.mozilla.org/en-US/docs/Web/CSS/:invalid).
In this section, we\'ll use the following CSS, which will place a check
(tick) next to inputs containing valid values, and a cross next to
inputs containing invalid values.

::: code-example
[css]{.language-name}

``` {signature="CKRTwu8HzX0yTXvAMib+eMKbf76PT5ZKisJwHlwijwc=" data-language="css"}
input:invalid ~ span::after {
  content: "✖";
  padding-left: 5px;
  position: absolute;
}

input:valid ~ span::after {
  content: "✓";
  padding-left: 5px;
  position: absolute;
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

``` {signature="iNjkpirg8ZCYqbUHWf7YcqdVMUJWOAZ9fb0pTa4CMqw=" data-language="html"}
<form>
  
    <input
      type="search"
      id="mySearch"
      name="q"
      placeholder="Search the site…"
      required />
    <button>Search</button>
    <span class="validity"></span>
  
</form>
```
:::

This renders like so:

::: {#sect11 .code-example}
::: iframe
:::
:::

In addition, if you try to submit the form with no search term entered
into it, the browser will show a message. The following example is from
Firefox:

![form field with attached message that says Please fill out this
field]
height="114" loading="lazy"}

Different messages will be shown when you try to submit the form with
different types of invalid data contained inside the inputs; see the
below examples.
:::

### Input value length {#input_value_length}

::: section-content
You can specify a minimum length, in characters, for the entered value
using the [`minlength`](../input#minlength) attribute; similarly, use
[`maxlength`](../input#maxlength) to set the maximum length of the
entered value.

The example below requires that the entered value be 4--8 characters in
length.

::: code-example
[html]{.language-name}

``` {signature="ZyMITUb28g7lxUjiFVL9MvpP+txnUKKeGuIwpaozwfY=" data-language="html"}
<form>
  
    <label for="mySearch">Search for user</label>
    <input
      type="search"
      id="mySearch"
      name="q"
      placeholder="User IDs are 4–8 characters in length"
      required
      size="30"
      minlength="4"
      maxlength="8" />
    <button>Search</button>
    <span class="validity"></span>
  
</form>
```
:::

This renders like so:

::: {#sect12 .code-example}
::: iframe
:::
:::

If you try to submit the form with less than 4 characters, you\'ll be
given an appropriate error message (which differs between browsers). If
you try to go beyond 8 characters in length, the browser won\'t let you.
:::

### Specifying a pattern {#specifying_a_pattern}

::: section-content
You can use the [`pattern`](../input#pattern) attribute to specify a
regular expression that the inputted value must follow to be considered
valid (see [Validating against a regular
expression](https://developer.mozilla.org/en-US/docs/Learn/Forms/Form_validation#validating_against_a_regular_expression)
for a simple crash course).

Let\'s look at an example. Say we wanted to provide a product ID search
form, and the IDs were all codes of two letters followed by four
numbers. The following example covers it:

::: code-example
[html]{.language-name}

``` {signature="RV6Kk6CwFhuerNj8b2cbJRsYyK6EpKsqPLPz+O9TvCU=" data-language="html"}
<form>
  
    <label for="mySearch">Search for product by ID:</label>
    <input
      type="search"
      id="mySearch"
      name="q"
      placeholder="two letters followed by four numbers"
      required
      size="30"
      pattern="[A-z]{2}[0-9]{4}" />
    <button>Search</button>
    <span class="validity"></span>
  
</form>
```
:::

This renders like so:

::: {#sect13 .code-example}
::: iframe
:::
:::
:::

## Examples

::: section-content
You can see a good example of a search form used in context at our
[website-aria-roles](https://github.com/mdn/learning-area/tree/main/accessibility/aria/website-aria-roles){target="_blank"}
example ([see it
live](https://mdn.github.io/learning-area/accessibility/aria/website-aria-roles/){target="_blank"}).
:::

## Technical summary {#technical_summary}

::: section-content
<figure class="table-container">
<div class="_table">
<table class="properties">
<tbody>
<tr class="odd">
<td><strong><a href="#value">Value</a></strong></td>
<td>A string representing the value contained in the search field.</td>
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
href="../input#required"><code>required</code></a>, <a
href="../input#size"><code>size</code></a>.</td>
<td></td>
</tr>
<tr class="even">
<td><strong>IDL attributes</strong></td>
<td><code>value</code></td>
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
href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLInputElement/setRangeText"><code>setRangeText()</code></a>,
<a
href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLInputElement/setSelectionRange"><code>setSelectionRange()</code></a>.</td>
<td></td>
</tr>
<tr class="odd">
<td><strong>Implicit ARIA Role</strong></td>
<td>with no <code>list</code> attribute: <a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/searchbox_role"><code>searchbox</code></a></td>
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
  ---------- --------- ------ --------- ------------------- ------- -------- ----------------- ---------------- --------------------- --------------- --------------- ------------------
             Chrome    Edge   Firefox   Internet Explorer   Opera   Safari   WebView Android   Chrome Android   Firefox for Android   Opera Android   Safari on IOS   Samsung Internet
  `search`   5         12     4         10                  10.6    5        4.4               18               4                     14              4.2             1.0
:::

## See also {#see_also}

::: section-content
-   [HTML Forms](https://developer.mozilla.org/en-US/docs/Learn/Forms)
-   [`<input>`](../input) and the
    [`HTMLInputElement`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLInputElement)
    interface it\'s based upon
-   [`<input type="text">`](text)
-   [Compatibility of CSS
    properties](https://developer.mozilla.org/en-US/docs/Learn/Forms/Property_compatibility_table_for_form_controls)
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/search](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/search){._attribution-link}
:::
