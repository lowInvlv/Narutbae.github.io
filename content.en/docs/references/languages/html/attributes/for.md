

# HTML attribute: for



::: section-content
The `for` attribute is an allowed attribute for
[`<label>`](../element/label) and [`<output>`](../element/output). When
used on a `<label>` element it indicates the form element that this
label describes. When used on an `<output>` element it allows for an
explicit relationship between the elements that represent values which
are used in the output.
:::

## Usage

::: section-content
When used as an attribute of `<label>`, the `for` attribute has a value
which is the `id` of the form element it relates to.

::: code-example
[html]{.language-name}

``` {signature="k90DFR/sdhD7TkaAGdVvWQdQG3HU2AzS8of0F0qC6Jg=" data-language="html"}
<label for="username">Your name</label> <input type="text" id="username" />
```
:::

When used as an attribute of `<output>`, the `for` attribute has a value
which is a space separated list of the `id` values of the elements which
are used to create the output.

::: code-example
[html]{.language-name}

``` {signature="3QYBkr0U2S7ekr01qqTzYcFYMkyK0jMTQAncV7h+xwk=" data-language="html"}
<input type="range" id="b" name="b" value="50" /> +
<input type="number" id="a" name="a" value="10" /> =
<output name="result" for="a b">60</output>
```
:::
:::

## Examples

::: section-content
See examples of usage on the element pages for
[`<label>`](../element/label) and [`<output>`](../element/output).
:::

## Specifications

::: _table
  ------------------------------------------------------------------------------------------------------
  Specification
  ------------------------------------------------------------------------------------------------------
  [HTML Standard\
  [\# attr-label-for]{.small}](https://html.spec.whatwg.org/multipage/forms.html#attr-label-for)

  [HTML Standard\
  [\#
  attr-output-for]{.small}](https://html.spec.whatwg.org/multipage/form-elements.html#attr-output-for)
  ------------------------------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
          Desktop                                                         Mobile                                                                                   
  ------- --------- ------ --------- ------------------- ------- -------- ----------------- ---------------- --------------------- --------------- --------------- ------------------
          Chrome    Edge   Firefox   Internet Explorer   Opera   Safari   WebView Android   Chrome Android   Firefox for Android   Opera Android   Safari on IOS   Samsung Internet
  `for`   10        ≤18    4         No                  11      7        4.4               18               4                     11              7               1.0
:::

::: _table
          Desktop                                                         Mobile                                                                                   
  ------- --------- ------ --------- ------------------- ------- -------- ----------------- ---------------- --------------------- --------------- --------------- ------------------
          Chrome    Edge   Firefox   Internet Explorer   Opera   Safari   WebView Android   Chrome Android   Firefox for Android   Opera Android   Safari on IOS   Samsung Internet
  `for`   1         12     1         Yes                 15      ≤4       4.4               18               4                     14              ≤3.2            1.0
:::

### html.elements.label.for

BCD tables only load in the browser with JavaScript enabled. Enable
JavaScript to view data.

### html.elements.output.for

BCD tables only load in the browser with JavaScript enabled. Enable
JavaScript to view data.

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes/for](https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes/for){._attribution-link}
:::
