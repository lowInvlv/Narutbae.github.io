

# \<mark\>: The Mark Text element



::: section-content
The `<mark>` [HTML](../index) element represents text which is
**marked** or **highlighted** for reference or notation purposes due to
the marked passage\'s relevance in the enclosing context.
:::

## Try it {#try_it}

::: section-content
::: iframe
::: {.output-header .border-rounded-top}
#### HTML Demo: \<mark\> {#html-demo-mark .output-heading}

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
    <p>Search results for "salamander":</p>

    <hr />

    <p>Several species of <mark>salamander</mark> inhabit the temperate rainforest of the Pacific Northwest.</p>

    <p>Most <mark>salamander</mark>s are nocturnal, and hunt for insects, worms, and other small creatures.</p>
:::
:::

::: {#css-panel .section .hidden tabindex="0" role="tabpanel" aria-labelledby="css" aria-hidden="true"}
::: {#css-editor}
    /* stylelint-disable-next-line block-no-empty */
    mark {
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
Typical use cases for `<mark>` include:

-   When used in a quotation ([`<q>`](q)) or block quote
    ([`<blockquote>`](blockquote)), it generally indicates text which is
    of special interest but is not marked in the original source
    material, or material which needs special scrutiny even though the
    original author didn\'t think it was of particular importance. Think
    of this like using a highlighter pen in a book to mark passages that
    you find of interest.
-   Otherwise, `<mark>` indicates a portion of the document\'s content
    which is likely to be relevant to the user\'s current activity. This
    might be used, for example, to indicate the words that matched a
    search operation.
-   Don\'t use `<mark>` for syntax highlighting purposes; instead, use
    the [`<span>`](span) element with appropriate CSS applied to it.

::: {#sect1 .notecard .note}
**Note:** Don\'t confuse `<mark>` with the [`<strong>`](strong) element;
`<mark>` is used to denote content which has a degree of *relevance*,
while `<strong>` indicates spans of text of *importance*.
:::
:::

## Examples

### Marking text of interest {#marking_text_of_interest}

::: section-content
In this first example, a `<mark>` element is used to mark some text
within a quote which is of particular interest to the user.

::: code-example
[html]{.language-name}

``` {signature="4nFU68jtDIfxzlLzp6KADHDnHc7VTZNPH7sKC4csKps=" data-language="html"}
<blockquote>
  It is a period of civil war. Rebel spaceships, striking from a hidden base,
  have won their first victory against the evil Galactic Empire. During the
  battle, <mark>Rebel spies managed to steal secret plans</mark> to the Empire's
  ultimate weapon, the DEATH STAR, an armored space station with enough power to
  destroy an entire planet.
</blockquote>
```
:::

#### Result

::: {#sect2 .code-example}
::: iframe
:::
:::
:::

### Identifying context-sensitive passages {#identifying_context-sensitive_passages}

::: section-content
This example demonstrates using `<mark>` to mark search results within a
passage.

::: code-example
[html]{.language-name}

``` {signature="D6SMpiFU+fIknROdjuudwKfwL3OW6lKXKb1b4sfKCo4=" data-language="html"}
<p>
  It is a dark time for the Rebellion. Although the Death Star has been
  destroyed, <mark class="match">Imperial</mark> troops have driven the Rebel
  forces from their hidden base and pursued them across the galaxy.
</p>

<p>
  Evading the dreaded <mark class="match">Imperial</mark> Starfleet, a group of
  freedom fighters led by Luke Skywalker has established a new secret base on
  the remote ice world of Hoth.
</p>
```
:::

To help distinguish the use of `<mark>` for search results from other
potential usage, this example applies the custom class `"match"` to each
match.

#### Result {#result_2}

::: {#sect3 .code-example}
::: iframe
:::
:::
:::

## Accessibility concerns {#accessibility_concerns}

::: section-content
The presence of the `mark` element is not announced by most screen
reading technology in its default configuration. It can be made to be
announced by using the CSS
[`content`](https://developer.mozilla.org/en-US/docs/Web/CSS/content)
property, along with the
[`::before`](https://developer.mozilla.org/en-US/docs/Web/CSS/::before)
and
[`::after`](https://developer.mozilla.org/en-US/docs/Web/CSS/::after)
pseudo-elements.

::: code-example
[css]{.language-name}

``` {signature="/z/NMcR/fBwUXyOBykZwJXigNSm/zDFjJ3jFTaJYz4E=" data-language="css"}
mark::before,
mark::after {
  clip-path: inset(100%);
  clip: rect(1px, 1px, 1px, 1px);
  height: 1px;
  overflow: hidden;
  position: absolute;
  white-space: nowrap;
  width: 1px;
}

mark::before {
  content: " [highlight start] ";
}

mark::after {
  content: " [highlight end] ";
}
```
:::

Some people who use screen readers deliberately disable announcing
content that creates extra verbosity. Because of this, it is important
to not abuse this technique and only apply it in situations where not
knowing content has been highlighted would adversely affect
understanding.

-   [Short note on making your mark (more accessible) \| The Paciello
    Group](https://www.tpgi.com/short-note-on-making-your-mark-more-accessible/){target="_blank"}
-   [Tweaking Text Level Styles \| Adrian
    Roselli](https://adrianroselli.com/2017/12/tweaking-text-level-styles.html){target="_blank"}
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
  ---------------------------------------------------------------------------------------------------------------
  Specification
  ---------------------------------------------------------------------------------------------------------------
  [HTML Standard\
  [\#
  the-mark-element]{.small}](https://html.spec.whatwg.org/multipage/text-level-semantics.html#the-mark-element)

  ---------------------------------------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
           Desktop                                                         Mobile                                                                                   
  -------- --------- ------ --------- ------------------- ------- -------- ----------------- ---------------- --------------------- --------------- --------------- ------------------
           Chrome    Edge   Firefox   Internet Explorer   Opera   Safari   WebView Android   Chrome Android   Firefox for Android   Opera Android   Safari on IOS   Samsung Internet
  `mark`   7         12     4         9                   11      5.1      4.4               18               4                     14              5               1.0
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Element/mark](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/mark){._attribution-link}
:::
