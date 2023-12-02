

# \<var\>: The Variable element



::: section-content
The `<var>` [HTML](../index) element represents the name of a variable
in a mathematical expression or a programming context. It\'s typically
presented using an italicized version of the current typeface, although
that behavior is browser-dependent.
:::

## Try it {#try_it}

::: section-content
::: iframe
::: {.output-header .border-rounded-top}
#### HTML Demo: \<var\> {#html-demo-var .output-heading}

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
    <p>
      The volume of a box is <var>l</var> × <var>w</var> × <var>h</var>, where <var>l</var> represents the length,
      <var>w</var> the width and <var>h</var> the height of the box.
    </p>
:::
:::

::: {#css-panel .section .hidden tabindex="0" role="tabpanel" aria-labelledby="css" aria-hidden="true"}
::: {#css-editor}
    var {
      font-weight: bold;
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

## Attributes

::: section-content
This element only includes the [global
attributes](../global_attributes).
:::

## Usage notes {#usage_notes}

### Related elements {#related_elements}

::: section-content
Other elements that are used in contexts in which `<var>` is commonly
used include:

-   [`<code>`](code): The HTML Code element
-   [`<kbd>`](kbd): The HTML Keyboard input element
-   [`<samp>`](samp): The HTML Sample Output element

If you encounter code that is mistakenly using `<var>` for style
purposes rather than semantic purposes, you should either use a
[`<span>`](span) with appropriate CSS or, an appropriate semantic
element among the following:

-   [`<em>`](em)
-   [`<i>`](i)
-   [`<q>`](q)
:::

### Default style {#default_style}

::: section-content
Most browsers apply
[`font-style`](https://developer.mozilla.org/en-US/docs/Web/CSS/font-style)
to `"italic"` when rendering `<var>`. This can be overridden in CSS,
like this:

::: code-example
[css]{.language-name}

``` {signature="ooDCnAfPzSn74y40bqmjyc49gE3Ng9SrzwFS01bQorU=" data-language="css"}
var {
  font-style: normal;
}
```
:::
:::

## Examples

### Basic example {#basic_example}

::: section-content
Here\'s a simple example, using `<var>` to denote variable names in a
mathematical equation.

::: code-example
[html]{.language-name}

``` {signature="SPY8TiR6LQslieJgDUA+lAn/aZlX4aH+zNwIAY20Nic=" data-language="html"}
<p>A simple equation: <var>x</var> = <var>y</var> + 2</p>
```
:::

#### Result

::: {#sect1 .code-example}
::: iframe
:::
:::
:::

### Overriding the default style {#overriding_the_default_style}

::: section-content
Using CSS, you can override the default style for the `<var>` element.
In this example, variable names are rendered using bold Courier if it\'s
available, otherwise it falls back to the default monospace font.

#### CSS

::: code-example
[css]{.language-name}

``` {signature="eMzwureY2MmO3vFSVx7d6aZJFB1YB0AdLWORvivgdd8=" data-language="css"}
var {
  font:
    bold 15px "Courier",
    "Courier New",
    monospace;
}
```
:::

#### HTML

::: code-example
[html]{.language-name}

``` {signature="RedQ7E9Z7ECjbf9ggcbiAUSJKZSFMtKTwq+CdNFjSAs=" data-language="html"}
<p>
  The variables <var>minSpeed</var> and <var>maxSpeed</var> control the minimum
  and maximum speed of the apparatus in revolutions per minute (RPM).
</p>
```
:::

This HTML uses `<var>` to enclose the names of two variables.

#### Result {#result_2}

::: {#sect2 .code-example}
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
href="../content_categories#phrasing_content">phrasing content</a>,
palpable content.</td>
</tr>
<tr class="even">
<th scope="row">Permitted content</th>
<td><a href="../content_categories#phrasing_content">Phrasing
content</a>.</td>
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
<td><a href="https://www.w3.org/TR/html-aria/#dfn-no-corresponding-role"
target="_blank">No corresponding role</a></td>
</tr>
<tr class="even">
<th scope="row">Permitted ARIA roles</th>
<td>Any</td>
</tr>
<tr class="odd">
<th scope="row">DOM interface</th>
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement"><code>HTMLElement</code></a></td>
</tr>
</tbody>
</table>

</figure>
:::

## Specifications

::: _table
  -------------------------------------------------------------------------------------------------------------
  Specification
  -------------------------------------------------------------------------------------------------------------
  [HTML Standard\
  [\#
  the-var-element]{.small}](https://html.spec.whatwg.org/multipage/text-level-semantics.html#the-var-element)

  -------------------------------------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
          Desktop                                                         Mobile                                                                                   
  ------- --------- ------ --------- ------------------- ------- -------- ----------------- ---------------- --------------------- --------------- --------------- ------------------
          Chrome    Edge   Firefox   Internet Explorer   Opera   Safari   WebView Android   Chrome Android   Firefox for Android   Opera Android   Safari on IOS   Samsung Internet
  `var`   1         12     1         Yes                 15      ≤4       4.4               18               4                     14              ≤3.2            1.0
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Element/var](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/var){._attribution-link}
:::
