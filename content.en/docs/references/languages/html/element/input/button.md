

# \<input type=\"button\"\>



::: section-content
[`<input>`](../input) elements of type `button` are rendered as simple
push buttons, which can be programmed to control custom functionality
anywhere on a webpage as required when assigned an event handler
function (typically for the
[`click`](https://developer.mozilla.org/en-US/docs/Web/API/Element/click_event)
event).
:::

## Try it {#try_it}

::: section-content
::: iframe
::: {.output-header .border-rounded-top}
#### HTML Demo: \<input type=\"button\"\> {#html-demo-input-typebutton .output-heading}

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
    <input class="favorite styled" type="button" value="Add to favorites" />
:::
:::

::: {#css-panel .section .hidden tabindex="0" role="tabpanel" aria-labelledby="css" aria-hidden="true"}
::: {#css-editor}
    .styled {
      border: 0;
      line-height: 2.5;
      padding: 0 20px;
      font-size: 1rem;
      text-align: center;
      color: #fff;
      text-shadow: 1px 1px 1px #000;
      border-radius: 10px;
      background-color: rgba(220, 0, 0, 1);
      background-image: linear-gradient(
        to top left,
        rgba(0, 0, 0, 0.2),
        rgba(0, 0, 0, 0.2) 30%,
        rgba(0, 0, 0, 0)
      );
      box-shadow:
        inset 2px 2px 3px rgba(255, 255, 255, 0.6),
        inset -2px -2px 3px rgba(0, 0, 0, 0.6);
    }

    .styled:hover {
      background-color: rgba(255, 0, 0, 1);
    }

    .styled:active {
      box-shadow:
        inset -2px -2px 3px rgba(255, 255, 255, 0.6),
        inset 2px 2px 3px rgba(0, 0, 0, 0.6);
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

::: {#sect1 .notecard .note}
**Note:** While `<input>` elements of type `button` are still perfectly
valid HTML, the newer [`<button>`](../button) element is now the favored
way to create buttons. Given that a [`<button>`](../button)\'s label
text is inserted between the opening and closing tags, you can include
HTML in the label, even images.
:::
:::

## Value

### Button with a value {#button_with_a_value}

::: section-content
An `<input type="button">` elements\' [`value`](../input#value)
attribute contains a string that is used as the button\'s label.

::: code-example
[html]{.language-name}

``` {signature="JqVC4tPMlE5RotIvKU43OjyMFWO8EuqD99h7OrpW+Zw=" data-language="html"}
<input type="button" value="Click Me" />
```
:::

::: {#sect2 .code-example}
::: iframe
:::
:::
:::

### Button without a value {#button_without_a_value}

::: section-content
If you don\'t specify a `value`, you get an empty button:

::: code-example
[html]{.language-name}

``` {signature="mMdnhOsT5+XbTJb8nEC8Q3CWQ34A0vwjTvDpBOB+UaY=" data-language="html"}
<input type="button" />
```
:::

::: {#sect3 .code-example}
::: iframe
:::
:::
:::

## Using buttons {#using_buttons}

::: section-content
`<input type="button">` elements have no default behavior (their
cousins, `<input type="submit">` and [`<input type="reset">`](reset) are
used to submit and reset forms, respectively). To make buttons do
anything, you have to write JavaScript code to do the work.
:::

### A simple button {#a_simple_button}

::: section-content
We\'ll begin by creating a simple button with a
[`click`](https://developer.mozilla.org/en-US/docs/Web/API/Element/click_event)
event handler that starts our machine (well, it toggles the `value` of
the button and the text content of the following paragraph):

::: code-example
[html]{.language-name}

``` {signature="PLjFPG/OxR4+QwFk/mzvDznf06zy3luT81D7/VBDbY8=" data-language="html"}
<form>
  <input type="button" value="Start machine" />
</form>
<p>The machine is stopped.</p>
```
:::

::: code-example
[js]{.language-name}

``` {signature="f+xxWKdnLr42gCDMy8ZqE2Q8nRTzncoE7P05FUQHha4=" data-language="js"}
const button = document.querySelector("input");
const paragraph = document.querySelector("p");

button.addEventListener("click", updateButton);

function updateButton() {
  if (button.value === "Start machine") {
    button.value = "Stop machine";
    paragraph.textContent = "The machine has started!";
  } else {
    button.value = "Start machine";
    paragraph.textContent = "The machine is stopped.";
  }
}
```
:::

The script gets a reference to the
[`HTMLInputElement`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLInputElement)
object representing the `<input>` in the DOM, saving this reference in
the variable `button`.
[`addEventListener()`](https://developer.mozilla.org/en-US/docs/Web/API/EventTarget/addEventListener)
is then used to establish a function that will be run when
[`click`](https://developer.mozilla.org/en-US/docs/Web/API/Element/click_event)
events occur on the button.

::: {#sect4 .code-example}
::: iframe
:::
:::
:::

### Adding keyboard shortcuts to buttons {#adding_keyboard_shortcuts_to_buttons}

::: section-content
Keyboard shortcuts, also known as access keys and keyboard equivalents,
let the user trigger a button using a key or combination of keys on the
keyboard. To add a keyboard shortcut to a button --- just as you would
with any [`<input>`](../input) for which it makes sense --- you use the
[`accesskey`](../../global_attributes/accesskey) global attribute.

In this example, [s]{.kbd} is specified as the access key (you\'ll need
to press [s]{.kbd} plus the particular modifier keys for your browser/OS
combination; see [accesskey](../../global_attributes/accesskey) for a
useful list of those).

::: code-example
[html]{.language-name}

``` {signature="2NF/PTOO1F74Yq9VWxzWmZO3eTsPetLDrRYqKnfVJrc=" data-language="html"}
<form>
  <input type="button" value="Start machine" accesskey="s" />
</form>
<p>The machine is stopped.</p>
```
:::

::: {#sect5 .code-example}
::: iframe
:::
:::

::: {#sect6 .notecard .note}
**Note:** The problem with the above example of course is that the user
will not know what the access key is! In a real site, you\'d have to
provide this information in a way that doesn\'t interfere with the site
design (for example by providing an easily accessible link that points
to information on what the site accesskeys are).
:::
:::

### Disabling and enabling a button {#disabling_and_enabling_a_button}

::: section-content
To disable a button, specify the [`disabled`](../../attributes/disabled)
global attribute on it, like so:

::: code-example
[html]{.language-name}

``` {signature="rDS6mN6lj6mRA+fz2xx7Z1aPGKQtynRevZ9ne8lzyr4=" data-language="html"}
<input type="button" value="Disable me" disabled />
```
:::

#### Setting the disabled attribute {#setting_the_disabled_attribute}

You can enable and disable buttons at run time by setting `disabled` to
`true` or `false`. In this example our button starts off enabled, but if
you press it, it is disabled using `button.disabled = true`. A
[`setTimeout()`](https://developer.mozilla.org/en-US/docs/Web/API/setTimeout)
function is then used to reset the button back to its enabled state
after two seconds.

::: code-example
[html]{.language-name}

``` {signature="bryPS5bkVfBZClS3Lc+gFYRjDWAjxWu74gJwXtKZLMA=" data-language="html"}
<input type="button" value="Enabled" />
```
:::

::: code-example
[js]{.language-name}

``` {signature="B/vdg8GzQ9ZBMKZ+v9aUD+VUEkMuwWPr1T7sFMOtWsk=" data-language="js"}
const button = document.querySelector("input");

button.addEventListener("click", disableButton);

function disableButton() {
  button.disabled = true;
  button.value = "Disabled";
  setTimeout(() => {
    button.disabled = false;
    button.value = "Enabled";
  }, 2000);
}
```
:::

::: {#sect7 .code-example}
::: iframe
:::
:::

#### Inheriting the disabled state {#inheriting_the_disabled_state}

If the `disabled` attribute isn\'t specified, the button inherits its
`disabled` state from its parent element. This makes it possible to
enable and disable groups of elements all at once by enclosing them in a
container such as a [`<fieldset>`](../fieldset) element, and then
setting `disabled` on the container.

The example below shows this in action. This is very similar to the
previous example, except that the `disabled` attribute is set on the
`<fieldset>` when the first button is pressed --- this causes all three
buttons to be disabled until the two second timeout has passed.

::: code-example
[html]{.language-name}

``` {signature="JnkRu+XGwp9oqq8oaAbUhr598DUU2f2WnaPIWo3kXko=" data-language="html"}
<fieldset>
  <legend>Button group</legend>
  <input type="button" value="Button 1" />
  <input type="button" value="Button 2" />
  <input type="button" value="Button 3" />
</fieldset>
```
:::

::: code-example
[js]{.language-name}

``` {signature="P96vgeHqZ1re8w9f+UAlQY6q1jAtvrVX5rMWwhNyKL4=" data-language="js"}
const button = document.querySelector("input");
const fieldset = document.querySelector("fieldset");

button.addEventListener("click", disableButton);

function disableButton() {
  fieldset.disabled = true;
  setTimeout(() => {
    fieldset.disabled = false;
  }, 2000);
}
```
:::

::: {#sect8 .code-example}
::: iframe
:::
:::

::: {#sect9 .notecard .note}
**Note:** Firefox will, unlike other browsers, by default, [persist the
dynamic disabled
state](https://stackoverflow.com/questions/5985839/bug-with-firefox-disabled-attribute-of-input-not-resetting-when-refreshing){target="_blank"}
of a [`<button>`](../button) across page loads. Use the
[`autocomplete`](../button#autocomplete) attribute to control this
feature.
:::
:::

## Validation

::: section-content
Buttons don\'t participate in constraint validation; they have no real
value to be constrained.
:::

## Examples

::: section-content
The below example shows a very simple drawing app created using a
[`<canvas>`](../canvas) element and some simple CSS and JavaScript
(we\'ll hide the CSS for brevity). The top two controls allow you to
choose the color and size of the drawing pen. The button, when clicked,
invokes a function that clears the canvas.

::: code-example
[html]{.language-name}

``` {signature="GZUVlWpo/6YLdmNkqn42E5TfsF22ieGpf24HkIN26YY=" data-language="html"}
<div class="toolbar">
  <input type="color" aria-label="select pen color" />
  <input
    type="range"
    min="2"
    max="50"
    value="30"
    aria-label="select pen size" /><span class="output">30</span>
  <input type="button" value="Clear canvas" />


<canvas class="myCanvas">
  <p>Add suitable fallback here.</p>
</canvas>
```
:::

::: code-example
[js]{.language-name}

``` {signature="pl16qvUsaGbCDn3Syt8kp4auFvHU+9kpEPisWMjf3uQ=" data-language="js"}
const canvas = document.querySelector(".myCanvas");
const width = (canvas.width = window.innerWidth);
const height = (canvas.height = window.innerHeight - 85);
const ctx = canvas.getContext("2d");

ctx.fillStyle = "rgb(0,0,0)";
ctx.fillRect(0, 0, width, height);

const colorPicker = document.querySelector('input[type="color"]');
const sizePicker = document.querySelector('input[type="range"]');
const output = document.querySelector(".output");
const clearBtn = document.querySelector('input[type="button"]');

// covert degrees to radians
function degToRad(degrees) {
  return (degrees * Math.PI) / 180;
}

// update sizepicker output value

sizePicker.oninput = () => {
  output.textContent = sizePicker.value;
};

// store mouse pointer coordinates, and whether the button is pressed
let curX;
let curY;
let pressed = false;

// update mouse pointer coordinates
document.onmousemove = (e) => {
  curX = e.pageX;
  curY = e.pageY;
};

canvas.onmousedown = () => {
  pressed = true;
};

canvas.onmouseup = () => {
  pressed = false;
};

clearBtn.onclick = () => {
  ctx.fillStyle = "rgb(0,0,0)";
  ctx.fillRect(0, 0, width, height);
};

function draw() {
  if (pressed) {
    ctx.fillStyle = colorPicker.value;
    ctx.beginPath();
    ctx.arc(
      curX,
      curY - 85,
      sizePicker.value,
      degToRad(0),
      degToRad(360),
      false,
    );
    ctx.fill();
  }

  requestAnimationFrame(draw);
}

draw();
```
:::

::: {#sect10 .code-example}
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
  --------------------------------------------------------------------------------------------------------------------
  Specification
  --------------------------------------------------------------------------------------------------------------------
  [HTML Standard\
  [\#
  button-state-(type=button)]{.small}](https://html.spec.whatwg.org/multipage/input.html#button-state-(type=button))

  --------------------------------------------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
             Desktop                                                         Mobile                                                                                   
  ---------- --------- ------ --------- ------------------- ------- -------- ----------------- ---------------- --------------------- --------------- --------------- ------------------
             Chrome    Edge   Firefox   Internet Explorer   Opera   Safari   WebView Android   Chrome Android   Firefox for Android   Opera Android   Safari on IOS   Samsung Internet
  `button`   1         12     1         Yes                 15      1        4.4               18               4                     14              1               1.0
:::

## See also {#see_also}

::: section-content
-   [`<input>`](../input) and the
    [`HTMLInputElement`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLInputElement)
    interface which implements it.
-   The more modern [`<button>`](../button) element.
-   [Compatibility of CSS
    properties](https://developer.mozilla.org/en-US/docs/Learn/Forms/Property_compatibility_table_for_form_controls)
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/button](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/button){._attribution-link}
:::
