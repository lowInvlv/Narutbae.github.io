

# \<input type=\"submit\"\>



::: section-content
[`<input>`](../input) elements of type `submit` are rendered as buttons.
When the
[`click`](https://developer.mozilla.org/en-US/docs/Web/API/Element/click_event)
event occurs (typically because the user clicked the button), the [user
agent](https://developer.mozilla.org/en-US/docs/Glossary/User_agent)
attempts to submit the form to the server.
:::

## Value

::: section-content
An `<input type="submit">` element\'s [`value`](../input#value)
attribute contains a string which is displayed as the button\'s label.
Buttons do not have a true value otherwise.
:::

### Setting the value attribute {#setting_the_value_attribute}

::: section-content
::: code-example
[html]{.language-name}

``` {signature="Iad9SdiITwbaZsfhVkuq1ca4xsTOhxrbOjWaRKzcUoI=" data-language="html"}
<input type="submit" value="Send Request" />
```
:::

::: {#sect1 .code-example}
::: iframe
:::
:::
:::

### Omitting the value attribute {#omitting_the_value_attribute}

::: section-content
If you don\'t specify a `value`, the button will have a default label,
chosen by the user agent. This label is likely to be something along the
lines of \"Submit\" or \"Submit Query.\" Here\'s an example of a submit
button with a default label in your browser:

::: code-example
[html]{.language-name}

``` {signature="9XziiCTJpPvXKPOMD9NMZYz10+nHFyT/JAi6vrgJtAs=" data-language="html"}
<input type="submit" />
```
:::

::: {#sect2 .code-example}
::: iframe
:::
:::
:::

## Additional attributes {#additional_attributes}

::: section-content
In addition to the attributes shared by all [`<input>`](../input)
elements, `submit` button inputs support the following attributes.
:::

### formaction

::: section-content
A string indicating the URL to which to submit the data. This takes
precedence over the [`action`](../form#action) attribute on the
[`<form>`](../form) element that owns the [`<input>`](../input).

This attribute is also available on [`<input type="image">`](image) and
[`<button>`](../button) elements.
:::

### formenctype

::: section-content
A string that identifies the encoding method to use when submitting the
form data to the server. There are three permitted values:

[`application/x-www-form-urlencoded`](#applicationx-www-form-urlencoded)

:   This, the default value, sends the form data as a string after [URL
    encoding](https://en.wikipedia.org/wiki/URL_encoding){target="_blank"}
    the text using an algorithm such as
    [`encodeURI()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/encodeURI).

[`multipart/form-data`](#multipartform-data)

:   Uses the
    [`FormData`](https://developer.mozilla.org/en-US/docs/Web/API/FormData)
    API to manage the data, allowing for files to be submitted to the
    server. You *must* use this encoding type if your form includes any
    [`<input>`](../input) elements of [`type`](../input#type) `file`
    ([`<input type="file">`](file)).

[`text/plain`](#textplain)

:   Plain text; mostly useful only for debugging, so you can easily see
    the data that\'s to be submitted.

If specified, the value of the `formenctype` attribute overrides the
owning form\'s [`action`](../form#action) attribute.

This attribute is also available on [`<input type="image">`](image) and
[`<button>`](../button) elements.
:::

### formmethod

::: section-content
A string indicating the HTTP method to use when submitting the form\'s
data; this value overrides any [`method`](../form#method) attribute
given on the owning form. Permitted values are:

[`get`](#get)

:   A URL is constructed by starting with the URL given by the
    `formaction` or [`action`](../form#action) attribute, appending a
    question mark (\"?\") character, then appending the form\'s data,
    encoded as described by `formenctype` or the form\'s
    [`enctype`](../form#enctype) attribute. This URL is then sent to the
    server using an HTTP
    [`get`](https://developer.mozilla.org/en-US/docs/Web/HTTP/Methods/GET)
    request. This method works well for simple forms that contain only
    [ASCII](https://developer.mozilla.org/en-US/docs/Glossary/ASCII)
    characters and have no side effects. This is the default value.

[`post`](#post)

:   The form\'s data is included in the body of the request that is sent
    to the URL given by the `formaction` or [`action`](../form#action)
    attribute using an HTTP
    [`post`](https://developer.mozilla.org/en-US/docs/Web/HTTP/Methods/POST)
    method. This method supports complex data and file attachments.

[`dialog`](#dialog)

:   This method is used to indicate that the button closes the dialog
    with which the input is associated, and does not transmit the form
    data at all.

This attribute is also available on [`<input type="image">`](image) and
[`<button>`](../button) elements.
:::

### formnovalidate

::: section-content
A Boolean attribute which, if present, specifies that the form should
not be validated before submission to the server. This overrides the
value of the [`novalidate`](../form#novalidate) attribute on the
element\'s owning form.

This attribute is also available on [`<input type="image">`](image) and
[`<button>`](../button) elements.
:::

### formtarget

::: section-content
A string which specifies a name or keyword that indicates where to
display the response received after submitting the form. The string must
be the name of a **browsing context** (that is, a tab, window, or
[`<iframe>`](../iframe)). A value specified here overrides any target
given by the [`target`](../form#target) attribute on the
[`<form>`](../form) that owns this input.

In addition to the actual names of tabs, windows, or inline frames,
there are a few special keywords that can be used:

[`_self`](#_self)

:   Loads the response into the same browsing context as the one that
    contains the form. This will replace the current document with the
    received data. This is the default value used if none is specified.

[`_blank`](#_blank)

:   Loads the response into a new, unnamed, browsing context. This is
    typically a new tab in the same window as the current document, but
    may differ depending on the configuration of the [user
    agent](https://developer.mozilla.org/en-US/docs/Glossary/User_agent).

[`_parent`](#_parent)

:   Loads the response into the parent browsing context of the current
    one. If there is no parent context, this behaves the same as
    `_self`.

[`_top`](#_top)

:   Loads the response into the top-level browsing context; this is the
    browsing context that is the topmost ancestor of the current
    context. If the current context is the topmost context, this behaves
    the same as `_self`.

This attribute is also available on [`<input type="image">`](image) and
[`<button>`](../button) elements.
:::

## Using submit buttons {#using_submit_buttons}

::: section-content
`<input type="submit">` buttons are used to submit forms. If you want to
create a custom button and then customize the behavior using JavaScript,
you need to use [`<input type="button">`](button), or better still, a
[`<button>`](../button) element.

If you choose to use `<button>` elements to create the buttons in your
form, keep this in mind: If the `<button>` is inside a
[`<form>`](../form), that button will be treated as the \"submit\"
button. So you should be in the habit of expressly specifying which
button is the submit button.
:::

### A simple submit button {#a_simple_submit_button}

::: section-content
We\'ll begin by creating a form with a simple submit button:

::: code-example
[html]{.language-name}

``` {signature="iaL7MHRcae7FuABNcbmaI9FKC0pgQgoeaY2jBRyTd6o=" data-language="html"}
<form>
  
    <label for="example">Let's submit some text</label>
    <input id="example" type="text" name="text" />
  
  
    <input type="submit" value="Send" />
  
</form>
```
:::

This renders like so:

::: {#sect3 .code-example}
::: iframe
:::
:::

Try entering some text into the text field, and then submitting the
form.

Upon submitting, the data name/value pair gets sent to the server. In
this instance, the string will be `text=usertext`, where \"usertext\" is
the text entered by the user, encoded to preserve special characters.
Where and how the data is submitted depends on the configuration of the
`<form>`; see [Sending form
data](https://developer.mozilla.org/en-US/docs/Learn/Forms/Sending_and_retrieving_form_data)
for more details.
:::

### Adding a keyboard shortcut to a submit button {#adding_a_keyboard_shortcut_to_a_submit_button}

::: section-content
Keyboard shortcuts, also known as access keys and keyboard equivalents,
let the user trigger a button using a key or combination of keys on the
keyboard. To add a keyboard shortcut to a submit button --- just as you
would with any [`<input>`](../input) for which it makes sense --- you
use the [`accesskey`](../../global_attributes/accesskey) global
attribute.

In this example, [s]{.kbd} is specified as the access key (you\'ll need
to press [s]{.kbd} plus the particular modifier keys for your browser/OS
combination). In order to avoid conflicts with the user agent\'s own
keyboard shortcuts, different modifier keys are used for access keys
than for other shortcuts on the host computer. See
[`accesskey`](../../global_attributes/accesskey) for further details.

Here\'s the previous example with the [s]{.kbd} access key added:

::: code-example
[html]{.language-name}

``` {signature="aUkdr6Tr6+e7VvXKC4XfqnnkhmlVGqB2Eq4qhnHOtj8=" data-language="html"}
<form>
  
    <label for="example">Let's submit some text</label>
    <input id="example" type="text" name="text" />
  
  
    <input type="submit" value="Send" accesskey="s" />
  
</form>
```
:::

For example, in Firefox for Mac, pressing
[Control]{.kbd}-[Option]{.kbd}-[S]{.kbd} triggers the Send button, while
Chrome on Windows uses [Alt]{.kbd}+[S]{.kbd}.

::: {#sect4 .code-example}
::: iframe
:::
:::

The problem with the above example is that the user will not know what
the access key is! This is especially true since the modifiers are
typically non-standard to avoid conflicts. When building a site, be sure
to provide this information in a way that doesn\'t interfere with the
site design (for example by providing an easily accessible link that
points to information on what the site access keys are). Adding a
tooltip to the button (using the
[`title`](../../global_attributes/title) attribute) can also help,
although it\'s not a complete solution for accessibility purposes.
:::

### Disabling and enabling a submit button {#disabling_and_enabling_a_submit_button}

::: section-content
To disable a submit button, specify the
[`disabled`](../../attributes/disabled) attribute on it, like so:

::: code-example
[html]{.language-name}

``` {signature="kPAtfE9Bey+Jqe3PqeX+PqPgh4ROMvbixxEqEYHQomQ=" data-language="html"}
<input type="submit" value="Send" disabled />
```
:::

You can enable and disable buttons at run time by setting `disabled` to
`true` or `false`; in JavaScript this looks like `btn.disabled = true`
or `btn.disabled = false`.

::: {#sect5 .notecard .note}
**Note:** See the
[`<input type="button">`](button#disabling_and_enabling_a_button) page
for more ideas about enabling and disabling buttons.
:::
:::

## Validation

::: section-content
Submit buttons don\'t participate in constraint validation; they have no
real value to be constrained.
:::

## Examples

::: section-content
We\'ve included simple examples above. There isn\'t really anything more
to say about submit buttons. There\'s a reason this kind of control is
sometimes called a \"simple button.\"
:::

## Technical Summary {#technical_summary}

::: section-content
<figure class="table-container">
<div class="_table">
<table class="properties">
<tbody>
<tr class="odd">
<td><strong><a href="#value">Value</a></strong></td>
<td>A string used as the button's label</td>
</tr>
<tr class="even">
<td><strong>Events</strong></td>
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/API/Element/click_event"><code>click</code></a></td>
</tr>
<tr class="odd">
<td><strong>Supported common attributes</strong></td>
<td><a href="../input#type"><code>type</code></a> and <a
href="../input#value"><code>value</code></a></td>
</tr>
<tr class="even">
<td><strong>IDL attributes</strong></td>
<td><code>value</code></td>
</tr>
<tr class="odd">
<td><strong>DOM interface</strong></td>
<td><p><a
href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLInputElement"><code>HTMLInputElement</code></a></p></td>
</tr>
<tr class="even">
<td><strong>Methods</strong></td>
<td>None</td>
</tr>
<tr class="odd">
<td><strong>Implicit ARIA Role</strong></td>
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/button_role"><code>button</code></a></td>
</tr>
</tbody>
</table>

</figure>
:::

## Specifications

::: _table
  ----------------------------------------------------------------------------------------------------------------------------------
  Specification
  ----------------------------------------------------------------------------------------------------------------------------------
  [HTML Standard\
  [\#
  submit-button-state-(type=submit)]{.small}](https://html.spec.whatwg.org/multipage/input.html#submit-button-state-(type=submit))

  ----------------------------------------------------------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
  ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
             Desktop                                                                                                                                                                       Mobile                                                                                                                                                                  
  ---------- --------- ------ -------------------------------------------------------------------------------------------------------------------------------- ---------- ------- -------- --------- --------- -------------------------------------------------------------------------------------------------------------------------------- --------- -------- ----------
             Chrome    Edge   Firefox                                                                                                                          Internet   Opera   Safari   WebView   Chrome    Firefox for Android                                                                                                              Opera     Safari   Samsung
                                                                                                                                                               Explorer                    Android   Android                                                                                                                                    Android   on IOS   Internet

  `submit`   1         12     1                                                                                                                                Yes        15      1        4.4       18        4                                                                                                                                14        1        1.0
                                                                                                                                                                                                                                                                                                                                                                   
                              Unlike other browsers, Firefox by default [persists the dynamic disabled                                                                                                         Unlike other browsers, Firefox by default [persists the dynamic disabled                                                                            
                              state](https://stackoverflow.com/questions/5985839/bug-with-firefox-disabled-attribute-of-input-not-resetting-when-refreshing)                                                   state](https://stackoverflow.com/questions/5985839/bug-with-firefox-disabled-attribute-of-input-not-resetting-when-refreshing)                      
                              of a `<button>` across page loads. Use the                                                                                                                                       of a `<button>` across page loads. Use the                                                                                                          
                              [`autocomplete`](https://developer.mozilla.org/docs/Web/HTML/Element/button#attr-autocomplete) attribute to control this                                                         [`autocomplete`](https://developer.mozilla.org/docs/Web/HTML/Element/button#attr-autocomplete) attribute to control this                            
                              feature.                                                                                                                                                                         feature.                                                                                                                                            
  ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
:::

## See also {#see_also}

::: section-content
-   [`<input>`](../input) and the
    [`HTMLInputElement`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLInputElement)
    interface which implements it.
-   [Forms and
    buttons](https://developer.mozilla.org/en-US/docs/Learn/Forms/Basic_native_form_controls#actual_buttons)
-   [HTML forms](https://developer.mozilla.org/en-US/docs/Learn/Forms)
-   The [`<button>`](../button) element
-   [Compatibility of CSS
    properties](https://developer.mozilla.org/en-US/docs/Learn/Forms/Property_compatibility_table_for_form_controls)
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/submit](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/submit){._attribution-link}
:::
