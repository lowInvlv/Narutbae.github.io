

# \<input type=\"reset\"\>



::: section-content
[`<input>`](../input) elements of type `reset` are rendered as buttons,
with a default
[`click`](https://developer.mozilla.org/en-US/docs/Web/API/Element/click_event)
event handler that resets all inputs in the form to their initial
values.
:::

## Try it {#try_it}

::: section-content
::: iframe
::: {.output-header .border-rounded-top}
#### HTML Demo: \<input type=\"reset\"\> {#html-demo-input-typereset .output-heading}

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
    <form>
      <div class="controls">
        <label for="id">User ID:</label>
        <input type="text" id="id" name="id" />

        <input type="reset" value="Reset" />
        <input type="submit" value="Submit" />
      
    </form>
:::
:::

::: {#css-panel .section .hidden tabindex="0" role="tabpanel" aria-labelledby="css" aria-hidden="true"}
::: {#css-editor}
    .controls {
      padding-top: 1rem;
      display: grid;
      grid-template-rows: repeat(3, 1fr);
      grid-template-columns: 1fr 2fr;
      gap: 0.7rem;
    }

    label {
      font-size: 0.8rem;
      justify-self: end;
    }

    input[type='reset'],
    input[type='submit'] {
      width: 5rem;
      justify-self: end;
    }

    input[type='reset'] {
      grid-column: 2;
      grid-row: 2;
    }

    input[type='submit'] {
      grid-column: 2;
      grid-row: 3;
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
**Note:** You should usually avoid including reset buttons in your
forms. They\'re rarely useful, and are instead more likely to frustrate
users who click them by mistake (often while trying to click the [submit
button](submit)).
:::
:::

## Value

::: section-content
An `<input type="reset">` element\'s [`value`](../input#value) attribute
contains a string that is used as the button\'s label. Buttons such as
`reset` don\'t have a value otherwise.
:::

### Setting the value attribute {#setting_the_value_attribute}

::: section-content
::: code-example
[html]{.language-name}

``` {signature="y9upZyhUmZowaLPfEkynRvZ+cdp9NYVaRlmHmuuvlOo=" data-language="html"}
<input type="reset" value="Reset the form" />
```
:::

::: {#sect2 .code-example}
::: iframe
:::
:::
:::

### Omitting the value attribute {#omitting_the_value_attribute}

::: section-content
If you don\'t specify a `value`, you get a button with the default label
(typically \"Reset,\" but this will vary depending on the [user
agent](https://developer.mozilla.org/en-US/docs/Glossary/User_agent)):

::: code-example
[html]{.language-name}

``` {signature="iAibKstbYIjQndax3V/srq8jblT4qs56bNSD7qLsw5g=" data-language="html"}
<input type="reset" />
```
:::

::: {#sect3 .code-example}
::: iframe
:::
:::
:::

## Using reset buttons {#using_reset_buttons}

::: section-content
`<input type="reset">` buttons are used to reset forms. If you want to
create a custom button and then customize the behavior using JavaScript,
you need to use [`<input type="button">`](button), or better still, a
[`<button>`](../button) element.
:::

### A simple reset button {#a_simple_reset_button}

::: section-content
We\'ll begin by creating a simple reset button:

::: code-example
[html]{.language-name}

``` {signature="Opl3QihR5Mhz2wa3Xx50+WGt6GXfaqVID3Ye+VzwMjY=" data-language="html"}
<form>
  
    <label for="example">Type in some sample text</label>
    <input id="example" type="text" />
  
  
    <input type="reset" value="Reset the form" />
  
</form>
```
:::

This renders like so:

::: {#sect4 .code-example}
::: iframe
:::
:::

Try entering some text into the text field, and then pressing the reset
button.
:::

### Adding a reset keyboard shortcut {#adding_a_reset_keyboard_shortcut}

::: section-content
To add a keyboard shortcut to a reset button --- just as you would with
any [`<input>`](../input) for which it makes sense --- you use the
[`accesskey`](../../global_attributes#accesskey) global attribute.

In this example, [r]{.kbd} is specified as the access key (you\'ll need
to press [r]{.kbd} plus the particular modifier keys for your browser/OS
combination; see [`accesskey`](../../global_attributes#accesskey) for a
useful list of those).

::: code-example
[html]{.language-name}

``` {signature="zbdhn8Y6s2WzA2+iVL+lInnHrsNFd+FZI6EfOCpygg0=" data-language="html"}
<form>
  
    <label for="example">Type in some sample text</label>
    <input id="example" type="text" />
  
  
    <input type="reset" value="Reset the form" accesskey="r" />
  
</form>
```
:::

::: {#sect5 .code-example}
::: iframe
:::
:::

The problem with the above example is that there\'s no way for the user
to know what the access key is! This is especially true since the
modifiers are typically non-standard to avoid conflicts. When building a
site, be sure to provide this information in a way that doesn\'t
interfere with the site design (for example by providing an easily
accessible link that points to information on what the site access keys
are). Adding a tooltip to the button (using the
[`title`](../../global_attributes#title) attribute) can also help,
although it\'s not a complete solution for accessibility purposes.
:::

### Disabling and enabling a reset button {#disabling_and_enabling_a_reset_button}

::: section-content
To disable a reset button, specify the [`disabled`](../input#disabled)
attribute on it, like so:

::: code-example
[html]{.language-name}

``` {signature="x5/neyc9WZi/gwwktShDOF40zsR3sRcsE0gHjs3Qw24=" data-language="html"}
<input type="reset" value="Disabled" disabled />
```
:::

You can enable and disable buttons at run time by setting `disabled` to
`true` or `false`; in JavaScript this looks like `btn.disabled = true`
or `btn.disabled = false`.

::: {#sect6 .notecard .note}
**Note:** See the
[`<input type="button">`](button#disabling_and_enabling_a_button) page
for more ideas about enabling and disabling buttons.
:::
:::

## Validation

::: section-content
Buttons don\'t participate in constraint validation; they have no real
value to be constrained.
:::

## Examples

::: section-content
We\'ve included simple examples above. There isn\'t really anything more
to say about reset buttons.
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
  ------------------------------------------------------------------------------------------------------------------------------
  Specification
  ------------------------------------------------------------------------------------------------------------------------------
  [HTML Standard\
  [\#
  reset-button-state-(type=reset)]{.small}](https://html.spec.whatwg.org/multipage/input.html#reset-button-state-(type=reset))

  ------------------------------------------------------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
  --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
            Desktop                                                                                                                                                                       Mobile                                                                                                                                                                  
  --------- --------- ------ -------------------------------------------------------------------------------------------------------------------------------- ---------- ------- -------- --------- --------- -------------------------------------------------------------------------------------------------------------------------------- --------- -------- ----------
            Chrome    Edge   Firefox                                                                                                                          Internet   Opera   Safari   WebView   Chrome    Firefox for Android                                                                                                              Opera     Safari   Samsung
                                                                                                                                                              Explorer                    Android   Android                                                                                                                                    Android   on IOS   Internet

  `reset`   1         12     1                                                                                                                                Yes        15      1        4.4       18        4                                                                                                                                14        1        1.0
                                                                                                                                                                                                                                                                                                                                                                  
                             Unlike other browsers, Firefox by default [persists the dynamic disabled                                                                                                         Unlike other browsers, Firefox by default [persists the dynamic disabled                                                                            
                             state](https://stackoverflow.com/questions/5985839/bug-with-firefox-disabled-attribute-of-input-not-resetting-when-refreshing)                                                   state](https://stackoverflow.com/questions/5985839/bug-with-firefox-disabled-attribute-of-input-not-resetting-when-refreshing)                      
                             of a `<button>` across page loads. Use the                                                                                                                                       of a `<button>` across page loads. Use the                                                                                                          
                             [`autocomplete`](https://developer.mozilla.org/docs/Web/HTML/Element/button#attr-autocomplete) attribute to control this                                                         [`autocomplete`](https://developer.mozilla.org/docs/Web/HTML/Element/button#attr-autocomplete) attribute to control this                            
                             feature.                                                                                                                                                                         feature.                                                                                                                                            
  --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
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
[https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/reset](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/reset){._attribution-link}
:::
