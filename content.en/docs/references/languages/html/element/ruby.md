

# \<ruby\>: The Ruby Annotation element



::: section-content
The `<ruby>` [HTML](../index) element represents small annotations that
are rendered above, below, or next to base text, usually used for
showing the pronunciation of East Asian characters. It can also be used
for annotating other kinds of text, but this usage is less common.

The term *ruby* originated as [a unit of measurement used by
typesetters](https://en.wikipedia.org/wiki/Agate_(typography)){target="_blank"},
representing the smallest size that text can be printed on newsprint
while remaining legible.
:::

## Try it {#try_it}

::: section-content
::: iframe
::: {.output-header .border-rounded-top}
#### HTML Demo: \<ruby\> {#html-demo-ruby .output-heading}

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
    <ruby> 明日 <rp>(</rp><rt>Ashita</rt><rp>)</rp> </ruby>
:::
:::

::: {#css-panel .section .hidden tabindex="0" role="tabpanel" aria-labelledby="css" aria-hidden="true"}
::: {#css-editor}
    ruby {
      font-size: 2em;
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

## Attributes

::: section-content
This element only includes the [global
attributes](../global_attributes).
:::

## Examples

### Example 1: Character {#example_1_character}

::: section-content
::: code-example
[html]{.language-name}

``` {signature="Y+5q/G3EBi/ofswS5LfyI/FrJgypPFnlRQxpSurHYlA=" data-language="html"}
<ruby>
  漢 <rp>(</rp><rt>Kan</rt><rp>)</rp> 字 <rp>(</rp><rt>ji</rt><rp>)</rp>
</ruby>
```
:::

#### Result

::: {#sect1 .code-example}
::: iframe
:::
:::
:::

### Example 2: Word {#example_2_word}

::: section-content
::: code-example
[html]{.language-name}

``` {signature="kxTOGr0mDKTUUitWa/Wn6g33xUq3S5goNG9ONodGkeA=" data-language="html"}
<ruby> 明日 <rp>(</rp><rt>Ashita</rt><rp>)</rp> </ruby>
```
:::

#### Result {#result_2}

::: {#sect2 .code-example}
::: iframe
:::
:::
:::

## Specifications

::: _table
  ---------------------------------------------------------------------------------------------------------------
  Specification
  ---------------------------------------------------------------------------------------------------------------
  [HTML Standard\
  [\#
  the-ruby-element]{.small}](https://html.spec.whatwg.org/multipage/text-level-semantics.html#the-ruby-element)

  ---------------------------------------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
           Desktop                                                         Mobile                                                                                   
  -------- --------- ------ --------- ------------------- ------- -------- ----------------- ---------------- --------------------- --------------- --------------- ------------------
           Chrome    Edge   Firefox   Internet Explorer   Opera   Safari   WebView Android   Chrome Android   Firefox for Android   Opera Android   Safari on IOS   Samsung Internet
  `ruby`   5         12     38        5                   15      5        4.4               18               38                    14              4.2             1.0
:::

## See also {#see_also}

::: section-content
-   [`<rt>`](rt)
-   [`<rp>`](rp)
-   [`<rb>`](rb)
-   [`<rtc>`](rtc)
-   [`text-transform`](https://developer.mozilla.org/en-US/docs/Web/CSS/text-transform):
    full-size-kana
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Element/ruby](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/ruby){._attribution-link}
:::
