

# \<i\>: The Idiomatic Text element



::: section-content
The `<i>` [HTML](../index) element represents a range of text that is
set off from the normal text for some reason, such as idiomatic text,
technical terms, taxonomical designations, among others. Historically,
these have been presented using italicized type, which is the original
source of the `<i>` naming of this element.
:::

## Try it {#try_it}

::: section-content
::: iframe
::: {.output-header .border-rounded-top}
#### HTML Demo: \<i\> {#html-demo-i .output-heading}

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
    <p>I looked at it and thought <i>This can't be real!</i></p>

    <p><i>Musa</i> is one of two or three genera in the family <i>Musaceae</i>; it includes bananas and plantains.</p>

    <p>
      The term <i>bandwidth</i> describes the measure of how much information can pass through a data connection in a given
      amount of time.
    </p>
:::
:::

::: {#css-panel .section .hidden tabindex="0" role="tabpanel" aria-labelledby="css" aria-hidden="true"}
::: {#css-editor}
    /* stylelint-disable-next-line block-no-empty */
    i {
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
-   Use the `<i>` element for text that is set off from the normal prose
    for readability reasons. This would be a range of text with
    different semantic meaning than the surrounding text. Among the use
    cases for the `<i>` element are spans of text representing a
    different quality or mode of text, such as:
    -   Alternative voice or mood
    -   Taxonomic designations (such as the genus and species \"*Homo
        sapiens*\")
    -   Idiomatic terms from another language (such as \"*et cetera*\");
        these should include the [`lang`](../global_attributes#lang)
        attribute to identify the language
    -   Technical terms
    -   Transliterations
    -   Thoughts (such as \"She wondered, *What is this writer talking
        about, anyway?*\")
    -   Ship or vessel names in Western writing systems (such as \"They
        searched the docks for the *Empress of the Galaxy*, the ship to
        which they were assigned.\")
-   In earlier versions of the HTML specification, the `<i>` element was
    merely a presentational element used to display text in italics,
    much like the `<b>` element was used to display text in bold
    letters. This is no longer true, as these tags now define semantics
    rather than typographic appearance. A browser will typically still
    display the contents of the `<i>` element in italic type, but is, by
    definition, no longer required to do so. To display text in italic
    type, authors should use the CSS
    [`font-style`](https://developer.mozilla.org/en-US/docs/Web/CSS/font-style)
    property.
-   Be sure the text in question is not actually more appropriately
    marked up with another element.
    -   Use [`<em>`](em) to indicate stress emphasis.
    -   Use [`<strong>`](strong) to indicate importance, seriousness, or
        urgency.
    -   Use [`<mark>`](mark) to indicate relevance.
    -   Use [`<cite>`](cite) to mark up the name of a work, such as a
        book, play, or song.
    -   Use [`<dfn>`](dfn) to mark up the defining instance of a term.
:::

## Examples

::: section-content
This example demonstrates using the `<i>` element to mark text that is
in another language.

::: code-example
[html]{.language-name}

``` {signature="PHmI/0yafArFd8LM2S9O2dl46U8y63Akk5NuGMk8T24=" data-language="html"}
<p>
  The Latin phrase <i lang="la">Veni, vidi, vici</i> is often mentioned in
  music, art, and literature.
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
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/generic_role"><code>generic</code></a></td>
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
  ---------------------------------------------------------------------------------------------------------
  Specification
  ---------------------------------------------------------------------------------------------------------
  [HTML Standard\
  [\#
  the-i-element]{.small}](https://html.spec.whatwg.org/multipage/text-level-semantics.html#the-i-element)

  ---------------------------------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
        Desktop                                                         Mobile                                                                                   
  ----- --------- ------ --------- ------------------- ------- -------- ----------------- ---------------- --------------------- --------------- --------------- ------------------
        Chrome    Edge   Firefox   Internet Explorer   Opera   Safari   WebView Android   Chrome Android   Firefox for Android   Opera Android   Safari on IOS   Samsung Internet
  `i`   1         12     1         Yes                 15      ≤4       4.4               18               4                     14              ≤3.2            1.0
:::

## See also {#see_also}

::: section-content
-   [`<em>`](em)
-   Other italicized elements: [`<var>`](var), [`<dfn>`](dfn),
    [`<cite>`](cite), [`<address>`](address)
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Element/i](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/i){._attribution-link}
:::
