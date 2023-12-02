

# \<select\>: The HTML Select element



::: section-content
The `<select>` [HTML](../index) element represents a control that
provides a menu of options.
:::

## Try it {#try_it}

::: section-content
::: iframe
::: {.output-header .border-rounded-top}
#### HTML Demo: \<select\> {#html-demo-select .output-heading}

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
    <label for="pet-select">Choose a pet:</label>

    <select name="pets" id="pet-select">
      <option value="">--Please choose an option--</option>
      <option value="dog">Dog</option>
      <option value="cat">Cat</option>
      <option value="hamster">Hamster</option>
      <option value="parrot">Parrot</option>
      <option value="spider">Spider</option>
      <option value="goldfish">Goldfish</option>
    </select>
:::
:::

::: {#css-panel .section .hidden tabindex="0" role="tabpanel" aria-labelledby="css" aria-hidden="true"}
::: {#css-editor}
    label {
      font-family: sans-serif;
      font-size: 1rem;
      padding-right: 10px;
    }

    select {
      font-size: 0.9rem;
      padding: 2px 5px;
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

The above example shows typical `<select>` usage. It is given an `id`
attribute to enable it to be associated with a [`<label>`](label) for
accessibility purposes, as well as a `name` attribute to represent the
name of the associated data point submitted to the server. Each menu
option is defined by an [`<option>`](option) element nested inside the
`<select>`.

Each `<option>` element should have a [`value`](option#value) attribute
containing the data value to submit to the server when that option is
selected. If no `value` attribute is included, the value defaults to the
text contained inside the element. You can include a
[`selected`](option#selected) attribute on an `<option>` element to make
it selected by default when the page first loads.

The `<select>` element has some unique attributes you can use to control
it, such as `multiple` to specify whether multiple options can be
selected, and `size` to specify how many options should be shown at
once. It also accepts most of the general form input attributes such as
`required`, `disabled`, `autofocus`, etc.

You can further nest `<option>` elements inside [`<optgroup>`](optgroup)
elements to create separate groups of options inside the dropdown.

For further examples, see [The native form widgets: Drop-down
content](https://developer.mozilla.org/en-US/docs/Learn/Forms/Other_form_controls#drop-down_controls).
:::

## Attributes

::: section-content
This element includes the [global attributes](../global_attributes).

[`autocomplete`](#autocomplete)

:   A string providing a hint for a [user
    agent\'s](https://developer.mozilla.org/en-US/docs/Glossary/User_agent)
    autocomplete feature. See [The HTML autocomplete
    attribute](../attributes/autocomplete) for a complete list of values
    and details on how to use autocomplete.

[`autofocus`](#autofocus)

:   This Boolean attribute lets you specify that a form control should
    have input focus when the page loads. Only one form element in a
    document can have the `autofocus` attribute.

[`disabled`](#disabled)

:   This Boolean attribute indicates that the user cannot interact with
    the control. If this attribute is not specified, the control
    inherits its setting from the containing element, for example
    [`<fieldset>`](fieldset); if there is no containing element with the
    `disabled` attribute set, then the control is enabled.

[`form`](#form)

:   The [`<form>`](form) element to associate the `<select>` with (its
    *form owner*). The value of this attribute must be the
    [`id`](../global_attributes#id) of a `<form>` in the same document.
    (If this attribute is not set, the `<select>` is associated with its
    ancestor `<form>` element, if any.)

    This attribute lets you associate `<select>` elements to `<form>`s
    anywhere in the document, not just inside a `<form>`. It can also
    override an ancestor `<form>` element.

[`multiple`](#multiple)

:   This Boolean attribute indicates that multiple options can be
    selected in the list. If it is not specified, then only one option
    can be selected at a time. When `multiple` is specified, most
    browsers will show a scrolling list box instead of a single line
    dropdown.

[`name`](#name)

:   This attribute is used to specify the name of the control.

[`required`](#required)

:   A Boolean attribute indicating that an option with a non-empty
    string value must be selected.

[`size`](#size)

:   If the control is presented as a scrolling list box (e.g. when
    `multiple` is specified), this attribute represents the number of
    rows in the list that should be visible at one time. Browsers are
    not required to present a select element as a scrolled list box. The
    default value is `0`.

    ::: {#sect1 .notecard .note}
    **Note:** According to the HTML specification, the default value for
    size should be `1`; however, in practice, this has been found to
    break some websites, and no other browser currently does that, so
    Mozilla has opted to continue to return `0` for the time being with
    Firefox.
    :::
:::

## Usage notes {#usage_notes}

### Selecting multiple options {#selecting_multiple_options}

::: section-content
On a desktop computer, there are a number of ways to select multiple
options in a `<select>` element with a `multiple` attribute:

Mouse users can hold the [Ctrl]{.kbd}, [Command]{.kbd}, or [Shift]{.kbd}
keys (depending on what makes sense for your operating system) and then
click multiple options to select/deselect them.

::: {#sect2 .notecard .warning}
**Warning:** The mechanism for selecting multiple non-contiguous items
via the keyboard described below currently only seems to work in
Firefox.

On macOS, the [Ctrl]{.kbd} + [Up]{.kbd} and [Ctrl]{.kbd} + [Down]{.kbd}
shortcuts conflict with the OS default shortcuts for *Mission Control*
and *Application windows*, so you\'ll have to turn these off before it
will work.
:::

Keyboard users can select multiple contiguous items by:

-   Focusing on the `<select>` element (e.g. using [Tab]{.kbd} ).
-   Selecting an item at the top or bottom of the range they want to
    select using the [Up]{.kbd} and [Down]{.kbd} cursor keys to go up
    and down the options.
-   Holding down the [Shift]{.kbd} key and then using the [Up]{.kbd} and
    [Down]{.kbd} cursor keys to increase or decrease the range of items
    selected.

Keyboard users can select multiple non-contiguous items by:

-   Focusing on the `<select>` element (e.g. using [Tab]{.kbd} ).
-   Holding down the [Ctrl]{.kbd} key then using the [Up]{.kbd} and
    [Down]{.kbd} cursor keys to change the \"focused\" select option,
    i.e. the one that will be selected if you choose to do so. The
    \"focused\" select option is highlighted with a dotted outline, in
    the same way as a keyboard-focused link.
-   Pressing [Space]{.kbd} to select/deselect \"focused\" select
    options.
:::

## Styling with CSS {#styling_with_css}

::: section-content
The `<select>` element is notoriously difficult to style productively
with CSS. You can affect certain aspects like any element --- for
example, manipulating the [box
model](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/The_box_model),
the [displayed
font](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_fonts), etc.,
and you can use the
[`appearance`](https://developer.mozilla.org/en-US/docs/Web/CSS/appearance)
property to remove the default system `appearance`.

However, these properties don\'t produce a consistent result across
browsers, and it is hard to do things like line different types of form
element up with one another in a column. The `<select>` element\'s
internal structure is complex, and hard to control. If you want to get
full control, you should consider using a library with good facilities
for styling form widgets, or try rolling your own dropdown menu using
non-semantic elements, JavaScript, and
[WAI-ARIA](https://developer.mozilla.org/en-US/docs/Learn/Accessibility/WAI-ARIA_basics)
to provide semantics.

For more useful information on styling `<select>`, see:

-   [Styling HTML
    forms](https://developer.mozilla.org/en-US/docs/Learn/Forms/Styling_web_forms)
-   [Advanced styling for HTML
    forms](https://developer.mozilla.org/en-US/docs/Learn/Forms/Advanced_form_styling)

Also see the \"Customizing select styles\" example below for an example
of you could attempt a simple `<select>` styling.
:::

## Examples

### Basic select {#basic_select}

::: section-content
The following example creates a very simple dropdown menu, the second
option of which is selected by default.

::: code-example
[html]{.language-name}

``` {signature="TPyBcla2JefLSgyZXj+GYW50vdXGUi9mYWW55AyUHIE=" data-language="html"}
<!-- The second value will be selected initially -->
<select name="choice">
  <option value="first">First Value</option>
  <option value="second" selected>Second Value</option>
  <option value="third">Third Value</option>
</select>
```
:::

#### Result

::: {#sect3 .code-example}
::: iframe
:::
:::
:::

### Advanced select with multiple features {#advanced_select_with_multiple_features}

::: section-content
The follow example is more complex, showing off more features you can
use on a `<select>` element:

::: code-example
[html]{.language-name}

``` {signature="gS9YJxhQ7MKmQIRBzQ0n705Ob6tGLmMv+QMElR/iMQw=" data-language="html"}
<label>
  Please choose one or more pets:
  <select name="pets" multiple size="4">
    <optgroup label="4-legged pets">
      <option value="dog">Dog</option>
      <option value="cat">Cat</option>
      <option value="hamster" disabled>Hamster</option>
    </optgroup>
    <optgroup label="Flying pets">
      <option value="parrot">Parrot</option>
      <option value="macaw">Macaw</option>
      <option value="albatross">Albatross</option>
    </optgroup>
  </select>
</label>
```
:::

#### Result {#result_2}

::: {#sect4 .code-example}
::: iframe
:::
:::

You\'ll see that:

-   Multiple options are selectable because we\'ve included the
    `multiple` attribute.
-   The `size` attribute causes only 4 lines to display at a time; you
    can scroll to view all the options.
-   We\'ve included [`<optgroup>`](optgroup) elements to divide the
    options up into different groups. This is a purely visual grouping,
    its visualization generally consists of the group name being bolded,
    and the options being indented.
-   The \"Hamster\" option includes a `disabled` attribute and therefore
    can\'t be selected at all.
:::

### Customizing select styles {#customizing_select_styles}

::: section-content
This example shows how you could use some CSS and JavaScript to provide
extensive custom styling for a `<select>` box.

This example basically:

-   Clones the `<select>`\'s context (the [`<option>`](option) elements)
    in a parent wrapper and reimplements the standard expected behavior
    using additional HTML elements and JavaScript. This includes basic
    tab behavior to provide keyboard accessibility.
-   Maps some standards native `attributes` to `data-attributes` of the
    new elements in order to manage state and CSS.

::: {#sect5 .notecard .note}
**Note:** Not all native features are supported, it\'s a Proof of
Concept. IT starts from standard HTML but the same results can be
achieved starting from JSON data, custom HTML, or other solutions.
:::

#### HTML

::: code-example
[html]{.language-name}

``` {signature="5jQB5n72rOLcUOQfu26qdO6uKEbpK6VIgeR8yH1lLh0=" data-language="html"}
<form>
  <fieldset>
    <legend>Standard controls</legend>
    <select name="1A" id="select" autocomplete="off" required>
      <option>Carrots</option>
      <option>Peas</option>
      <option>Beans</option>
      <option>Pneumonoultramicroscopicsilicovolcanoconiosis</option>
    </select>
  </fieldset>
  <fieldset id="custom">
    <legend>Custom controls</legend>
    <select name="2A" id="select" autocomplete="off" required>
      <option>Carrots</option>
      <option>Peas</option>
      <option>Beans</option>
      <option>Pneumonoultramicroscopicsilicovolcanoconiosis</option>
    </select>
  </fieldset>
</form>
```
:::

#### CSS

::: code-example
[css]{.language-name}

``` {signature="hoa421zURWd/2yz5HGpqM2f+AG0g74k/IX/8x8UFo/c=" data-language="css"}
body {
  font-family: Cambria, Cochin, Georgia, Times, "Times New Roman", serif;
}

.select:focus {
  border-color: blue;
}

html body form fieldset#custom div.select[data-multiple] div.header {
  display: none;
}

html body form fieldset#custom div.select div.header {
  content: "↓";
  display: flex;
  flex: 1;
  align-items: center;
  padding: 0;
  position: relative;
  width: auto;
  box-sizing: border-box;
  border-width: 1px;
  border-style: inherit;
  border-color: inherit;
  border-radius: inherit;
}

html body form fieldset#custom div.select div.header::after {
  content: "↓";
  align-self: stretch;
  display: flex;
  align-content: center;
  justify-content: center;
  justify-items: center;
  align-items: center;
  padding: 0.5em;
}

html body form fieldset#custom div.select div.header:hover::after {
  background-color: blue;
}

.select .header select {
  appearance: none;
  font-family: inherit;
  font-size: inherit;
  padding: 0;
  border-width: 0;
  width: 100%;
  flex: 1;
  display: none;
}

.select .header select optgroup {
  display: none;
}

.select select div.option {
  display: none;
}

html body form fieldset#custom div.select {
  user-select: none;
  box-sizing: border-box;
  position: relative;
  border-radius: 4px;
  border-style: solid;
  border-width: 0;
  border-color: gray;
  width: auto;
  display: inline-block;
}

html body form fieldset#custom div.select:focus,
html body form fieldset#custom div.select:hover {
  border-color: blue;
}

html body form fieldset#custom div.select[data-open] {
  border-bottom-left-radius: 0;
  border-bottom-right-radius: 0;
}

html body form fieldset#custom div.select[data-open] datalist {
  display: initial;
}

html body form fieldset#custom div.select datalist {
  appearance: none;
  position: absolute;
  border-style: solid;
  border-width: 1px;
  border-color: gray;
  left: 0;
  display: none;
  width: 100%;
  box-sizing: border-box;
  z-index: 2;
  border-bottom-left-radius: 4px;
  border-bottom-right-radius: 4px;
}

html body form fieldset#custom div.select datalist div.option {
  background-color: white;
  margin-bottom: 1px;
  cursor: pointer;
  padding: 0.5em;
  border-width: 0;
}

html body form fieldset#custom div.select datalist div.option:hover,
html body form fieldset#custom div.select datalist div.option:focus,
html body form fieldset#custom div.select datalist div.option:checked {
  background-color: blue;
  color: white;
}

html
  body
  form
  fieldset#custom
  div.select
  div.optgroup
  div.option[data-disabled] {
  color: gray;
}

html
  body
  form
  fieldset#custom
  div.select
  div.optgroup
  div.option[data-checked] {
  background-color: blue;
  color: white;
}

html body form fieldset#custom div.select div.optgroup div.label {
  font-weight: bold;
}

html body form fieldset#custom div.select div.optgroup div.option div.label {
  font-weight: normal;
  padding: 0.25em;
}

html body form fieldset#custom div.select div.header span {
  flex: 1;
  padding: 0.5em;
}
```
:::

#### JavaScript

::: code-example
[js]{.language-name}

``` {signature="VBcwxA5gHMPSr1t4RJ64AxBBQlFeMAOWQ+bTmQDiEZM=" data-language="js"}
const selects = custom.querySelectorAll("select");
for (const select of selects) {
  const div = document.createElement("div");
  const header = document.createElement("div");
  const datalist = document.createElement("datalist");
  const optgroups = select.querySelectorAll("optgroup");
  const span = document.createElement("span");
  const options = select.options;
  const parent = select.parentElement;
  const multiple = select.hasAttribute("multiple");
  function onclick(e) {
    const disabled = this.hasAttribute("data-disabled");
    select.value = this.dataset.value;
    span.innerText = this.dataset.label;
    if (disabled) return;
    if (multiple) {
      if (e.shiftKey) {
        const checked = this.hasAttribute("data-checked");
        if (checked) {
          this.removeAttribute("data-checked");
        } else {
          this.setAttribute("data-checked", "");
        }
      } else {
        const options = div.querySelectorAll(".option");
        for (let i = 0; i < options.length; i++) {
          const option = options[i];
          option.removeAttribute("data-checked");
        }
        this.setAttribute("data-checked", "");
      }
    }
  }

  function onkeyup(e) {
    e.preventDefault();
    e.stopPropagation();
    if (e.keyCode === 13) {
      this.click();
    }
  }

  div.classList.add("select");
  header.classList.add("header");
  div.tabIndex = 1;
  select.tabIndex = -1;
  span.innerText = select.label;
  header.appendChild(span);

  for (const attribute of select.attributes) {
    div.dataset[attribute.name] = attribute.value;
  }
  for (let i = 0; i < options.length; i++) {
    const option = document.createElement("div");
    const label = document.createElement("div");
    const o = options[i];
    for (const attribute of o.attributes) {
      option.dataset[attribute.name] = attribute.value;
    }
    option.classList.add("option");
    label.classList.add("label");
    label.innerText = o.label;
    option.dataset.value = o.value;
    option.dataset.label = o.label;
    option.onclick = onclick;
    option.onkeyup = onkeyup;
    option.tabIndex = i + 1;
    option.appendChild(label);
    datalist.appendChild(option);
  }
  div.appendChild(header);
  for (const o of optgroups) {
    const optgroup = document.createElement("div");
    const label = document.createElement("div");
    const options = o.querySelectorAll("option");

    Object.assign(optgroup, o);
    optgroup.classList.add("optgroup");
    label.classList.add("label");
    label.innerText = o.label;
    optgroup.appendChild(label);
    div.appendChild(optgroup);
    for (const o of options) {
      const option = document.createElement("div");
      const label = document.createElement("div");

      for (const attribute of o.attributes) {
        option.dataset[attribute.name] = attribute.value;
      }
      option.classList.add("option");
      label.classList.add("label");
      label.innerText = o.label;
      option.tabIndex = i + 1;
      option.dataset.value = o.value;
      option.dataset.label = o.label;
      option.onclick = onclick;
      option.onkeyup = onkeyup;
      option.tabIndex = i + 1;
      option.appendChild(label);
      optgroup.appendChild(option);
    }
  }

  div.onclick = (e) => {
    e.preventDefault();
  };

  parent.insertBefore(div, select);
  header.appendChild(select);
  div.appendChild(datalist);
  datalist.style.top = `${header.offsetTop + header.offsetHeight}px`;

  div.onclick = (e) => {
    if (!multiple) {
      const open = div.hasAttribute("data-open");
      e.stopPropagation();
      if (open) {
        div.removeAttribute("data-open");
      } else {
        div.setAttribute("data-open", "");
      }
    }
  };

  div.onkeyup = (event) => {
    event.preventDefault();
    if (event.keyCode === 13) {
      div.click();
    }
  };

  document.addEventListener("click", (e) => {
    if (div.hasAttribute("data-open")) {
      div.removeAttribute("data-open");
    }
  });

  const width = Math.max(
    ...Array.from(options).map((e) => {
      span.innerText = e.label;
      return div.offsetWidth;
    }),
  );

  console.log(width);
  div.style.width = `${width}px`;
}
document.forms[0].onsubmit = (e) => {
  const data = new FormData(this);
  e.preventDefault();
  submit.innerText = JSON.stringify([...data.entries()]);
};
```
:::

#### Result {#result_3}

::: iframe
Standard controls Carrots Peas Beans
Pneumonoultramicroscopicsilicovolcanoconiosis

Custom controls Carrots Peas Beans
Pneumonoultramicroscopicsilicovolcanoconiosis
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
href="../content_categories#interactive_content">interactive
content</a>, <a href="../content_categories#form_listed">listed</a>, <a
href="../content_categories#form_labelable">labelable</a>, <a
href="../content_categories#form_resettable">resettable</a>, and <a
href="../content_categories#form_submittable">submittable</a> <a
href="../content_categories#form-associated_">form-associated</a>
element</td>
</tr>
<tr class="even">
<th scope="row">Permitted content</th>
<td>Zero or more <a href="option"><code>&lt;option&gt;</code></a> or <a
href="optgroup"><code>&lt;optgroup&gt;</code></a> elements.</td>
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
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/combobox_role"><code>combobox</code></a>
with <strong>no</strong> <code>multiple</code> attribute and
<strong>no</strong> <code>size</code> attribute greater than 1,
otherwise <a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/listbox_role"><code>listbox</code></a></td>
</tr>
<tr class="even">
<th scope="row">Permitted ARIA roles</th>
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/menu_role"><code>menu</code></a>
with <strong>no</strong> <code>multiple</code> attribute and
<strong>no</strong> <code>size</code> attribute greater than 1,
otherwise no <code>role</code> permitted</td>
</tr>
<tr class="odd">
<th scope="row">DOM interface</th>
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLSelectElement"><code>HTMLSelectElement</code></a></td>
</tr>
</tbody>
</table>

</figure>
:::

## Specifications

::: _table
  ------------------------------------------------------------------------------------------------------------
  Specification
  ------------------------------------------------------------------------------------------------------------
  [HTML Standard\
  [\#
  the-select-element]{.small}](https://html.spec.whatwg.org/multipage/form-elements.html#the-select-element)

  ------------------------------------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
  ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
               Desktop                                                                                                       Mobile                                                                                                     
  ------------ ---------------------- ------ ------------------------------------- ---------- ------- ---------------------- ---------------------- ---------------------- --------------------------- --------- ---------------------- ----------------------
               Chrome                 Edge   Firefox                               Internet   Opera   Safari                 WebView Android        Chrome Android         Firefox for Android         Opera     Safari on IOS          Samsung Internet
                                                                                   Explorer                                                                                                            Android                          

  `select`     1                      12     1                                     Yes        2       1                      ≤37                    18                     4                           10.1      1                      1.0
                                                                                                                                                                                                                                        
               `border-radius` on            Historically, Firefox has allowed                        `border-radius` on     \[\"In the Browser app `border-radius` on     Firefox for Android, by               `border-radius` on     `border-radius` on
               `<select>` elements is        keyboard and mouse events to bubble                      `<select>` elements is for Android 4.1 (and   `<select>` elements is default, sets a                       `<select>` elements is `<select>` elements is
               ignored unless                up from the `<option>` element to the                    ignored unless         possibly later         ignored unless         `background-image` gradient           ignored unless         ignored unless
               `-webkit-appearance`          parent `<select>` element, although                      `-webkit-appearance`   versions), there is a  `-webkit-appearance`   on all `<select multiple>`            `-webkit-appearance`   `-webkit-appearance`
               is overridden to an           this behavior is inconsistent across                     is overridden to an    bug where the menu     is overridden to an    elements. This can be                 is overridden to an    is overridden to an
               appropriate value.            many browsers. For better Web                            appropriate value.     indicator triangle on  appropriate value.     disabled using                        appropriate value.     appropriate value.
                                             compatibility (and for technical                                                the side of a                                 `background-image: none`.                                    
                                             reasons), when Firefox is in                                                    `<select>` will not be                                                                                     
                                             multi-process mode the `<select>`                                               displayed if a                                                                                             
                                             element is displayed as a drop-down                                             `background`,                                                                                              
                                             list. The behavior is unchanged if                                              `border`, or                                                                                               
                                             the `<select>` is presented inline                                              `border-radius` style                                                                                      
                                             and it has either the multiple                                                  is applied to the                                                                                          
                                             attribute defined or a size attribute                                           `<select>`.\",                                                                                             
                                             set to more than 1. Rather than                                                 \"`border-radius` on                                                                                       
                                             watching `<option>` elements for                                                `<select>` elements is                                                                                     
                                             events, you should watch for change                                             ignored unless                                                                                             
                                             events on `<select>`. See [bug                                                  `-webkit-appearance`                                                                                       
                                             1090602](https://bugzil.la/1090602)                                             is overridden to an                                                                                        
                                             for details.                                                                    appropriate value.\"\]                                                                                     

  `disabled`   1                      12     1                                     Yes        15      3                      4.4                    18                     4                           14        2                      1.0

  `form`       1                      12     1                                     Yes        15      3                      4.4                    18                     4                           14        2                      1.0

  `multiple`   1                      12     1                                     Yes        15      3                      4.4                    18                     4                           14        2                      1.0

  `name`       1                      12     1                                     Yes        15      3                      4.4                    18                     4                           14        2                      1.0

  `required`   10                     12     4                                     10         15      5.1                    4.4                    18                     4                           14        5                      1.0

  `size`       1                      12     1                                     Yes        15      3                      4.4                    18                     4                           14        2                      1.0
  ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
:::

## See also {#see_also}

::: section-content
-   Events fired by `<select>`:
    [`change`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/change_event),
    [`input`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/input_event)
-   The [`<option>`](option) element
-   The [`<optgroup>`](optgroup) element
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Element/select](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/select){._attribution-link}
:::
