

# \<wbr\>: The Line Break Opportunity element



::: section-content
The `<wbr>` [HTML](../index) element represents a word break
opportunity---a position within text where the browser may optionally
break a line, though its line-breaking rules would not otherwise create
a break at that location.
:::

## Try it {#try_it}

::: section-content
::: iframe
::: {.output-header .border-rounded-top}
#### HTML Demo: \<wbr\> {#html-demo-wbr .output-heading}

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
    <div id="example-paragraphs">
      <p>Fernstraßenbauprivatfinanzierungsgesetz</p>
      <p>Fernstraßen<wbr />bau<wbr />privat<wbr />finanzierungs<wbr />gesetz</p>
      <p>Fernstraßen&shy;bau&shy;privat&shy;finanzierungs&shy;gesetz</p>
    
:::
:::

::: {#css-panel .section .hidden tabindex="0" role="tabpanel" aria-labelledby="css" aria-hidden="true"}
::: {#css-editor}
    #example-paragraphs {
      background-color: white;
      overflow: hidden;
      resize: horizontal;
      width: 9rem;
      border: 2px dashed #999;
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

## Notes

::: section-content
On UTF-8 encoded pages, `<wbr>` behaves like the
`U+200B ZERO-WIDTH SPACE` code point. In particular, it behaves like a
Unicode bidi BN code point, meaning it has no effect on
[bidi](https://developer.mozilla.org/en-US/docs/Glossary/BiDi)-ordering:
`<div dir=rtl>123,<wbr>456` displays, when not broken on two
lines, `123,456` and not `456,123`.

For the same reason, the `<wbr>` element does not introduce a hyphen at
the line break point. To make a hyphen appear only at the end of a line,
use the soft hyphen character entity (`&shy;`) instead.
:::

## Examples

::: section-content
*[The Yahoo Style
Guide](https://web.archive.org/web/20121014054923/http://styleguide.yahoo.com/){target="_blank"}*
recommends [breaking a URL *before*
punctuation](https://web.archive.org/web/20121105171040/http://styleguide.yahoo.com/editing/treat-abbreviations-capitalization-and-titles-consistently/website-names-and-addresses){target="_blank"},
to avoid leaving a punctuation mark at the end of the line, which the
reader might mistake for the end of the URL.

::: code-example
[html]{.language-name}

``` {signature="4s7hWl5kN2nPA0+IC1dvaua6h1SuMOc3rJlCmECm5yU=" data-language="html"}
<p>
  http://this<wbr />.is<wbr />.a<wbr />.really<wbr />.long<wbr />.example<wbr />.com/With<wbr />/deeper<wbr />/level<wbr />/pages<wbr />/deeper<wbr />/level<wbr />/pages<wbr />/deeper<wbr />/level<wbr />/pages<wbr />/deeper<wbr />/level<wbr />/pages<wbr />/deeper<wbr />/level<wbr />/pages
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
href="../content_categories#phrasing_content">phrasing content</a>.</td>
</tr>
<tr class="even">
<th scope="row">Permitted content</th>
<td>Empty</td>
</tr>
<tr class="odd">
<th scope="row">Tag omission</th>
<td>It is a <a
href="https://developer.mozilla.org/en-US/docs/Glossary/Void_element">void
element</a>; it must have a start tag, but must not have an end
tag.</td>
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
  -------------------------------------------------------------------------------------------------------------
  Specification
  -------------------------------------------------------------------------------------------------------------
  [HTML Standard\
  [\#
  the-wbr-element]{.small}](https://html.spec.whatwg.org/multipage/text-level-semantics.html#the-wbr-element)

  -------------------------------------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
          Desktop                                                         Mobile                                                                                   
  ------- --------- ------ --------- ------------------- ------- -------- ----------------- ---------------- --------------------- --------------- --------------- ------------------
          Chrome    Edge   Firefox   Internet Explorer   Opera   Safari   WebView Android   Chrome Android   Firefox for Android   Opera Android   Safari on IOS   Samsung Internet
  `wbr`   1         79     1         5.5--7              11.6    4        4.4               18               4                     12              3.2             1.0
:::

## See also {#see_also}

::: section-content
-   [`overflow-wrap`](https://developer.mozilla.org/en-US/docs/Web/CSS/overflow-wrap)
-   [`word-break`](https://developer.mozilla.org/en-US/docs/Web/CSS/word-break)
-   [`hyphens`](https://developer.mozilla.org/en-US/docs/Web/CSS/hyphens)
-   The [`<br>`](br) element
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Element/wbr](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/wbr){._attribution-link}
:::
