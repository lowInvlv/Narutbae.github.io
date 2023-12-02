

# HTML attribute: minlength



::: section-content
The `minlength` attribute defines the minimum [string
length](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/length)
that the user can enter into an [`<input>`](../element/input) or
[`<textarea>`](../element/textarea). The attribute must have an integer
value of 0 or higher.

The length is measured in UTF-16 code units, which ([for most
scripts](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/length#strings_with_length_not_equal_to_the_number_of_characters))
is equivalent to the number of characters. If no `minlength` is
specified, or an invalid value is specified, the input has no minimum
length. This value must be less than or equal to the value of
[maxlength](maxlength), otherwise the value will never be valid, as it
is impossible to meet both criteria.

The input will fail constraint validation if the length of the text
value of the field is less than minlength UTF-16 code units long, with
[`validityState.tooShort`](https://developer.mozilla.org/en-US/docs/Web/API/ValidityState/tooShort)
returning `true`. Constraint validation is only applied when the value
is changed by the user. Once submission fails, some browsers will
display an error message indicating the minimum length required and the
current length.
:::

## Try it {#try_it}

::: section-content
::: iframe
::: {.output-header .border-rounded-top}
#### HTML Demo: minlength {#html-demo-minlength .output-heading}

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
By adding `minlength="5"`, the value must either be empty or five
characters or longer to be valid.

::: code-example
[html]{.language-name}

``` {signature="BVDyOX4r0iz2c7Z3QxxOuELvexWmwfvpHnUK14xF5Mc=" data-language="html"}
<label for="fruit">Enter a fruit name that is at least 5 letters long</label>
<input type="text" minlength="5" id="fruit" />
```
:::

We can use pseudoclasses to style the element based on whether the value
is valid. The value will be valid as long as it is either null (empty)
or five or more characters long. *Lime* is invalid, *lemon is valid*.

::: code-example
[css]{.language-name}

``` {signature="Q8x3i75AtKMOIhTESyx16mmg2Nv/Vgs/sjUou9yeZOs=" data-language="css"}
input {
  border: 2px solid currentcolor;
}
input:invalid {
  border: 2px dashed red;
}
input:invalid:focus {
  background-image: linear-gradient(pink, lightgreen);
}
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
  `minlength`   40        17     51        No                  27      10.1     40                40               51                    27              10.3            4.0
:::

::: _table
                Desktop                                                         Mobile                                                                                   
  ------------- --------- ------ --------- ------------------- ------- -------- ----------------- ---------------- --------------------- --------------- --------------- ------------------
                Chrome    Edge   Firefox   Internet Explorer   Opera   Safari   WebView Android   Chrome Android   Firefox for Android   Opera Android   Safari on IOS   Samsung Internet
  `minlength`   40        17     51        No                  27      10.1     40                40               51                    27              10.3            4.0
:::

### html.elements.input.minlength

BCD tables only load in the browser with JavaScript enabled. Enable
JavaScript to view data.

### html.elements.textarea.minlength

BCD tables only load in the browser with JavaScript enabled. Enable
JavaScript to view data.

## See also {#see_also}

::: section-content
-   [`maxlength`](maxlength)
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
[https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes/minlength](https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes/minlength){._attribution-link}
:::
