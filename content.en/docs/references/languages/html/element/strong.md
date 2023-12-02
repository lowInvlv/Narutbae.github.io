

# \<strong\>: The Strong Importance element



::: section-content
The `<strong>` [HTML](../index) element indicates that its contents have
strong importance, seriousness, or urgency. Browsers typically render
the contents in bold type.
:::

## Try it {#try_it}

::: section-content
::: iframe
::: {.output-header .border-rounded-top}
#### HTML Demo: \<strong\> {#html-demo-strong .output-heading}

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
      ... the most important rule, the rule you can never forget, no matter how much he cries, no matter how much he begs:
      <strong>never feed him after midnight</strong>.
    </p>
:::
:::

::: {#css-panel .section .hidden tabindex="0" role="tabpanel" aria-labelledby="css" aria-hidden="true"}
::: {#css-editor}
    p {
      font-size: 1rem;
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
The `<strong>` element is for content that is of \"strong importance,\"
including things of great seriousness or urgency (such as warnings).
This could be a sentence that is of great importance to the whole page,
or you could merely try to point out that some words are of greater
importance compared to nearby content.

Typically this element is rendered by default using a bold font weight.
However, it should *not* be used to apply bold styling; use the CSS
[`font-weight`](https://developer.mozilla.org/en-US/docs/Web/CSS/font-weight)
property for that purpose. Use the [`<b>`](b) element to draw attention
to certain text without indicating a higher level of importance. Use the
[`<em>`](em) element to mark text that has stress emphasis.

Another accepted use for `<strong>` is to denote the labels of
paragraphs which represent notes or warnings within the text of a page.
:::

### \<b\> vs. \<strong\> {#b_vs._strong}

::: section-content
It is often confusing to new developers why there are so many ways to
express the same thing on a rendered website. [`<b>`](b) and `<strong>`
are perhaps one of the most common sources of confusion, causing
developers to ask \"Should I use `<b>` or `<strong>`? Don\'t they both
do the same thing?\"

Not exactly. The `<strong>` element is for content that is of greater
importance, while the `<b>` element is used to draw attention to text
without indicating that it\'s more important.

It may help to realize that both are valid and semantic elements in HTML
and that it\'s a coincidence that they both have the same default
styling (boldface) in most browsers (although some older browsers
actually underline `<strong>`). Each element is meant to be used in
certain types of scenarios, and if you want to bold text for decoration,
you should instead actually use the CSS
[`font-weight`](https://developer.mozilla.org/en-US/docs/Web/CSS/font-weight)
property.

The intended meaning or purpose of the enclosed text should be what
determines which element you use. Communicating meaning is what
semantics are all about.
:::

### \<em\> vs. \<strong\> {#em_vs._strong}

::: section-content
Adding to the confusion is the fact that while HTML 4 defined `<strong>`
as indicating a stronger emphasis, HTML 5 defines `<strong>` as
representing \"strong importance for its contents.\" This is an
important distinction to make.

While `<em>` is used to change the meaning of a sentence as spoken
emphasis does (\"I *love* carrots\" vs. \"I love *carrots*\"),
`<strong>` is used to give portions of a sentence added importance
(e.g., \"**Warning!** This is **very dangerous.**\") Both `<strong>` and
`<em>` can be nested to increase the relative degree of importance or
stress emphasis, respectively.
:::

## Examples

### Basic example {#basic_example}

::: section-content
::: code-example
[html]{.language-name}

``` {signature="+ia1N9Cr/Ak2PJw0ZzSr6MjvzwYt24RhK5lB0/ynBVo=" data-language="html"}
<p>
  Before proceeding, <strong>make sure you put on your safety goggles</strong>.
</p>
```
:::

#### Result

::: {#sect1 .code-example}
::: iframe
:::
:::
:::

### Labeling warnings {#labeling_warnings}

::: section-content
::: code-example
[html]{.language-name}

``` {signature="aRvQkg5EdBGHvnO/h9OSM9U3Z0rxY/xx8glsxw4OjgM=" data-language="html"}
<p>
  <strong>Important:</strong> Before proceeding, make sure you add plenty of
  butter.
</p>
```
:::

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
<td>None; must have both a start tag and an end tag.</td>
</tr>
<tr class="even">
<th scope="row">Permitted parents</th>
<td>Any element that accepts <a
href="../content_categories#phrasing_content">phrasing content</a>, or
any element that accepts <a
href="../content_categories#flow_content">flow content</a>.</td>
</tr>
<tr class="odd">
<th scope="row">Implicit ARIA role</th>
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/structural_roles#structural_roles_with_html_equivalents"><code>strong</code></a></td>
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
  -------------------------------------------------------------------------------------------------------------------
  Specification
  -------------------------------------------------------------------------------------------------------------------
  [HTML Standard\
  [\#
  the-strong-element]{.small}](https://html.spec.whatwg.org/multipage/text-level-semantics.html#the-strong-element)

  -------------------------------------------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
  ---------------------------------------------------------------------------------------------------------------------------------------
             Desktop                                                          Mobile                                           
  ---------- --------- ------ ------------------- ---------- ------- -------- --------- --------- --------- --------- -------- ----------
             Chrome    Edge   Firefox             Internet   Opera   Safari   WebView   Chrome    Firefox   Opera     Safari   Samsung
                                                  Explorer                    Android   Android   for       Android   on IOS   Internet
                                                                                                  Android                      

  `strong`   1         12     1                   Yes        15      ≤4       4.4       18        4         14        ≤3.2     1.0
                                                                                                                               
                              Before Firefox 4,                                                                                
                              creating a                                                                                       
                              `<strong>` element                                                                               
                              incorrectly                                                                                      
                              resulted in an                                                                                   
                              `HTMLSpanElement`                                                                                
                              object, instead of                                                                               
                              the expected                                                                                     
                              `HTMLElement`.                                                                                   
  ---------------------------------------------------------------------------------------------------------------------------------------
:::

## See also {#see_also}

::: section-content
-   The [`<b>`](b) element
-   The [`<em>`](em) element
-   The
    [`font-weight`](https://developer.mozilla.org/en-US/docs/Web/CSS/font-weight)
    property
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Element/strong](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/strong){._attribution-link}
:::
