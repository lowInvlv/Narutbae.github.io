

# \<datalist\>: The HTML Data List element



::: section-content
The `<datalist>` [HTML](../index) element contains a set of
[`<option>`](option) elements that represent the permissible or
recommended options available to choose from within other controls.
:::

## Try it {#try_it}

::: section-content
::: iframe
::: {.output-header .border-rounded-top}
#### HTML Demo: \<datalist\> {#html-demo-datalist .output-heading}

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
    <label for="ice-cream-choice">Choose a flavor:</label>
    <input list="ice-cream-flavors" id="ice-cream-choice" name="ice-cream-choice" />

    <datalist id="ice-cream-flavors">
      <option value="Chocolate"></option>
      <option value="Coconut"></option>
      <option value="Mint"></option>
      <option value="Strawberry"></option>
      <option value="Vanilla"></option>
    </datalist>
:::
:::

::: {#css-panel .section .hidden tabindex="0" role="tabpanel" aria-labelledby="css" aria-hidden="true"}
::: {#css-editor}
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

To bind the `<datalist>` element to the control, we give it a unique
identifier in the [`id`](../global_attributes/id) attribute, and then
add the [`list`](input#list) attribute to the [`<input>`](input) element
with the same identifier as value. Only certain types of
[`<input>`](input) support this behavior, and it can also vary from
browser to browser.

::: {#sect1 .notecard .note}
**Note:** The `<option>` element can store a value as internal content
and in the `value` and `label` attributes. Which one will be visible in
the drop-down menu depends on the browser, but when clicked, content
entered into control field will always come from the `value` attribute.
:::
:::

## Attributes

::: section-content
This element has no other attributes than the [global
attributes](../global_attributes), common to all elements.
:::

## Examples

### Textual types {#textual_types}

::: section-content
Recommended values in types [text](input/text), [search](input/search),
[url](input/url), [tel](input/tel), [email](input/email) and
[number](input/number), are displayed in a drop-down menu when user
clicks or double-clicks on the control. Typically the right side of a
control will also have an arrow pointing to the presence of predefined
values.

::: code-example
[html]{.language-name}

``` {signature="Um7cQkHew3nfb4QcMVeNTewQjzzAl7/c2ZVqRKzCsQU=" data-language="html"}
<label for="myBrowser">Choose a browser from this list:</label>
<input list="browsers" id="myBrowser" name="myBrowser" />
<datalist id="browsers">
  <option value="Chrome"></option>
  <option value="Firefox"></option>
  <option value="Opera"></option>
  <option value="Safari"></option>
  <option value="Microsoft Edge"></option>
</datalist>
```
:::

::: {#sect2 .code-example}
::: iframe
:::
:::
:::

### Date and Time types {#date_and_time_types}

::: section-content
The types [month](input/month), [week](input/week), [date](input/date),
[time](input/time) and [datetime-local](input/datetime-local) can show
an interface that allows a convenient selection of a date and time.
Predefined values can be shown there, allowing the user to quickly fill
the control value.

::: {#sect3 .notecard .note}
**Note:** When type is not supported, `text` type creating simple text
field will be used instead. That field will correctly recognize
recommended values and display them to the user in a drop-down menu.
:::

::: code-example
[html]{.language-name}

``` {signature="Knuamdj8Bh+rScCHR5E47vauZEzYq+EDwdf+jmpNgHI=" data-language="html"}
<input type="time" list="popularHours" />
<datalist id="popularHours">
  <option value="12:00"></option>
  <option value="13:00"></option>
  <option value="14:00"></option>
</datalist>
```
:::

::: {#sect4 .code-example}
::: iframe
:::
:::
:::

### Range type {#range_type}

::: section-content
The recommended values in the [range](input/range) type will be shown as
series of hash marks that the user can easily select.

::: code-example
[html]{.language-name}

``` {signature="gjtgUcd4bhIjFbgTSgx6WBLsluwSy9aeP2u3LCmzCf8=" data-language="html"}
<label for="tick">Tip amount:</label>
<input type="range" list="tickmarks" min="0" max="100" id="tick" name="tick" />
<datalist id="tickmarks">
  <option value="0"></option>
  <option value="10"></option>
  <option value="20"></option>
  <option value="30"></option>
</datalist>
```
:::

::: {#sect5 .code-example}
::: iframe
:::
:::
:::

### Color type {#color_type}

::: section-content
The [color](input/color) type can show predefined colors in a
browser-provided interface.

::: code-example
[html]{.language-name}

``` {signature="zdB26FW60YEWknF+uFTufMIXImuYL/NmBGuDTDxOEQs=" data-language="html"}
<label for="colors">Pick a color (preferably a red tone):</label>
<input type="color" list="redColors" id="colors" />
<datalist id="redColors">
  <option value="#800000"></option>
  <option value="#8B0000"></option>
  <option value="#A52A2A"></option>
  <option value="#DC143C"></option>
</datalist>
```
:::

::: {#sect6 .code-example}
::: iframe
:::
:::
:::

### Password type {#password_type}

::: section-content
The specification allows linking `<datalist>` with a
[password](input/password) type, but no browser supports it for security
reasons.

::: code-example
[html]{.language-name}

``` {signature="eQQp3Lhw8pewE48TwwaY7cb3MGh5P/co24rJxtlvnPo=" data-language="html"}
<label for="pwd">Enter a password:</label>
<input type="password" list="randomPassword" id="pwd" />
<datalist id="randomPassword">
  <option value="5Mg[_3DnkgSu@!q#"></option>
</datalist>
```
:::

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
href="../content_categories#phrasing_content">phrasing content</a>.</td>
</tr>
<tr class="even">
<th scope="row">Permitted content</th>
<td>Either <a href="../content_categories#phrasing_content">phrasing
content</a> or zero or more <a
href="option"><code>&lt;option&gt;</code></a> elements.</td>
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
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/listbox_role">listbox</a></td>
</tr>
<tr class="even">
<th scope="row">Permitted ARIA roles</th>
<td>No <code>role</code> permitted</td>
</tr>
<tr class="odd">
<th scope="row">DOM interface</th>
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLDataListElement"><code>HTMLDataListElement</code></a></td>
</tr>
</tbody>
</table>

</figure>
:::

## Accessibility concerns {#accessibility_concerns}

::: section-content
When deciding to use the `<datalist>` element, here are some
accessibility issues to be mindful of:

-   The font size of the data list\'s options does not zoom, always
    remaining the same size. The contents of the autosuggest do not grow
    or shrink when the rest of the contents are zoomed in or out.
-   As targeting the list of options with CSS is very limited to
    non-existent, rendering can not be styled for high-contrast mode.
-   Some screen reader/browser combinations, including NVDA and Firefox,
    do not announce the contents of the autosuggest popup.
:::

## Specifications

::: _table
  ----------------------------------------------------------------------------------------------------------------
  Specification
  ----------------------------------------------------------------------------------------------------------------
  [HTML Standard\
  [\#
  the-datalist-element]{.small}](https://html.spec.whatwg.org/multipage/form-elements.html#the-datalist-element)

  ----------------------------------------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
  -----------------------------------------------------------------------------------------------------------------------------------------------------------------
               Desktop                                                     Mobile                                                                        
  ------------ --------- ------ -------------- ---------- ------- -------- --------- --------- -------------------------------------- --------- -------- ----------
               Chrome    Edge   Firefox        Internet   Opera   Safari   WebView   Chrome    Firefox for Android                    Opera     Safari   Samsung
                                               Explorer                    Android   Android                                          Android   on IOS   Internet

  `datalist`   20        12     4              10         9.5     12.1     4.4.3     33        79                                     20        12.2     2.0
                                                                                                                                                         
                                The                                                            The dropdown menu containing available                    
                                `<datalist>`                                                   options does not appear. See [bug                         
                                element will                                                   1535985](https://bugzil.la/1535985).                      
                                only create a                                                                                                            
                                dropdown for                                                   4--79                                                     
                                textual types,                                                                                                           
                                such as                                                                                                                  
                                `text`,                                                                                                                  
                                `search`,                                                                                                                
                                `url`, `tel`,                                                                                                            
                                `email` and                                                                                                              
                                `number`. The                                                                                                            
                                `date`,                                                                                                                  
                                `time`,                                                                                                                  
                                `range` and                                                                                                              
                                `color` types                                                                                                            
                                are not                                                                                                                  
                                supported.                                                                                                               
  -----------------------------------------------------------------------------------------------------------------------------------------------------------------
:::

## See also {#see_also}

::: section-content
-   The [`<input>`](input) element, and more specifically its
    [`list`](input#list) attribute;
-   The [`<option>`](option) element.
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Element/datalist](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/datalist){._attribution-link}
:::
