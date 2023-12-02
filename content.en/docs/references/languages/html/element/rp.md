

# \<rp\>: The Ruby Fallback Parenthesis element



::: section-content
The `<rp>` [HTML](../index) element is used to provide fall-back
parentheses for browsers that do not support display of ruby annotations
using the [`<ruby>`](ruby) element. One `<rp>` element should enclose
each of the opening and closing parentheses that wrap the [`<rt>`](rt)
element that contains the annotation\'s text.
:::

## Try it {#try_it}

::: section-content
::: iframe
::: {.output-header .border-rounded-top}
#### HTML Demo: \<rp\> {#html-demo-rp .output-heading}

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
:::

## Attributes

::: section-content
This element only includes the [global
attributes](../global_attributes).
:::

## Usage notes {#usage_notes}

::: section-content
-   Ruby annotations are for showing pronunciation of East Asian
    characters, like using Japanese furigana or Taiwanese bopomofo
    characters. The `<rp>` element is used in the case of lack of
    [`<ruby>`](ruby) element support; the `<rp>` content provides what
    should be displayed in order to indicate the presence of a ruby
    annotation, usually parentheses.
:::

## Examples

### Using ruby annotations {#using_ruby_annotations}

::: section-content
This example uses ruby annotations to display the
[Romaji](https://en.wikipedia.org/wiki/Romaji){target="_blank"}
equivalents for each character.

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

See the article about the [`<ruby>`](ruby) element for further examples.
:::

### Without ruby support {#without_ruby_support}

::: section-content
If your browser does not support ruby annotations, the result looks like
this instead:

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
<td>None.</td>
</tr>
<tr class="even">
<th scope="row">Permitted content</th>
<td>Text</td>
</tr>
<tr class="odd">
<th scope="row">Tag omission</th>
<td>The end tag can be omitted if the element is immediately followed by
an <a href="rt"><code>&lt;rt&gt;</code></a> or another
<code>&lt;rp&gt;</code> element, or if there is no more content in the
parent element.</td>
</tr>
<tr class="even">
<th scope="row">Permitted parents</th>
<td>A <a href="ruby"><code>&lt;ruby&gt;</code></a> element.
<code>&lt;rp&gt;</code> must be positioned immediately before or after
an <a href="rt"><code>&lt;rt&gt;</code></a> element.</td>
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
  the-rp-element]{.small}](https://html.spec.whatwg.org/multipage/text-level-semantics.html#the-rp-element)

  -----------------------------------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
         Desktop                                                         Mobile                                                                                   
  ------ --------- ------ --------- ------------------- ------- -------- ----------------- ---------------- --------------------- --------------- --------------- ------------------
         Chrome    Edge   Firefox   Internet Explorer   Opera   Safari   WebView Android   Chrome Android   Firefox for Android   Opera Android   Safari on IOS   Samsung Internet
  `rp`   5         79     38        5                   15      5        4.4               18               38                    14              4.2             1.0
:::

## See also {#see_also}

::: section-content
-   [`<ruby>`](ruby)
-   [`<rt>`](rt)
-   [`<rb>`](rb)
-   [`<rtc>`](rtc)
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Element/rp](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/rp){._attribution-link}
:::
