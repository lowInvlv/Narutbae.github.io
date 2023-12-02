

# \<input type=\"range\"\>



::: section-content
[`<input>`](../input) elements of type `range` let the user specify a
numeric value which must be no less than a given value, and no more than
another given value. The precise value, however, is not considered
important. This is typically represented using a slider or dial control
rather than a text entry box like the [number](number) input type.

Because this kind of widget is imprecise, it should only be used if the
control\'s exact value isn\'t important.
:::

## Try it {#try_it}

::: section-content
::: iframe
::: {.output-header .border-rounded-top}
#### HTML Demo: \<input type=\"range\"\> {#html-demo-input-typerange .output-heading}

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
    <p>Audio settings:</p>

    
      <input type="range" id="volume" name="volume" min="0" max="11" />
      <label for="volume">Volume</label>
    

    
      <input type="range" id="cowbell" name="cowbell" min="0" max="100" value="90" step="10" />
      <label for="cowbell">Cowbell</label>
    
:::
:::

::: {#css-panel .section .hidden tabindex="0" role="tabpanel" aria-labelledby="css" aria-hidden="true"}
::: {#css-editor}
    p,
    label {
      font:
        1rem 'Fira Sans',
        sans-serif;
    }

    input {
      margin: 0.4rem;
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

If the user\'s browser doesn\'t support type `range`, it will fall back
and treat it as a [`text`](text) input.
:::

### Validation

::: section-content
There is no pattern validation available; however, the following forms
of automatic validation are performed:

-   If the [`value`](../input#value) is set to something which can\'t be
    converted into a valid floating-point number, validation fails
    because the input is suffering from a bad input.
-   The value won\'t be less than [`min`](../input#min). The default is
    0.
-   The value won\'t be greater than [`max`](../input#max). The default
    is 100.
-   The value will be a multiple of [`step`](../input#step). The default
    is 1.
:::

### Value

::: section-content
The [`value`](../input#value) attribute contains a string which contains
a string representation of the selected number. The value is never an
empty string (`""`). The default value is halfway between the specified
minimum and maximum---unless the maximum is actually less than the
minimum, in which case the default is set to the value of the `min`
attribute. The algorithm for determining the default value is:

::: code-example
[js]{.language-name}

``` {signature="s0YJHxSrqtIfl3E7CsMpoqjj0V6S+Q868hUb2UVV41M=" data-language="js"}
defaultValue =
  rangeElem.max < rangeElem.min
    ? rangeElem.min
    : rangeElem.min + (rangeElem.max - rangeElem.min) / 2;
```
:::

If an attempt is made to set the value lower than the minimum, it is set
to the minimum. Similarly, an attempt to set the value higher than the
maximum results in it being set to the maximum.
:::

## Additional attributes {#additional_attributes}

::: section-content
In addition to the attributes shared by all [`<input>`](../input)
elements, range inputs offer the following attributes.
:::

### list

::: section-content
The value of the `list` attribute is the
[`id`](https://developer.mozilla.org/en-US/docs/Web/API/Element/id) of a
[`<datalist>`](../datalist) element located in the same document. The
[`<datalist>`](../datalist) provides a list of predefined values to
suggest to the user for this input. Any values in the list that are not
compatible with the [`type`](../input#type) are not included in the
suggested options. The values provided are suggestions, not
requirements: users can select from this predefined list or provide a
different value.

See the [adding tick marks](#adding_tick_marks) below for an example of
how the options on a range are denoted in supported browsers.
:::

### max

::: section-content
The greatest value in the range of permitted values. If the
[`value`](../input#value) entered into the element exceeds this, the
element fails [constraint validation](../../constraint_validation). If
the value of the [`max`](../../attributes/max) attribute isn\'t a
number, then the element has no maximum value.

This value must be greater than or equal to the value of the
[`min`](../../attributes/min) attribute. See the HTML
[`max`](../../attributes/max) attribute.
:::

### min

::: section-content
The lowest value in the range of permitted values. If the
[`value`](../input#value) of the element is less than this, the element
fails [constraint validation](../../constraint_validation). If a value
is specified for `min` that isn\'t a valid number, the input has no
minimum value.

This value must be less than or equal to the value of the
[`max`](../../attributes/max) attribute. See the HTML
[`min`](../../attributes/min) attribute.

::: {#sect1 .notecard .note}
**Note:** If the `min` and `max` values are equal or the `max` value is
lower than the `min` value the user will not be able to interact with
the range.
:::
:::

### step

::: section-content
The `step` attribute is a number that specifies the granularity that the
value must adhere to. Only values that match the specified stepping
interval ([`min`](#min) if specified, [`value`](../input#value)
otherwise, or an appropriate default value if neither of those is
provided) are valid.

The `step` attribute can also be set to the `any` string value. This
`step` value means that no stepping interval is implied and any value is
allowed in the specified range (barring other constraints, such as
[`min`](#min) and [`max`](#max)). See the [Setting step to the `any`
value](#setting_step_to_the_any_value) example for how this works in
supported browsers.

::: {#sect2 .notecard .note}
**Note:** When the value entered by a user doesn\'t adhere to the
stepping configuration, the [user
agent](https://developer.mozilla.org/en-US/docs/Glossary/User_agent) may
round off the value to the nearest valid value, preferring to round
numbers up when there are two equally close options.
:::

The default stepping value for `range` inputs is 1, allowing only
integers to be entered, *unless* the stepping base is not an integer;
for example, if you set `min` to -10 and `value` to 1.5, then a `step`
of 1 will allow only values such as 1.5, 2.5, 3.5,... in the positive
direction and -0.5, -1.5, -2.5,... in the negative direction. See the
[HTML `step` attribute](../../attributes/step).
:::

## Non-standard Attributes {#non-standard_attributes}

### orient

::: section-content
Similar to the -moz-orient non-standard CSS property impacting the
[`<progress>`](../progress) and [`<meter>`](../meter) elements, the
`orient` attribute defines the orientation of the range slider. Values
include `horizontal`, meaning the range is rendered horizontally, and
`vertical`, where the range is rendered vertically.

::: {#sect3 .notecard .note}
**Note:** The following input attributes do not apply to the input
range: `accept`, `alt`, `checked`, `dirname`, `formaction`,
`formenctype`, `formmethod`, `formnovalidate`, `formtarget`, `height`,
`maxlength`, `minlength`, `multiple`, `pattern`, `placeholder`,
`readonly`, `required`, `size`, and `src`. Any of these attributes, if
included, will be ignored.
:::
:::

## Examples

::: section-content
While the `number` type lets users enter a number with optional
constraints forcing their value to be between a minimum and a maximum
value, it does require that they enter a specific value. The `range`
input type lets you ask the user for a value in cases where the user may
not even care---or know---what the specific numeric value selected is.

A few examples of situations in which range inputs are commonly used:

-   Audio controls such as volume and balance, or filter controls.
-   Color configuration controls such as color channels, transparency,
    brightness, etc.
-   Game configuration controls such as difficulty, visibility distance,
    world size, and so forth.
-   Password length for a password manager\'s generated passwords.

As a rule, if the user is more likely to be interested in the percentage
of the distance between minimum and maximum values than the actual
number itself, a range input is a great candidate. For example, in the
case of a home stereo volume control, users typically think \"set volume
at halfway to maximum\" instead of \"set volume to 0.5\".
:::

### Specifying the minimum and maximum {#specifying_the_minimum_and_maximum}

::: section-content
By default, the minimum is 0 and the maximum is 100. If that\'s not what
you want, you can easily specify different bounds by changing the values
of the [`min`](../input#min) and/or [`max`](../input#max) attributes.
These can be any floating-point value.

For example, to ask the user for a value between -10 and 10, you can
use:

::: code-example
[html]{.language-name}

``` {signature="61WSkGGyXk8u/sQdktXVjpFi3iZwLrFpdM4kKoHikL4=" data-language="html"}
<input type="range" min="-10" max="10" />
```
:::

::: {#sect4 .code-example}
::: iframe
:::
:::
:::

### Setting the value\'s granularity {#setting_the_values_granularity}

::: section-content
By default, the granularity is 1, meaning the value is always an
integer. To control the granularity, you can change the
[`step`](../input#step) attribute. For example, If you need a value to
be halfway between 5 and 10, you should set the value of `step` to 0.5:

#### Setting the step attribute {#setting_the_step_attribute}

::: code-example
[html]{.language-name}

``` {signature="RCETPs5lHxENwLew/431FgB7OdLvdmP5IUb+uLW1s5o=" data-language="html"}
<input type="range" min="5" max="10" step="0.5" />
```
:::

::: {#sect5 .code-example}
::: iframe
:::
:::

#### Setting step to \"any\" {#setting_step_to_any}

If you want to accept any value regardless of how many decimal places it
extends to, you can specify a value of `any` for the
[`step`](../input#step) attribute:

##### HTML

::: code-example
[html]{.language-name}

``` {signature="r+ZJhIMO14e+VyMp2xGpbY0SXGIRlBJ6eJpKGHXO7uA=" data-language="html"}
<input id="pi_input" type="range" min="0" max="3.14" step="any" />
<p>Value: <output id="value"></output></p>
```
:::

##### JavaScript

::: code-example
[js]{.language-name}

``` {signature="cQHNeG2dtOemQmBYUM3Aj2Ws6K76Cq1Za9GIXIIt810=" data-language="js"}
const value = document.querySelector("#value");
const input = document.querySelector("#pi_input");
value.textContent = input.value;
input.addEventListener("input", (event) => {
  value.textContent = event.target.value;
});
```
:::

::: {#sect6 .code-example}
::: iframe
:::
:::

This example lets the user select any value between 0 and π without any
restriction on the fractional part of the value selected. JavaScript is
used to show how the value changes as the user interacts with the range.
:::

### Adding tick marks {#adding_tick_marks}

::: section-content
To add tick marks to a range control, include the `list` attribute,
giving it the `id` of a [`<datalist>`](../datalist) element which
defines a series of tick marks on the control. Each point is represented
using an [`<option>`](../option) element with its
[`value`](../option#value) set to the range\'s value at which a mark
should be drawn.

#### HTML {#html_2}

::: code-example
[html]{.language-name}

``` {signature="MruCcANpMskjStC9xQAVNxzQ1EFSqQDDrTDn+HYcdsY=" data-language="html"}
<label for="temp">Choose a comfortable temperature:</label><br />
<input type="range" id="temp" name="temp" list="markers" />

<datalist id="markers">
  <option value="0"></option>
  <option value="25"></option>
  <option value="50"></option>
  <option value="75"></option>
  <option value="100"></option>
</datalist>
```
:::

#### Result

::: {#sect7 .code-example}
::: iframe
:::
:::
:::

### Using the same datalist for multiple range controls {#using_the_same_datalist_for_multiple_range_controls}

::: section-content
To help you from repeating code you can reuse that same
[`<datalist>`](../datalist) for multiple `<input type="range">`
elements, and other [`<input>`](../input) types.

::: {#sect8 .notecard .note}
**Note:** If you also want to [show the labels](#adding_labels) as in
the example below then you would need a `datalist` for each range input.
:::

#### HTML {#html_3}

::: code-example
[html]{.language-name}

``` {signature="EfTIISSTx0DO++c8Qzmr2pGJUk6zze1FdEt8NCE6dwg=" data-language="html"}
<p>
  <label for="temp1">Temperature for room 1:</label>
  <input type="range" id="temp1" name="temp1" list="values" />
</p>
<p>
  <label for="temp2">Temperature for room 2:</label>
  <input type="range" id="temp2" name="temp2" list="values" />
</p>

<p>
  <label for="temp3">Temperature for room 3:</label>
  <input type="range" id="temp3" name="temp3" list="values" />
</p>

<datalist id="values">
  <option value="0" label="0"></option>
  <option value="25" label="25"></option>
  <option value="50" label="50"></option>
  <option value="75" label="75"></option>
  <option value="100" label="100"></option>
</datalist>
```
:::

#### Result {#result_2}

::: {#sect9 .code-example}
::: iframe
:::
:::
:::

### Adding labels {#adding_labels}

::: section-content
You can label tick marks by giving the `<option>` elements `label`
attributes. However, the label content will not be displayed by default.
You can use CSS to show the labels and to position them correctly.
Here\'s one way you could do this.

#### HTML {#html_4}

::: code-example
[html]{.language-name}

``` {signature="r//H/j3KZ8Q137NLCpekHOAWBCqMxHrtrKaqIKdKfBs=" data-language="html"}
<label for="tempB">Choose a comfortable temperature:</label><br />
<input type="range" id="tempB" name="temp" list="values" />

<datalist id="values">
  <option value="0" label="very cold!"></option>
  <option value="25" label="cool"></option>
  <option value="50" label="medium"></option>
  <option value="75" label="getting warm!"></option>
  <option value="100" label="hot!"></option>
</datalist>
```
:::

#### CSS

::: code-example
[css]{.language-name}

``` {signature="4YiKFCF1vnbAmSqlnYxHLlwg2qZL6+e/h3001DS/OUg=" data-language="css"}
datalist {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  writing-mode: vertical-lr;
  width: 200px;
}

option {
  padding: 0;
}

input[type="range"] {
  width: 200px;
  margin: 0;
}
```
:::

#### Result {#result_3}

::: {#sect10 .code-example}
::: iframe
:::
:::
:::

### Creating vertical range controls {#creating_vertical_range_controls}

::: section-content
By default, browsers render range inputs as sliders with the knob
sliding left and right.

To create a vertical range, wherein the knob slides up and down, set the
CSS
[`appearance`](https://developer.mozilla.org/en-US/docs/Web/CSS/appearance)
property to `slider-vertical` and include the non-standard `orient`
attribute for Firefox.

#### Horizontal range control {#horizontal_range_control}

Consider this range control:

::: code-example
[html]{.language-name}

``` {signature="PZmCPbB1GsVAASr2aRI0j1y/EPHrOJFK5+C6t8t6vxs=" data-language="html"}
<input type="range" id="volume" min="0" max="11" value="7" step="1" />
```
:::

::: {#sect11 .code-example}
::: iframe
:::
:::

This control is horizontal (at least on most if not all major browsers;
others might vary).

#### Using the appearance property {#using_the_appearance_property}

The
[`appearance`](https://developer.mozilla.org/en-US/docs/Web/CSS/appearance)
property has a non-standard value of `slider-vertical` that, well, makes
sliders vertical.

We use the same HTML as in the previous examples:

::: code-example
[html]{.language-name}

``` {signature="RahzzulggSYi1Ost/ooaNF6DCMPtuVUjJ2Fd3DEpD/w=" data-language="html"}
<input type="range" min="0" max="11" value="7" step="1" />
```
:::

We target just the inputs with a type of range:

::: code-example
[css]{.language-name}

``` {signature="TFcTUtS3OJ5oP8mZkRuL7LxeM2YjSv8gSi/N0Iphmbg=" data-language="css"}
input[type="range"] {
  appearance: slider-vertical;
}
```
:::

::: {#sect12 .code-example}
::: iframe
:::
:::

#### Using the orient attribute {#using_the_orient_attribute}

In Firefox only, there is a non-standard `orient` property.

Use similar HTML as in the previous examples, we add the attribute with
a value of `vertical`:

::: code-example
[html]{.language-name}

``` {signature="Dln5U7nm8y1vVFMTpVJFoc87O4j/ydMQrAX4BlpttQ8=" data-language="html"}
<input type="range" min="0" max="11" value="7" step="1" orient="vertical" />
```
:::

::: {#sect13 .code-example}
::: iframe
:::
:::

#### writing-mode: bt-lr {#writing-mode_bt-lr}

The
[`writing-mode`](https://developer.mozilla.org/en-US/docs/Web/CSS/writing-mode)
property should generally not be used to alter text direction for
internationalization or localization purposes, but can be used for
special effects.

We use the same HTML as in the previous examples:

::: code-example
[html]{.language-name}

``` {signature="RahzzulggSYi1Ost/ooaNF6DCMPtuVUjJ2Fd3DEpD/w=" data-language="html"}
<input type="range" min="0" max="11" value="7" step="1" />
```
:::

We target just the inputs with a type of range, changing the writing
mode from the default to `bt-lr`, or bottom-to-top and left-to-right:

::: code-example
[css]{.language-name}

``` {signature="sBW+AMa57Jt1O9yXtadvV8QWXxJVW3pTtdxz2mRn1A0=" data-language="css"}
input[type="range"] {
  writing-mode: bt-lr;
}
```
:::

::: {#sect14 .code-example}
::: iframe
:::
:::

#### Putting it all together {#putting_it_all_together}

As each of the above examples works in different browsers, you can put
all of them in a single example to make it work cross browser:

We keep the `orient` attribute with a value of `vertical` for Firefox:

::: code-example
[html]{.language-name}

``` {signature="Dln5U7nm8y1vVFMTpVJFoc87O4j/ydMQrAX4BlpttQ8=" data-language="html"}
<input type="range" min="0" max="11" value="7" step="1" orient="vertical" />
```
:::

We target just the `input`s with a `type` of `range` and `orient` set to
`vertical`, changing the `writing-mode` from the default to `bt-lr`, or
bottom-to-top and left-to-right, for pre-Blink versions of Edge, and add
`appearance: slider-vertical` which is supported in Blink and Webkit
browsers:

::: code-example
[css]{.language-name}

``` {signature="uqTcM2RazaWjFY4wqrabir4SdK2PHCYdl5ICo+++lMc=" data-language="css"}
input[type="range"][orient="vertical"] {
  writing-mode: bt-lr;
  appearance: slider-vertical;
}
```
:::

::: {#sect15 .code-example}
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
<td><strong><a href="#value">Value</a></strong></td>
<td>A string containing the string representation of the selected
numeric value; use <span
class="page-not-created"><code>valueAsNumber</code></span> to get the
value as a number.</td>
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
href="../input#max"><code>max</code></a>, <a
href="../input#min"><code>min</code></a>, and <a
href="../input#step"><code>step</code></a></td>
</tr>
<tr class="even">
<td><strong>IDL attributes</strong></td>
<td><code>list</code>, <code>value</code>, and
<code>valueAsNumber</code></td>
</tr>
<tr class="odd">
<td><strong>DOM interface</strong></td>
<td><p><a
href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLInputElement"><code>HTMLInputElement</code></a></p></td>
</tr>
<tr class="even">
<td><strong>Methods</strong></td>
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLInputElement/stepDown"><code>stepDown()</code></a>
and <a
href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLInputElement/stepUp"><code>stepUp()</code></a></td>
</tr>
<tr class="odd">
<td><strong>Implicit ARIA Role</strong></td>
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/slider_role"><code>slider</code></a></td>
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
  range-state-(type=range)]{.small}](https://html.spec.whatwg.org/multipage/input.html#range-state-(type=range))

  ----------------------------------------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
  ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
                           Desktop                                                                                                                                                                           Mobile                                                                                                                                                                    
  ------------------------ --------------------------------------- ----------------------- --------- ----------------------- --------------------------------------- --------------------------------------- --------------------------------------- --------------------------------------- --------- --------------------------------------- --------------------------------------- ---------------------------------------
                           Chrome                                  Edge                    Firefox   Internet Explorer       Opera                                   Safari                                  WebView Android                         Chrome Android                          Firefox   Opera Android                           Safari on IOS                           Samsung Internet
                                                                                                                                                                                                                                                                                             for                                                                                       
                                                                                                                                                                                                                                                                                             Android                                                                                   

  `range`                  4                                       12                      23        10                      11                                      3.1                                     4.4                                     57                                      52        11                                      5                                       7.0
                                                                                                                                                                                                                                                                                                                                                                                       
                                                                                                                                                                                                             2--4.4                                                                                                                                                                    
                                                                                                                                                                                                                                                                                                                                                                                       
                                                                                                                                                                                                             Pre-Chromium Android WebView recognizes                                                                                                                                   
                                                                                                                                                                                                             the `range` type, but doesn\'t                                                                                                                                            
                                                                                                                                                                                                             implement a range-specific control.                                                                                                                                       

  `tick_marks`             Yes                                     ≤79                     109       No                      Yes                                     12.1                                    Yes                                     Yes                                     109       Yes                                     12.2                                    Yes

  `vertical_orientation`   Yes                                     12                      No        10                      Yes                                     Yes                                     Yes                                     Yes                                     No        Yes                                     Yes                                     Yes
                                                                                                                                                                                                                                                                                                                                                                                       
                           The slider can be oriented vertically   The slider can be                 The slider can be       The slider can be oriented vertically   The slider can be oriented vertically   The slider can be oriented vertically   The slider can be oriented vertically             The slider can be oriented vertically   The slider can be oriented vertically   The slider can be oriented vertically
                           by setting the non-standard             oriented vertically by            oriented vertically by  by setting the non-standard             by setting the non-standard             by setting the non-standard             by setting the non-standard                       by setting the non-standard             by setting the non-standard             by setting the non-standard
                           `-webkit-appearance: slider-vertical`   setting the                       setting the             `-webkit-appearance: slider-vertical`   `-webkit-appearance: slider-vertical`   `-webkit-appearance: slider-vertical`   `-webkit-appearance: slider-vertical`             `-webkit-appearance: slider-vertical`   `-webkit-appearance: slider-vertical`   `-webkit-appearance: slider-vertical`
                           style on the `input` element. You       `writing-mode: bt-lr`             `writing-mode: bt-lr`   style on the `input` element. You       style on the `input` element. You       style on the `input` element. You       style on the `input` element. You                 style on the `input` element. You       style on the `input` element. You       style on the `input` element. You
                           shouldn\'t use this, since it\'s        style on the `input`              style on the `input`    shouldn\'t use this, since it\'s        shouldn\'t use this, since it\'s        shouldn\'t use this, since it\'s        shouldn\'t use this, since it\'s                  shouldn\'t use this, since it\'s        shouldn\'t use this, since it\'s        shouldn\'t use this, since it\'s
                           proprietary, unless you include         element.                          element.                proprietary, unless you include         proprietary, unless you include         proprietary, unless you include         proprietary, unless you include                   proprietary, unless you include         proprietary, unless you include         proprietary, unless you include
                           appropriate fallbacks for users of                                                                appropriate fallbacks for users of      appropriate fallbacks for users of      appropriate fallbacks for users of      appropriate fallbacks for users of                appropriate fallbacks for users of      appropriate fallbacks for users of      appropriate fallbacks for users of
                           other browsers.                                                                                   other browsers.                         other browsers.                         other browsers.                         other browsers.                                   other browsers.                         other browsers.                         other browsers.
  ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
:::

## See also {#see_also}

::: section-content
-   [HTML Forms](https://developer.mozilla.org/en-US/docs/Learn/Forms)
-   [`<input>`](../input) and the
    [`HTMLInputElement`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLInputElement)
    interface it\'s based upon
-   [`<input type="number">`](number)
-   [`validityState.rangeOverflow`](https://developer.mozilla.org/en-US/docs/Web/API/ValidityState/rangeOverflow)
    and
    [`validityState.rangeUnderflow`](https://developer.mozilla.org/en-US/docs/Web/API/ValidityState/rangeUnderflow)
-   [Controlling multiple parameters with
    ConstantSourceNode](https://developer.mozilla.org/en-US/docs/Web/API/Web_Audio_API/Controlling_multiple_parameters_with_ConstantSourceNode)
-   [Styling the range
    element](https://css-tricks.com/sliding-nightmare-understanding-range-input/){target="_blank"}
-   [Compatibility of CSS
    properties](https://developer.mozilla.org/en-US/docs/Learn/Forms/Property_compatibility_table_for_form_controls)
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/range](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/range){._attribution-link}
:::
