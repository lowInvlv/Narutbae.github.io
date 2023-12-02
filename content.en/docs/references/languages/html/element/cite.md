

# \<cite\>: The Citation element



::: section-content
The `<cite>` [HTML](../index) element is used to mark up the title of a
cited creative work. The reference may be in an abbreviated form
according to context-appropriate conventions related to citation
metadata.
:::

## Try it {#try_it}

::: section-content
::: iframe
::: {.output-header .border-rounded-top}
#### HTML Demo: \<cite\> {#html-demo-cite .output-heading}

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
    <figure>
      <blockquote>
        <p>It was a bright cold day in April, and the clocks were striking thirteen.</p>
      </blockquote>
      <figcaption>
        First sentence in <cite><a href="http://www.george-orwell.org/1984/0.html">Nineteen Eighty-Four</a></cite> by George
        Orwell (Part 1, Chapter 1).
      </figcaption>
    </figure>
:::
:::

::: {#css-panel .section .hidden tabindex="0" role="tabpanel" aria-labelledby="css" aria-hidden="true"}
::: {#css-editor}
    /* stylelint-disable-next-line block-no-empty */
    cite {
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
In the context of the `<cite>` element, a creative work that might be
cited could be, for example, one of the following:

-   A book
-   A research paper
-   An essay
-   A poem
-   A musical score
-   A song
-   A play or film script
-   A film
-   A television show
-   A game
-   A sculpture
-   A painting
-   A theatrical production
-   A play
-   An opera
-   A musical
-   An exhibition
-   A legal case report
-   A computer program
-   A website
-   A web page
-   A blog post or comment
-   A forum post or comment
-   A tweet
-   A Facebook post
-   A written or oral statement
-   And so forth.

To include a reference to the source of quoted material which is
contained within a [`<blockquote>`](blockquote) or [`<q>`](q) element,
use the [`cite`](blockquote#cite) attribute on the element.

Typically, browsers style the contents of a `<cite>` element in italics
by default. To avoid this, apply the CSS
[`font-style`](https://developer.mozilla.org/en-US/docs/Web/CSS/font-style)
property to the `<cite>` element.
:::

## Examples

::: section-content
::: code-example
[html]{.language-name}

``` {signature="sVzvdVHFMhCLClfm9x+0sMmNKhAojkzC1IELrdzleHk=" data-language="html"}
<p>More information can be found in <cite>[ISO-0000]</cite>.</p>
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
  ---------------------------------------------------------------------------------------------------------------
  Specification
  ---------------------------------------------------------------------------------------------------------------
  [HTML Standard\
  [\#
  the-cite-element]{.small}](https://html.spec.whatwg.org/multipage/text-level-semantics.html#the-cite-element)

  ---------------------------------------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
           Desktop                                                         Mobile                                                                                   
  -------- --------- ------ --------- ------------------- ------- -------- ----------------- ---------------- --------------------- --------------- --------------- ------------------
           Chrome    Edge   Firefox   Internet Explorer   Opera   Safari   WebView Android   Chrome Android   Firefox for Android   Opera Android   Safari on IOS   Samsung Internet
  `cite`   1         12     1         Yes                 15      ≤4       4.4               18               4                     14              ≤3.2            1.0
:::

## See also {#see_also}

::: section-content
-   The element [`<blockquote>`](blockquote) for long quotations.
-   The element [`<q>`](q) for inline quotations and the
    [`cite`](q#cite) attribute.
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Element/cite](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/cite){._attribution-link}
:::
