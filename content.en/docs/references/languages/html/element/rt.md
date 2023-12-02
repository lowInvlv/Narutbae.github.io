

# \<rt\>: The Ruby Text element



::: section-content
The `<rt>` [HTML](../index) element specifies the ruby text component of
a ruby annotation, which is used to provide pronunciation, translation,
or transliteration information for East Asian typography. The `<rt>`
element must always be contained within a [`<ruby>`](ruby) element.
:::

## Try it {#try_it}

::: section-content
::: iframe
::: {.output-header .border-rounded-top}
#### HTML Demo: \<rt\> {#html-demo-rt .output-heading}

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
    <ruby> 漢 <rp>(</rp><rt>kan</rt><rp>)</rp> 字 <rp>(</rp><rt>ji</rt><rp>)</rp> </ruby>
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

See the article about the [`<ruby>`](ruby) element for more examples.
:::

## Attributes

::: section-content
This element only includes the [global
attributes](../global_attributes).
:::

## Examples

### Using ruby annotations {#using_ruby_annotations}

::: section-content
This simple example provides Romaji transliteration for the kanji
characters within the [`<ruby>`](ruby) element:

::: code-example
[html]{.language-name}

``` {signature="ERUjSl+Rnqs4e1ggHovuFevQrhW8y+J1z4R+k7i+98I=" data-language="html"}
<ruby> 漢 <rt>Kan</rt> 字 <rt>ji</rt> </ruby>
```
:::

#### Result

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
<td>None.</td>
</tr>
<tr class="even">
<th scope="row">Permitted content</th>
<td><a href="../content_categories#phrasing_content">Phrasing
content</a>.</td>
</tr>
<tr class="odd">
<th scope="row">Tag omission</th>
<td>The end tag may be omitted if the <code>&lt;rt&gt;</code> element is
immediately followed by an <code>&lt;rt&gt;</code> or <a
href="rp"><code>&lt;rp&gt;</code></a> element, or if there is no more
content in the parent element</td>
</tr>
<tr class="even">
<th scope="row">Permitted parents</th>
<td>A <a href="ruby"><code>&lt;ruby&gt;</code></a> element.</td>
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
  -----------------------------------------------------------------------------------------------------------
  Specification
  -----------------------------------------------------------------------------------------------------------
  [HTML Standard\
  [\#
  the-rt-element]{.small}](https://html.spec.whatwg.org/multipage/text-level-semantics.html#the-rt-element)

  -----------------------------------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
         Desktop                                                         Mobile                                                                                   
  ------ --------- ------ --------- ------------------- ------- -------- ----------------- ---------------- --------------------- --------------- --------------- ------------------
         Chrome    Edge   Firefox   Internet Explorer   Opera   Safari   WebView Android   Chrome Android   Firefox for Android   Opera Android   Safari on IOS   Samsung Internet
  `rt`   5         79     38        5                   15      5        4.4               18               38                    14              4.2             1.0
:::

## See also {#see_also}

::: section-content
-   [`<ruby>`](ruby)
-   [`<rp>`](rp)
-   [`<rb>`](rb)
-   [`<rtc>`](rtc)
-   [`text-transform: full-size-kana`](https://developer.mozilla.org/en-US/docs/Web/CSS/text-transform)
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Element/rt](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/rt){._attribution-link}
:::
