

# \<textarea\>: The Textarea element



::: section-content
The `<textarea>` [HTML](../index) element represents a multi-line
plain-text editing control, useful when you want to allow users to enter
a sizeable amount of free-form text, for example a comment on a review
or feedback form.
:::

## Try it {#try_it}

::: section-content
::: iframe
::: {.output-header .border-rounded-top}
#### HTML Demo: \<textarea\> {#html-demo-textarea .output-heading}

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
    <label for="story">Tell us your story:</label>

    <textarea id="story" name="story" rows="5" cols="33">
    It was a dark and stormy night...
    </textarea>
:::
:::

::: {#css-panel .section .hidden tabindex="0" role="tabpanel" aria-labelledby="css" aria-hidden="true"}
::: {#css-editor}
    label,
    textarea {
      font-size: 0.8rem;
      letter-spacing: 1px;
    }

    textarea {
      padding: 10px;
      max-width: 100%;
      line-height: 1.5;
      border-radius: 5px;
      border: 1px solid #ccc;
      box-shadow: 1px 1px 1px #999;
    }

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

The above example demonstrates a number of features of `<textarea>`:

-   An `id` attribute to allow the `<textarea>` to be associated with a
    [`<label>`](label) element for accessibility purposes
-   A `name` attribute to set the name of the associated data point
    submitted to the server when the form is submitted.
-   `rows` and `cols` attributes to allow you to specify an exact size
    for the `<textarea>` to take. Setting these is a good idea for
    consistency, as browser defaults can differ.
-   Default content entered between the opening and closing tags.
    `<textarea>` does not support the `value` attribute.

The `<textarea>` element also accepts several attributes common to form
`<input>`s, such as `autocomplete`, `autofocus`, `disabled`,
`placeholder`, `readonly`, and `required`.
:::

## Attributes

::: section-content
This element includes the [global attributes](../global_attributes).

[`autocomplete`](#autocomplete)

:   This attribute indicates whether the value of the control can be
    automatically completed by the browser. Possible values are:

    -   `off`: The user must explicitly enter a value into this field
        for every use, or the document provides its own auto-completion
        method; the browser does not automatically complete the entry.
    -   `on`: The browser can automatically complete the value based on
        values that the user has entered during previous uses.

    If the `autocomplete` attribute is not specified on a `<textarea>`
    element, then the browser uses the `autocomplete` attribute value of
    the `<textarea>` element\'s form owner. The form owner is either the
    [`<form>`](form) element that this `<textarea>` element is a
    descendant of or the form element whose `id` is specified by the
    `form` attribute of the input element. For more information, see the
    [`autocomplete`](form#autocomplete) attribute in [`<form>`](form).

[`autocorrect`](#autocorrect) [Non-standard]{.visually-hidden}

:   A string which indicates whether to activate automatic spelling
    correction and processing of text substitutions (if any are
    configured) while the user is editing this `textarea`. Permitted
    values are:

    [`on`](#on)

    :   Enable automatic spelling correction and text substitutions.

    [`off`](#off)

    :   Disable automatic spelling correction and text substitutions.

[`autofocus`](#autofocus)

:   This Boolean attribute lets you specify that a form control should
    have input focus when the page loads. Only one form-associated
    element in a document can have this attribute specified.

[`cols`](#cols)

:   The visible width of the text control, in average character widths.
    If it is specified, it must be a positive integer. If it is not
    specified, the default value is `20`.

[`dirname`](#dirname)

:   This attribute is used to indicate the text directionality of the
    element contents similar to the [`dirname`](input#dirname) attribute
    of the `<input>` element. For more information, see the [`dirname`
    attribute](../attributes/dirname).

[`disabled`](#disabled)

:   This Boolean attribute indicates that the user cannot interact with
    the control. If this attribute is not specified, the control
    inherits its setting from the containing element, for example
    [`<fieldset>`](fieldset); if there is no containing element when the
    `disabled` attribute is set, the control is enabled.

[`form`](#form)

:   The form element that the `<textarea>` element is associated with
    (its \"form owner\"). The value of the attribute must be the `id` of
    a form element in the same document. If this attribute is not
    specified, the `<textarea>` element must be a descendant of a form
    element. This attribute enables you to place `<textarea>` elements
    anywhere within a document, not just as descendants of form
    elements.

[`maxlength`](#maxlength)

:   The maximum string length (measured in UTF-16 code units) that the
    user can enter. If this value isn\'t specified, the user can enter
    an unlimited number of characters.

[`minlength`](#minlength)

:   The minimum string length (measured in UTF-16 code units) required
    that the user should enter.

[`name`](#name)

:   The name of the control.

[`placeholder`](#placeholder)

:   A hint to the user of what can be entered in the control. Carriage
    returns or line-feeds within the placeholder text must be treated as
    line breaks when rendering the hint.

    ::: {#sect1 .notecard .note}
    **Note:** Placeholders should only be used to show an example of the
    type of data that should be entered into a form; they are *not* a
    substitute for a proper [`<label>`](label) element tied to the
    input. See [`<input>` labels](input#labels) for a full explanation.
    :::

[`readonly`](#readonly)

:   This Boolean attribute indicates that the user cannot modify the
    value of the control. Unlike the `disabled` attribute, the
    `readonly` attribute does not prevent the user from clicking or
    selecting in the control. The value of a read-only control is still
    submitted with the form.

[`required`](#required)

:   This attribute specifies that the user must fill in a value before
    submitting a form.

[`rows`](#rows)

:   The number of visible text lines for the control. If it is
    specified, it must be a positive integer. If it is not specified,
    the default value is 2.

[`spellcheck`](#spellcheck)

:   Specifies whether the `<textarea>` is subject to spell checking by
    the underlying browser/OS. The value can be:

    -   `true`: Indicates that the element needs to have its spelling
        and grammar checked.
    -   `default` : Indicates that the element is to act according to a
        default behavior, possibly based on the parent element\'s own
        `spellcheck` value.
    -   `false` : Indicates that the element should not be spell
        checked.

[`wrap`](#wrap)

:   Indicates how the control should wrap the value for form submission.
    Possible values are:

    -   `hard`: The browser automatically inserts line breaks (CR+LF) so
        that each line is no longer than the width of the control; the
        [`cols`](#cols) attribute must be specified for this to take
        effect
    -   `soft`: The browser ensures that all line breaks in the entered
        value are a `CR+LF` pair, but no additional line breaks are
        added to the value.
    -   `off` [Non-standard]{.visually-hidden} : Like `soft` but changes
        appearance to `white-space: pre` so line segments exceeding
        `cols` are not wrapped and the `<textarea>` becomes horizontally
        scrollable.

    If this attribute is not specified, `soft` is its default value.
:::

## Styling with CSS {#styling_with_css}

::: section-content
`<textarea>` is a [replaced
element](https://developer.mozilla.org/en-US/docs/Web/CSS/Replaced_element)
--- it has intrinsic dimensions, like a raster image. By default, its
[`display`](https://developer.mozilla.org/en-US/docs/Web/CSS/display)
value is `inline-block`. Compared to other form elements it is
relatively easy to style, with its box model, fonts, color scheme, etc.
being easily manipulable using regular CSS.

[Styling HTML
forms](https://developer.mozilla.org/en-US/docs/Learn/Forms/Styling_web_forms)
provides some useful tips on styling `<textarea>`s.
:::

### Baseline inconsistency {#baseline_inconsistency}

::: section-content
The HTML specification doesn\'t define where the baseline of a
`<textarea>` is, so different browsers set it to different positions.
For Gecko, the `<textarea>` baseline is set on the baseline of the first
line of the textarea, on another browser it may be set on the bottom of
the `<textarea>` box. Don\'t use
[`vertical-align`](https://developer.mozilla.org/en-US/docs/Web/CSS/vertical-align)`: baseline`
on it; the behavior is unpredictable.
:::

### Controlling whether a textarea is resizable {#controlling_whether_a_textarea_is_resizable}

::: section-content
In most browsers, `<textarea>`s are resizable --- you\'ll notice the
drag handle in the right-hand corner, which can be used to alter the
size of the element on the page. This is controlled by the
[`resize`](https://developer.mozilla.org/en-US/docs/Web/CSS/resize) CSS
property --- resizing is enabled by default, but you can explicitly
disable it using a `resize` value of `none`:

::: code-example
[css]{.language-name}

``` {signature="Kb/u3bu1nvpT/O7lKtEIo+bzXU7mcTXkT9lOo9LL1Tc=" data-language="css"}
textarea {
  resize: none;
}
```
:::
:::

### Styling valid and invalid values {#styling_valid_and_invalid_values}

::: section-content
Valid and invalid values of a `<textarea>` element (e.g. those within,
and outside the bounds set by `minlength`, `maxlength`, or `required`)
can be highlighted using the
[`:valid`](https://developer.mozilla.org/en-US/docs/Web/CSS/:valid) and
[`:invalid`](https://developer.mozilla.org/en-US/docs/Web/CSS/:invalid)
pseudo-classes. For example, to give your textarea a different border
depending on whether it is valid or invalid:

::: code-example
[css]{.language-name}

``` {signature="N1OulE5MuoghhOvoxHx6yKJIuwQYHshO3FFMuoHpy2U=" data-language="css"}
textarea:invalid {
  border: 2px dashed red;
}

textarea:valid {
  border: 2px solid lime;
}
```
:::
:::

## Examples

### Basic example {#basic_example}

::: section-content
The following example shows a very simple textarea, with a set numbers
of rows and columns and some default content.

::: code-example
[html]{.language-name}

``` {signature="3xzEtcGNjkcxT2lYqEWT3Y2E4wDgoJnvVDp2lJx2pgU=" data-language="html"}
<textarea name="textarea" rows="10" cols="50">Write something here</textarea>
```
:::

#### Result

::: {#sect2 .code-example}
::: iframe
:::
:::
:::

### Example using \"minlength\" and \"maxlength\" {#example_using_minlength_and_maxlength}

::: section-content
This example has a minimum and maximum number of characters --- of 10
and 20 respectively. Try it and see.

::: code-example
[html]{.language-name}

``` {signature="t8iKj8NgWrolFZ7i29EfhPEnrDyIQ/lcPwDjqcLMjSc=" data-language="html"}
<textarea name="textarea" rows="5" cols="30" minlength="10" maxlength="20">
Write something here…
</textarea>
```
:::

#### Result {#result_2}

::: {#sect3 .code-example}
::: iframe
:::
:::

Note that `minlength` doesn\'t stop the user from removing characters so
that the number entered goes past the minimum, but it does make the
value entered into the `<textarea>` invalid. Also note that even if you
have a `minlength` value set (3, for example), an empty `<textarea>` is
still considered valid unless you also have the `required` attribute
set.
:::

### Example using \"placeholder\" {#example_using_placeholder}

::: section-content
This example has a placeholder set. Notice how it disappears when you
start typing into the box.

::: code-example
[html]{.language-name}

``` {signature="c8BLjCrmL4EJU3QGFI05qXHW6ARUF3NZsaGZ/Pk11MI=" data-language="html"}
<textarea
  name="textarea"
  rows="5"
  cols="30"
  placeholder="Comment text."></textarea>
```
:::

#### Result {#result_3}

::: {#sect4 .code-example}
::: iframe
:::
:::

::: {#sect5 .notecard .note}
**Note:** Placeholders should only be used to show an example of the
type of data that should be entered into a form; they are *not* a
substitute for a proper [`<label>`](label) element tied to the input.
See [`<input>` labels](input#labels) for a full explanation.
:::
:::

### Disabled and readonly {#disabled_and_readonly}

::: section-content
This example shows two `<textarea>`s --- one of which is `disabled`, and
one of which is `readonly`. Have a play with both and you\'ll see the
difference in behavior --- the `disabled` element is not selectable in
any way (and its value is not submitted), whereas the `readonly` element
is selectable and its contents copyable (and its value is submitted);
you just can\'t edit the contents.

::: {#sect6 .notecard .note}
**Note:** In browsers other than Firefox, such as chrome, the `disabled`
textarea content may be selectable and copyable.
:::

::: code-example
[html]{.language-name}

``` {signature="pPF6CDzabHrLb4EVAO8xnop4FGYhaJHn5zO0Qxsl2Bo=" data-language="html"}
<textarea name="textarea" rows="5" cols="30" disabled>
I am a disabled textarea.
</textarea>
<textarea name="textarea" rows="5" cols="30" readonly>
I am a read-only textarea.
</textarea>
```
:::

#### Result {#result_4}

::: {#sect7 .code-example}
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
<td><a href="../content_categories#flow_content">Flow content</a>, <a
href="../content_categories#phrasing_content">phrasing content</a>, <a
href="../content_categories#interactive_content">Interactive
content</a>, <a href="../content_categories#form_listed">listed</a>, <a
href="../content_categories#form_labelable">labelable</a>, <a
href="../content_categories#form_resettable">resettable</a>, and <a
href="../content_categories#form_submittable">submittable</a> <a
href="../content_categories#form-associated_">form-associated</a>
element.</td>
</tr>
<tr class="even">
<th scope="row">Permitted content</th>
<td>Text</td>
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
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/textbox_role"><code>textbox</code></a></td>
</tr>
<tr class="even">
<th scope="row">Permitted ARIA roles</th>
<td>No <code>role</code> permitted</td>
</tr>
<tr class="odd">
<th scope="row">DOM interface</th>
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLTextAreaElement"><code>HTMLTextAreaElement</code></a></td>
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
  the-textarea-element]{.small}](https://html.spec.whatwg.org/multipage/form-elements.html#the-textarea-element)

  ----------------------------------------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
  ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
                   Desktop                                                                                  Mobile                                                                                     
  ---------------- --------- ------ ------------------------------------------- ---------- ------- -------- --------- --------- ------------------------------------------- --------- ---------------- ----------
                   Chrome    Edge   Firefox                                     Internet   Opera   Safari   WebView   Chrome    Firefox for Android                         Opera     Safari on IOS    Samsung
                                                                                Explorer                    Android   Android                                               Android                    Internet

  `textarea`       1         12     1                                           Yes        ≤12.1   ≤4       4.4       18        4                                           ≤12.1     ≤3               1.0
                                                                                                                                                                                                       
                                    \[\"Before Firefox 6, when a `<textarea>`                                                   \[\"Before Firefox 6, when a `<textarea>`             Unlike other     
                                    was focused, the insertion point was placed                                                 was focused, the insertion point was placed           major browsers,  
                                    at the end of the text by default. Other                                                    at the end of the text by default. Other              a default style  
                                    major browsers place the insertion point at                                                 major browsers place the insertion point at           of               
                                    the beginning of the text.\", \"A default                                                   the beginning of the text.\", \"A default             `opacity: 0.4`   
                                    background-image gradient is applied to all                                                 background-image gradient is applied to all           is applied to    
                                    `<textarea>` elements, which can be                                                         `<textarea>` elements, which can be                   disabled         
                                    disabled using `background-image: none`.\",                                                 disabled using `background-image: none`.\",           `<textarea>`     
                                    \"Before Firefox 89, manipulating the                                                       \"Before Firefox 89, manipulating the                 elements.        
                                    content of `<textarea>` elements using                                                      content of `<textarea>` elements using                                 
                                    `Document.execCommand()` commands requires                                                  `Document.execCommand()` commands requires                             
                                    workarounds (see [bug                                                                       workarounds (see [bug                                                  
                                    1220696](https://bugzil.la/1220696)).\"\]                                                   1220696](https://bugzil.la/1220696)).\"\]                              

  `autocomplete`   66        79     59                                          No         53      9.1      66        66        59                                          47        9.3              9.0

  `cols`           1         12     1                                           ≤6         ≤12.1   ≤4       4.4       18        4                                           ≤12.1     ≤3.2             1.0

  `dirname`        17        79     116                                         No         ≤12.1   6        ≤37       18        116                                         ≤12.1     6                1.0

  `disabled`       1         12     1                                           ≤6         ≤12.1   ≤4       4.4       18        4                                           ≤12.1     ≤3.2             1.0

  `form`           1         12     1                                           ≤6         ≤12.1   ≤4       4.4       18        4                                           ≤12.1     ≤3.2             1.0

  `maxlength`      4         12     4                                           10         ≤12.1   5        ≤37       18        4                                           ≤12.1     5                1.0

  `minlength`      40        17     51                                          No         27      10.1     40        40        51                                          27        10.3             4.0

  `name`           1         12     1                                           ≤6         ≤12.1   ≤4       4.4       18        4                                           ≤12.1     ≤3.2             1.0

  `placeholder`    4         12     4                                           10         ≤12.1   5        ≤37       18        4                                           ≤12.1     5                1.0

  `readonly`       1         12     1                                           ≤6         ≤12.1   ≤4       4.4       18        4                                           ≤12.1     ≤3.2             1.0

  `required`       4         12     4                                           10         ≤12.1   5        ≤37       18        4                                           ≤12.1     5                1.0

  `rows`           1         12     1                                           ≤6         ≤12.1   ≤4       4.4       18        4                                           ≤12.1     ≤3.2             1.0

  `spellcheck`     9         12     2                                           Yes        15      5.1      4.4       18        4                                           14        5                1.0

  `wrap`           16        12     4                                           ≤6         ≤12.1   6        ≤37       18        4                                           ≤12.1     6                1.0
  ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
:::

## See also {#see_also}

::: section-content
Other form-related elements:

-   [`<form>`](form)
-   [`<button>`](button)
-   [`<datalist>`](datalist)
-   [`<legend>`](legend)
-   [`<label>`](label)
-   [`<select>`](select)
-   [`<optgroup>`](optgroup)
-   [`<option>`](option)
-   [`<input>`](input)
-   [`<fieldset>`](fieldset)
-   [`<output>`](output)
-   [`<progress>`](progress)
-   [`<meter>`](meter)
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Element/textarea](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/textarea){._attribution-link}
:::
