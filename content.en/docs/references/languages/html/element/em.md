

# \<em\>: The Emphasis element



::: section-content
The `<em>` [HTML](../index) element marks text that has stress emphasis.
The `<em>` element can be nested, with each level of nesting indicating
a greater degree of emphasis.
:::

## Try it {#try_it}

::: section-content
::: iframe
::: {.output-header .border-rounded-top}
#### HTML Demo: \<em\> {#html-demo-em .output-heading}

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
    <p>Get out of bed <em>now</em>!</p>

    <p>We <em>had</em> to do something about it.</p>

    <p>This is <em>not</em> a drill!</p>
:::
:::

::: {#css-panel .section .hidden tabindex="0" role="tabpanel" aria-labelledby="css" aria-hidden="true"}
::: {#css-editor}
    /* stylelint-disable-next-line block-no-empty */
    em {
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
The `<em>` element is for words that have a stressed emphasis compared
to surrounding text, which is often limited to a word or words of a
sentence and affects the meaning of the sentence itself.

Typically this element is displayed in italic type. However, it should
not be used to apply italic styling; use the CSS
[`font-style`](https://developer.mozilla.org/en-US/docs/Web/CSS/font-style)
property for that purpose. Use the [`<cite>`](cite) element to mark the
title of a work (book, play, song, etc.). Use the [`<i>`](i) element to
mark text that is in an alternate tone or mood, which covers many common
situations for italics such as scientific names or words in other
languages. Use the [`<strong>`](strong) element to mark text that has
greater importance than surrounding text.
:::

### \<i\> vs. \<em\> {#i_vs._em}

::: section-content
Some developers may be confused by how multiple elements seemingly
produce similar visual results. `<em>` and `<i>` are a common example,
since they both italicize text. What\'s the difference? Which should you
use?

By default, the visual result is the same. However, the semantic meaning
is different. The `<em>` element represents stress emphasis of its
contents, while the `<i>` element represents text that is set off from
the normal prose, such as a foreign word, fictional character thoughts,
or when the text refers to the definition of a word instead of
representing its semantic meaning. (The title of a work, such as the
name of a book or movie, should use `<cite>`.)

This means the right one to use depends on the situation. Neither is for
purely decorative purposes, that\'s what CSS styling is for.

An example for `<em>` could be: \"Just *do* it already!\", or: \"We
*had* to do something about it\". A person or software reading the text
would pronounce the words in italics with an emphasis, using verbal
stress.

An example for `<i>` could be: \"The *Queen Mary* sailed last night\".
Here, there is no added emphasis or importance on the word \"Queen
Mary\". It is merely indicated that the object in question is not a
queen named Mary, but a ship named *Queen Mary*. Another example for
`<i>` could be: \"The word *the* is an article\".
:::

## Examples

::: section-content
In this example, the `<em>` element is used to highlight an implicit or
explicit contrast between two ingredient lists:

::: code-example
[html]{.language-name}

``` {signature="UXf1xt3uyeRdmREApaSKk1UzFYim5tpPfITzH0C3tD4=" data-language="html"}
<p>
  Ice cream is made with milk, sweetener, and cream. Frozen custard, on the
  other hand, is made of milk, cream, sweetener, and <em>egg yolks</em>.
</p>
```
:::
:::

### Result

::: section-content
::: {#sect1 .code-example}
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
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/structural_roles#structural_roles_with_html_equivalents"><code>emphasis</code></a></td>
</tr>
<tr class="even">
<th scope="row">Permitted ARIA roles</th>
<td>Any</td>
</tr>
<tr class="odd">
<th scope="row">DOM interface</th>
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement"><code>HTMLElement</code></a>
Up to Gecko 1.9.2 (Firefox 4) inclusive, Firefox implements the <a
href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLSpanElement"><code>HTMLSpanElement</code></a>
interface for this element.</td>
</tr>
</tbody>
</table>

</figure>
:::

## Specifications

::: _table
  -----------------------------------------------------------------------------------------------------------
  Specification
  -----------------------------------------------------------------------------------------------------------
  [HTML Standard\
  [\#
  the-em-element]{.small}](https://html.spec.whatwg.org/multipage/text-level-semantics.html#the-em-element)

  -----------------------------------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
         Desktop                                                         Mobile                                                                                   
  ------ --------- ------ --------- ------------------- ------- -------- ----------------- ---------------- --------------------- --------------- --------------- ------------------
         Chrome    Edge   Firefox   Internet Explorer   Opera   Safari   WebView Android   Chrome Android   Firefox for Android   Opera Android   Safari on IOS   Samsung Internet
  `em`   1         12     1         Yes                 15      ≤4       4.4               18               4                     14              ≤3.2            1.0
:::

## See also {#see_also}

::: section-content
-   [`<i>`](i)
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Element/em](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/em){._attribution-link}
:::
