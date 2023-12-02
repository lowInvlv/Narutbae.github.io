

# \<input type=\"datetime-local\"\>



::: section-content
[`<input>`](../input) elements of type `datetime-local` create input
controls that let the user easily enter both a date and a time,
including the year, month, and day as well as the time in hours and
minutes.
:::

## Try it {#try_it}

::: section-content
::: iframe
::: {.output-header .border-rounded-top}
#### HTML Demo: \<input type=\"datetime-local\"\> {#html-demo-input-typedatetime-local .output-heading}

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
    <label for="meeting-time">Choose a time for your appointment:</label>

    <input
      type="datetime-local"
      id="meeting-time"
      name="meeting-time"
      value="2018-06-12T19:30"
      min="2018-06-07T00:00"
      max="2018-06-14T00:00" />
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

The control\'s UI varies in general from browser to browser. In browsers
with no support, these degrade gracefully to simple
[`<input type="text">`](text) controls.

The control is intended to represent *a local date and time*, not
necessarily *the user\'s local date and time*. In other words, the input
allows any valid combination of year, month, day, hour, and
minute---even if such a combination is invalid in the user\'s local time
zone (such as the one hour within a daylight saving time spring-forward
transition gap).
:::

## Value

::: section-content
A string representing the value of the date entered into the input. The
format of the date and time value used by this input type is described
in [Local date and time
strings](../../date_and_time_formats#local_date_and_time_strings).

You can set a default value for the input by including a date and time
inside the [`value`](../input#value) attribute, like so:

::: code-example
[html]{.language-name}

``` {signature="kwZ/uT1FjSSLcKvvuJpJxgun07zIin9Z9Yr5P+dBY48=" data-language="html"}
<label for="party">Enter a date and time for your party booking:</label>
<input
  id="party"
  type="datetime-local"
  name="partydate"
  value="2017-06-01T08:30" />
```
:::

::: {#sect1 .code-example}
::: iframe
:::
:::

One thing to note is that the displayed date and time formats differ
from the actual `value`; the displayed date and time are formatted
according to the user\'s locale as reported by their operating system,
whereas the date/time `value` is always formatted `YYYY-MM-DDThh:mm`.
When the above value is submitted to the server, for example, it will
look like `partydate=2024-06-01T08:30`.

::: {#sect2 .notecard .note}
**Note:** Also bear in mind that if such data is submitted via HTTP
[`GET`](https://developer.mozilla.org/en-US/docs/Web/HTTP/Methods/GET),
the colon character will need to be escaped for inclusion in the URL
parameters, e.g. `partydate=2024-06-01T08%3A30`. See
[`encodeURI()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/encodeURI)
for one way to do this.
:::

You can also get and set the date value in JavaScript using the
[`HTMLInputElement`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLInputElement)
`value` property, for example:

::: code-example
[js]{.language-name}

``` {signature="nlVjs+FdRTmymC4zaX6jlC3lsvwYXtcryOjj1GE5yZI=" data-language="js"}
const dateControl = document.querySelector('input[type="datetime-local"]');
dateControl.value = "2017-06-01T08:30";
```
:::
:::

## Additional attributes {#additional_attributes}

::: section-content
In addition to the attributes common to all [`<input>`](../input)
elements, `datetime-local` inputs offer the following attributes.
:::

### max

::: section-content
The latest date and time to accept. If the [`value`](../input#value)
entered into the element is later than this timestamp, the element fails
[constraint validation](../../constraint_validation). If the value of
the `max` attribute isn\'t a valid string that follows the format
`YYYY-MM-DDThh:mm`, then the element has no maximum value.

This value must specify a date string later than or equal to the one
specified by the `min` attribute.
:::

### min

::: section-content
The earliest date and time to accept; timestamps earlier than this will
cause the element to fail [constraint
validation](../../constraint_validation). If the value of the `min`
attribute isn\'t a valid string that follows the format
`YYYY-MM-DDThh:mm`, then the element has no minimum value.

This value must specify a date string earlier than or equal to the one
specified by the `max` attribute.
:::

### step

::: section-content
The `step` attribute is a number that specifies the granularity that the
value must adhere to, or the special value `any`, which is described
below. Only values which are equal to the basis for stepping
([`min`](#min) if specified, [`value`](../input#value) otherwise, and an
appropriate default value if neither of those is provided) are valid.

A string value of `any` means that no stepping is implied, and any value
is allowed (barring other constraints, such as [`min`](#min) and
[`max`](#max)).

::: {#sect3 .notecard .note}
**Note:** When the data entered by the user doesn\'t adhere to the
stepping configuration, the [user
agent](https://developer.mozilla.org/en-US/docs/Glossary/User_agent) may
round to the nearest valid value, preferring numbers in the positive
direction when there are two equally close options.
:::

For `datetime-local` inputs, the value of `step` is given in seconds,
with a scaling factor of 1000 (since the underlying numeric value is in
milliseconds). The default value of `step` is 60, indicating 60 seconds
(or 1 minute, or 60,000 milliseconds).

*At this time, it\'s unclear what a value of `any` means for `step` when
used with `datetime-local` inputs. This will be updated as soon as that
information is determined.*
:::

## Using datetime-local inputs {#using_datetime-local_inputs}

::: section-content
Date/time inputs are convenient for the developer; they provide an easy
UI for choosing dates and times, and they normalize the data format sent
to the server, regardless of the user\'s locale. However, it is
important to consider your users. Don\'t require your users to enter
data that is not needed for your app to function.
:::

### Controlling input size {#controlling_input_size}

::: section-content
`<input type="datetime-local">` doesn\'t support form control sizing
attributes such as [`size`](../input#size). You\'ll have to resort to
[CSS](https://developer.mozilla.org/en-US/docs/Web/CSS) for customizing
the sizes of these elements.
:::

### Setting timezones {#setting_timezones}

::: section-content
One thing the `datetime-local` input type doesn\'t provide is a way to
set the time zone and/or locale of the date/time control. This was
available in the `datetime` input type, but this type is now obsolete,
having been removed from the spec. The main reasons why this was removed
are a lack of implementation in browsers and concerns over the user
interface/experience. It is easier to just have a control (or controls)
for setting the date/time and then deal with the locale in a separate
control.

For example, if you are creating a system where the user is likely to
already be logged in, with their locale already set, you could provide
the timezone in a [`hidden`](hidden) input type. For example:

::: code-example
[html]{.language-name}

``` {signature="ef9KIX+FOM+T+G9HJMBPyM5dyf/HomTirSF24wLA2sA=" data-language="html"}
<input type="hidden" id="timezone" name="timezone" value="-08:00" />
```
:::

On the other hand, if you were required to allow the user to enter a
time zone along with a date/time input, you could have a
[`<select>`](../select) element to enable the user to set the right time
zone by choosing a particular location from among a set of locations:

::: code-example
[html]{.language-name}

``` {signature="F94VbTaqRpjqkyn9IbEcl2SXN5T/B76nyEZR9WGH2/8=" data-language="html"}
<select name="timezone" id="timezone">
  <option value="Pacific/Kwajalein">Eniwetok, Kwajalein</option>
  <option value="Pacific/Midway">Midway Island, Samoa</option>
  <option value="Pacific/Honolulu">Hawaii</option>
  <option value="Pacific/Marquesas">Taiohae</option>
  <!-- and so on -->
</select>
```
:::

In either case, the date/time and time zone values would be submitted to
the server as separate data points, and then you\'d need to store them
appropriately in the database on the server-side.
:::

## Validation

::: section-content
By default, `<input type="datetime-local">` does not apply any
validation to entered values. The UI implementations generally don\'t
let you enter anything that isn\'t a date/time --- which is helpful ---
but a user might still fill in no value and submit, or enter an invalid
date and/or time (e.g. the 32nd of April).

You can use [`min`](../input#min) and [`max`](../input#max) to restrict
the available dates (see [Setting maximum and minimum
dates](#setting_maximum_and_minimum_dates)), and you can use the
[`required`](../input#required) attribute to make filling in the
date/time mandatory. As a result, supporting browsers will display an
error if you try to submit a date that is outside the set bounds or an
empty date field.

Let\'s look at an example; here we\'ve set minimum and maximum date/time
values, and also made the field required:

::: code-example
[html]{.language-name}

``` {signature="corPgpDZ5O2oxNe8+g0Zn5OwnZ4GW3x8jetxP5ThLB4=" data-language="html"}
<form>
  
    <label for="party">
      Choose your preferred party date and time (required, June 1st 8.30am to
      June 30th 4.30pm):
    </label>
    <input
      id="party"
      type="datetime-local"
      name="partydate"
      min="2017-06-01T08:30"
      max="2017-06-30T16:30"
      required />
    <span class="validity"></span>
  
  
    <input type="submit" value="Book party!" />
  
</form>
```
:::

If you try to submit the form with an incomplete date (or with a date
outside the set bounds), the browser displays an error. Try playing with
the example now:

::: {#sect4 .code-example}
::: iframe
:::
:::

Here\'s the CSS used in the above example. Here we make use of the
[`:valid`](https://developer.mozilla.org/en-US/docs/Web/CSS/:valid) and
[`:invalid`](https://developer.mozilla.org/en-US/docs/Web/CSS/:invalid)
CSS properties to style the input based on whether the current value is
valid. We put the icons on a [`<span>`](../span) next to the input.

::: code-example
[css]{.language-name}

``` {signature="2eZkvfBs8/bDWnklRDJmX3FAUPNJelJw8hEyRehs7dc=" data-language="css"}
div {
  margin-bottom: 10px;
  display: flex;
  align-items: center;
}

label {
  display: inline-block;
  width: 300px;
}

input:invalid + span::after {
  content: "✖";
  padding-left: 5px;
}

input:valid + span::after {
  content: "✓";
  padding-left: 5px;
}
```
:::

::: {#sect5 .notecard .warning}
**Warning:** HTML form validation is *not* a substitute for scripts that
ensure that the entered data is in the proper format. It\'s far too easy
for someone to make adjustments to the HTML that allow them to bypass
the validation, or to remove it entirely. It\'s also possible for
someone to bypass your HTML entirely and submit the data directly to
your server. If your server-side code fails to validate the data it
receives, problems can arise when improperly-formatted data is submitted
(or data that is too large, is of the wrong type, and so forth).
:::

::: {#sect6 .notecard .note}
**Note:** With a `datetime-local` input, the date value is always
normalized to the format `YYYY-MM-DDThh:mm`.
:::
:::

## Examples

### Basic uses of datetime-local {#basic_uses_of_datetime-local}

::: section-content
The simplest use of `<input type="datetime-local">` involves a basic
`<input>` and [`<label>`](../label) element combination, as seen below:

::: code-example
[html]{.language-name}

``` {signature="DZvxt+CVOfipn69TBi+o0Bo8zHJtHGwmd7r1bFnQInk=" data-language="html"}
<form>
  <label for="party">Enter a date and time for your party booking:</label>
  <input id="party" type="datetime-local" name="partydate" />
</form>
```
:::

::: {#sect7 .code-example}
::: iframe
:::
:::
:::

### Setting maximum and minimum dates and times {#setting_maximum_and_minimum_dates_and_times}

::: section-content
You can use the [`min`](../input#min) and [`max`](../input#max)
attributes to restrict the dates/times that can be chosen by the user.
In the following example, we are setting a minimum datetime of
`2024-06-01T08:30` and a maximum datetime of `2024-06-30T16:30`:

::: code-example
[html]{.language-name}

``` {signature="QOF6UCB7v76GsCDKdT+yy/bB7vHnqmooQC4q3vpCROk=" data-language="html"}
<form>
  <label for="party">Enter a date and time for your party booking:</label>
  <input
    id="party"
    type="datetime-local"
    name="partydate"
    min="2024-06-01T08:30"
    max="2024-06-30T16:30" />
</form>
```
:::

::: {#sect8 .code-example}
::: iframe
:::
:::

Only days in June 2024 can be selected. Depending on what browser you
are using, times outside the specified values might not be selectable.
In other browsers, invalid dates and times are selectable but will match
[`:invalid`](https://developer.mozilla.org/en-US/docs/Web/CSS/:invalid)
and
[`:out-of-range`](https://developer.mozilla.org/en-US/docs/Web/CSS/:out-of-range)
and will fail [validation](#validation).

In some browsers (Chrome and Edge), only the \"days\" part of the date
value will be editable, and dates outside June can\'t be scrolled. In
others (Safari), the date picker will appear to allow any date, but the
value will be clamped to the valid range when a date is selected.

The valid range included all times between the `min` and `max` values;
the time of day is only constrained on the first and last dates in the
range.

::: {#sect9 .notecard .note}
**Note:** You should be able to use the [`step`](../input#step)
attribute to vary the number of days jumped each time the date is
incremented (e.g. maybe you only want to make Saturdays selectable).
However, this does not seem to work effectively in any implementation at
the time of writing.
:::
:::

## Technical summary {#technical_summary}

::: section-content
<figure class="table-container">
<div class="_table">
<table class="properties">
<tbody>
<tr class="odd">
<td><strong><a href="#value">Value</a></strong></td>
<td>A string representing a date and time (in the local time zone), or
empty.</td>
</tr>
<tr class="even">
<td><strong>Events</strong></td>
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/change_event"><code>change</code></a>
and <a
href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/input_event"><code>input</code></a></td>
</tr>
<tr class="odd">
<td><strong>Supported common attributes</strong></td>
<td><a href="../input#autocomplete"><code>autocomplete</code></a>, <a
href="../input#list"><code>list</code></a>, <a
href="../input#readonly"><code>readonly</code></a>, and <a
href="../input#step"><code>step</code></a></td>
</tr>
<tr class="even">
<td><strong>IDL attributes</strong></td>
<td><code>list</code>, <code>value</code>,
<code>valueAsNumber</code>.</td>
</tr>
<tr class="odd">
<td><strong>DOM interface</strong></td>
<td><p><a
href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLInputElement"><code>HTMLInputElement</code></a></p></td>
</tr>
<tr class="even">
<td><strong>Methods</strong></td>
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLInputElement/select"><code>select()</code></a>,
<a
href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLInputElement/stepDown"><code>stepDown()</code></a>,
<a
href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLInputElement/stepUp"><code>stepUp()</code></a></td>
</tr>
<tr class="odd">
<td><strong>Implicit ARIA Role</strong></td>
<td><a href="https://www.w3.org/TR/html-aria/#dfn-no-corresponding-role"
target="_blank"><code>no corresponding role</code></a></td>
</tr>
</tbody>
</table>

</figure>
:::

## Specifications

::: _table
  --------------------------------------------------------------------------------------------------------------------------------------------------------------
  Specification
  --------------------------------------------------------------------------------------------------------------------------------------------------------------
  [HTML Standard\
  [\#
  local-date-and-time-state-(type=datetime-local)]{.small}](https://html.spec.whatwg.org/multipage/input.html#local-date-and-time-state-(type=datetime-local))

  --------------------------------------------------------------------------------------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
                     Desktop                                                         Mobile                                                                                   
  ------------------ --------- ------ --------- ------------------- ------- -------- ----------------- ---------------- --------------------- --------------- --------------- ------------------
                     Chrome    Edge   Firefox   Internet Explorer   Opera   Safari   WebView Android   Chrome Android   Firefox for Android   Opera Android   Safari on IOS   Samsung Internet
  `datetime-local`   20        12     93        No                  11      14.1     4.4               25               93                    11              5               1.5
:::

## See also {#see_also}

::: section-content
-   The generic [`<input>`](../input) element and the interface used to
    manipulate it,
    [`HTMLInputElement`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLInputElement)
-   [`<input type="date">`](date) and [`<input type="time">`](time)
-   [Date and time formats used in HTML](../../date_and_time_formats)
-   [Date and Time picker
    tutorial](https://developer.mozilla.org/en-US/docs/Learn/Forms/Basic_native_form_controls#date_and_time_picker)
-   [Compatibility of CSS
    properties](https://developer.mozilla.org/en-US/docs/Learn/Forms/Property_compatibility_table_for_form_controls)
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/datetime-local](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/datetime-local){._attribution-link}
:::
