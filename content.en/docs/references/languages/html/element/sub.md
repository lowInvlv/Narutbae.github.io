

# \<sub\>: The Subscript element



::: section-content
The `<sub>` [HTML](../index) element specifies inline text which should
be displayed as subscript for solely typographical reasons. Subscripts
are typically rendered with a lowered baseline using smaller text.
:::

## Try it {#try_it}

::: section-content
::: iframe
::: {.output-header .border-rounded-top}
#### HTML Demo: \<sub\> {#html-demo-sub .output-heading}

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
      Almost every developer's favorite molecule is C<sub>8</sub>H<sub>10</sub>N<sub>4</sub>O<sub>2</sub>, also known as
      "caffeine."
    </p>
:::
:::

::: {#css-panel .section .hidden tabindex="0" role="tabpanel" aria-labelledby="css" aria-hidden="true"}
::: {#css-editor}
    p {
      font:
        1rem 'Fira Sans',
        sans-serif;
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

::: section-content
The `<sub>` element should be used only for typographical reasons---that
is, to change the position of the text to comply with typographical
conventions or standards, rather than solely for presentation or
appearance purposes.

For example, using `<sub>` to style the name of a company which uses
altered baselines in their
[wordmark](https://en.wikipedia.org/wiki/Wordmark){target="_blank"}
would not be appropriate; instead, CSS should be used. For example, you
could use the
[`vertical-align`](https://developer.mozilla.org/en-US/docs/Web/CSS/vertical-align)
property with a declaration like `vertical-align: sub` or, to more
precisely control the baseline shift, `vertical-align: -25%`.

Appropriate use cases for `<sub>` include (but aren\'t necessarily
limited to):

-   Marking up footnote numbers. See [Footnote
    numbers](#footnote_numbers) for an example.
-   Marking up the subscript in mathematical variable numbers (although
    you may also consider using a
    [MathML](https://developer.mozilla.org/en-US/docs/Web/MathML)
    formula for this). See [Variable subscripts](#variable_subscripts).
-   Denoting the number of atoms of a given element within a chemical
    formula (such as every developer\'s best friend, C ~8~ H ~10~ N ~4~
    O ~2~ , otherwise known as \"caffeine\"). See [Chemical
    formulas](#chemical_formulas).
:::

## Examples

### Footnote numbers {#footnote_numbers}

::: section-content
Traditional footnotes are denoted using numbers which are rendered in
subscript. This is a common use case for `<sub>`:

::: code-example
[html]{.language-name}

``` {signature="mTljQa7lvApf0eis59NcyCtwMHPX/Cs6vWDX7xo89p0=" data-language="html"}
<p>
  According to the computations by Nakamura, Johnson, and Mason<sub>1</sub> this
  will result in the complete annihilation of both particles.
</p>
```
:::

#### Result

::: {#sect1 .code-example}
::: iframe
:::
:::
:::

### Variable subscripts {#variable_subscripts}

::: section-content
In mathematics, families of variables related to the same concept (such
as distances along the same axis) are represented using the same
variable name with a subscript following. For example:

::: code-example
[html]{.language-name}

``` {signature="9v18rU9x1ggtVHpn2xw8R6e83DxPWD85oGxBAWVvaFA=" data-language="html"}
<p>
  The horizontal coordinates' positions along the X-axis are represented as
  <var>x<sub>1</sub></var> … <var>x<sub>n</sub></var>.
</p>
```
:::

#### Result {#result_2}

::: {#sect2 .code-example}
::: iframe
:::
:::
:::

### Chemical formulas {#chemical_formulas}

::: section-content
When writing a chemical formula, such as H~2~0, the number of atoms of a
given element within the described molecule is represented using a
subscripted number; in the case of water, the subscripted \"2\"
indicates that there are two atoms of hydrogen in the molecule.

Another example:

::: code-example
[html]{.language-name}

``` {signature="x1TvICWeU/i582STE7h/wzqPLNpRkNxupsR3dUQlTlI=" data-language="html"}
<p>
  Almost every developer's favorite molecule is
  C<sub>8</sub>H<sub>10</sub>N<sub>4</sub>O<sub>2</sub>, which is commonly known
  as "caffeine."
</p>
```
:::

#### Result {#result_3}

::: {#sect3 .code-example}
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
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/structural_roles#structural_roles_with_html_equivalents"><code>subscript</code></a></td>
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
  -------------------------------------------------------------------------------------------------------------------------------
  Specification
  -------------------------------------------------------------------------------------------------------------------------------
  [HTML Standard\
  [\#
  the-sub-and-sup-elements]{.small}](https://html.spec.whatwg.org/multipage/text-level-semantics.html#the-sub-and-sup-elements)

  -------------------------------------------------------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
          Desktop                                                         Mobile                                                                                   
  ------- --------- ------ --------- ------------------- ------- -------- ----------------- ---------------- --------------------- --------------- --------------- ------------------
          Chrome    Edge   Firefox   Internet Explorer   Opera   Safari   WebView Android   Chrome Android   Firefox for Android   Opera Android   Safari on IOS   Samsung Internet
  `sub`   1         12     1         Yes                 15      ≤4       4.4               18               4                     14              ≤3.2            1.0
:::

## See also {#see_also}

::: section-content
-   The [`<sup>`](sup) HTML element that produces superscript. Note that
    you cannot use `sup` and `sub` both at the same time: you need to
    use [MathML](https://developer.mozilla.org/en-US/docs/Web/MathML) to
    produce both a superscript directly above a subscript next to the
    chemical symbol of an element, representing its atomic number and
    its nuclear number.
-   The
    [`<msub>`](https://developer.mozilla.org/en-US/docs/Web/MathML/Element/msub),
    [`<msup>`](https://developer.mozilla.org/en-US/docs/Web/MathML/Element/msup),
    and
    [`<msubsup>`](https://developer.mozilla.org/en-US/docs/Web/MathML/Element/msubsup)
    MathML elements.
-   The CSS
    [`vertical-align`](https://developer.mozilla.org/en-US/docs/Web/CSS/vertical-align)
    property.
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Element/sub](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/sub){._attribution-link}
:::
