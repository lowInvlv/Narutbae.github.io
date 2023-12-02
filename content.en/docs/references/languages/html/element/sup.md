

# \<sup\>: The Superscript element



::: section-content
The `<sup>` [HTML](../index) element specifies inline text which is to
be displayed as superscript for solely typographical reasons.
Superscripts are usually rendered with a raised baseline using smaller
text.
:::

## Try it {#try_it}

::: section-content
::: iframe
::: {.output-header .border-rounded-top}
#### HTML Demo: \<sup\> {#html-demo-sup .output-heading}

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
    <p>The <em>Pythagorean theorem</em> is often expressed as the following equation:</p>

    <p>
      <var>a<sup>2</sup></var> + <var>b<sup>2</sup></var> = <var>c<sup>2</sup></var>
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
The `<sup>` element should only be used for typographical reasons---that
is, to change the position of the text to comply with typographical
conventions or standards, rather than solely for presentation or
appearance purposes.

For example, to style the
[wordmark](https://en.wikipedia.org/wiki/Wordmark){target="_blank"} of a
business or product which uses a raised baseline should be done using
CSS (most likely
[`vertical-align`](https://developer.mozilla.org/en-US/docs/Web/CSS/vertical-align))
rather than `<sup>`. This would be done using, for example,
`vertical-align: super` or, to shift the baseline up 50%,
`vertical-align: 50%`.

Appropriate use cases for `<sup>` include (but aren\'t necessarily
limited to):

-   Displaying exponents, such as \"x ^3^ .\" It may be worth
    considering the use of
    [MathML](https://developer.mozilla.org/en-US/docs/Web/MathML) for
    these, especially in more complex cases. See [Exponents](#exponents)
    under [Examples](#examples) below.
-   Displaying [superior
    lettering](https://en.wikipedia.org/wiki/Superior_letter){target="_blank"},
    which is used in some languages when rendering certain
    abbreviations. For example, in French, the word \"mademoiselle\" can
    be abbreviated \"M ^lle^ \"); this is an acceptable use case. See
    [Superior lettering](#superior_lettering) for examples.
-   Representing ordinal numbers, such as \"4 ^th^ \" instead of
    \"fourth.\" See [Ordinal numbers](#ordinal_numbers) for examples.
:::

## Examples

### Exponents

::: section-content
Exponents, or powers of a number, are among the most common uses of
superscripted text. For example:

::: code-example
[html]{.language-name}

``` {signature="DpXZ/BNHuxtQsdc3kx7MruNXIbi0j2CLfV4RyLBLaYE=" data-language="html"}
<p>
  One of the most common equations in all of physics is <var>E</var>=<var>m</var
  ><var>c</var><sup>2</sup>.
</p>
```
:::

#### Result

::: {#sect1 .code-example}
::: iframe
:::
:::
:::

### Superior lettering {#superior_lettering}

::: section-content
Superior lettering is not technically the same thing as superscript.
However, it is common to use `<sup>` to present superior lettering in
HTML. Among the most common uses of superior lettering is the
presentation of certain abbreviations in French:

::: code-example
[html]{.language-name}

``` {signature="htBaORvyqtGvLwr21mj+XbEeGdAt9HpaTG9h8tV8Y0s=" data-language="html"}
<p>Robert a présenté son rapport à M<sup>lle</sup> Bernard.</p>
```
:::

#### Result {#result_2}

::: {#sect2 .code-example}
::: iframe
:::
:::
:::

### Ordinal numbers {#ordinal_numbers}

::: section-content
Ordinal numbers, such as \"fourth\" in English or \"quinto\" in Spanish
may be abbreviated using numerals and language-specific text rendered in
superscript:

::: code-example
[html]{.language-name}

``` {signature="DrDkUGGmYQZCO+O83waLiV9u43fGlCWrnGALM2vI7zo=" data-language="html"}
<p>
  The ordinal number "fifth" can be abbreviated in various languages as follows:
</p>
<ul>
  <li>English: 5<sup>th</sup></li>
  <li>French: 5<sup>ème</sup></li>
</ul>
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
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/structural_roles#structural_roles_with_html_equivalents"><code>superscript</code></a></td>
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
  `sup`   1         12     1         Yes                 15      ≤4       4.4               18               4                     14              ≤3.2            1.0
:::

## See also {#see_also}

::: section-content
-   The [`<sub>`](sub) HTML element that produces subscripts. Note that
    you cannot use `sub` and `sup` at the same time: you need to use
    [MathML](https://developer.mozilla.org/en-US/docs/Web/MathML) to
    produce both a superscript and a subscript next to the chemical
    symbol of an element, representing its atomic number and its nuclear
    number.
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
[https://developer.mozilla.org/en-US/docs/Web/HTML/Element/sup](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/sup){._attribution-link}
:::
