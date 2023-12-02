

# HTML attribute: maxlength



::: section-content
The `maxlength` attribute defines the maximum [string
length](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/length)
that the user can enter into an [`<input>`](../element/input) or
[`<textarea>`](../element/textarea). The attribute must have an integer
value of 0 or higher.

The length is measured in UTF-16 code units, which ([for most
scripts](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/length#strings_with_length_not_equal_to_the_number_of_characters))
is equivalent to the number of characters. If no `maxlength` is
specified, or an invalid value is specified, the input has no maximum
length.

Any `maxlength` value must be greater than or equal to the value of
[`minlength`](minlength), if present and valid. The input will fail
constraint validation if the length of the text value of the field is
greater than maxlength UTF-16 code units long. Constraint validation is
only applied when the value is changed by the user.
:::

### Constraint validation {#constraint_validation}

::: section-content
While the browser will generally prevent user from entering more text
than the maxlength attribute allows, should the length be longer than
the maxlength allows, the read-only
[`tooLong`](https://developer.mozilla.org/en-US/docs/Web/API/ValidityState/tooLong)
property of a
[`ValidityState`](https://developer.mozilla.org/en-US/docs/Web/API/ValidityState)
object will be true.
:::

## Try it {#try_it}

::: section-content
::: iframe
::: {.output-header .border-rounded-top}
#### HTML Demo: maxlength {#html-demo-maxlength .output-heading}

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
    <label for="name">Product name:</label>
    <input name="name" type="text" value="Shampoo" minlength="3" maxlength="20" required />

    <label for="description">Product description:</label>
    <textarea name="description" minlength="10" maxlength="40" required></textarea>
:::
:::

::: {#css-panel .section .hidden tabindex="0" role="tabpanel" aria-labelledby="css" aria-hidden="true"}
::: {#css-editor}
    label {
      display: block;
      margin-top: 1em;
    }

    input:valid,
    textarea:valid {
      background-color: palegreen;
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

## Examples

::: section-content
::: code-example
[html]{.language-name}

``` {signature="6ccbeNUrp6Dm4PAnSJPQTwdGLtQXwnKcSrq67FxHF88=" data-language="html"}
<input type="password" maxlength="4" />
```
:::

::: {#sect1 .code-example}
::: iframe
:::
:::
:::

## Specifications

::: _table
  --------------------------------------------------------------------------------------------------------------------------------------------
  Specification
  --------------------------------------------------------------------------------------------------------------------------------------------
  [HTML Standard\
  [\#
  the-maxlength-and-minlength-attributes]{.small}](https://html.spec.whatwg.org/multipage/input.html#the-maxlength-and-minlength-attributes)

  --------------------------------------------------------------------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
                Desktop                                                         Mobile                                                                                   
  ------------- --------- ------ --------- ------------------- ------- -------- ----------------- ---------------- --------------------- --------------- --------------- ------------------
                Chrome    Edge   Firefox   Internet Explorer   Opera   Safari   WebView Android   Chrome Android   Firefox for Android   Opera Android   Safari on IOS   Samsung Internet
  `maxlength`   4         12     4         10                  ≤12.1   5        ≤37               18               4                     ≤12.1           5               1.0
:::

::: _table
                Desktop                                                         Mobile                                                                                   
  ------------- --------- ------ --------- ------------------- ------- -------- ----------------- ---------------- --------------------- --------------- --------------- ------------------
                Chrome    Edge   Firefox   Internet Explorer   Opera   Safari   WebView Android   Chrome Android   Firefox for Android   Opera Android   Safari on IOS   Samsung Internet
  `maxlength`   1         12     1         5.5                 ≤12.1   1        4.4               18               4                     ≤12.1           1               1.0
:::

### html.elements.input.maxlength

BCD tables only load in the browser with JavaScript enabled. Enable
JavaScript to view data.

### html.elements.textarea.maxlength

BCD tables only load in the browser with JavaScript enabled. Enable
JavaScript to view data.

## See also {#see_also}

::: section-content
-   [`minlength`](minlength)
-   [`size`](size)
-   [`pattern`](pattern)
-   [Constraint validation](../constraint_validation)
-   [Form
    validation](https://developer.mozilla.org/en-US/docs/Learn/Forms/Form_validation)
-   [`<input>`](../element/input)
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes/maxlength](https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes/maxlength){._attribution-link}
:::
