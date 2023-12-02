

# \<blockquote\>: The Block Quotation element



::: section-content
The `<blockquote>` [HTML](../index) element indicates that the enclosed
text is an extended quotation. Usually, this is rendered visually by
indentation (see [Notes](#usage_notes) for how to change it). A URL for
the source of the quotation may be given using the `cite` attribute,
while a text representation of the source can be given using the
[`<cite>`](cite) element.
:::

## Try it {#try_it}

::: section-content
::: iframe
::: {.output-header .border-rounded-top}
#### HTML Demo: \<blockquote\> {#html-demo-blockquote .output-heading}

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
    <blockquote cite="https://www.huxley.net/bnw/four.html">
      <p>Words can be like X-rays, if you use them properly—they’ll go through anything. You read and you’re pierced.</p>
      <footer>—Aldous Huxley, <cite>Brave New World</cite></footer>
    </blockquote>
:::
:::

::: {#css-panel .section .hidden tabindex="0" role="tabpanel" aria-labelledby="css" aria-hidden="true"}
::: {#css-editor}
    blockquote {
      margin: 0;
    }

    blockquote p {
      padding: 15px;
      background: #eee;
      border-radius: 5px;
    }

    blockquote p::before {
      content: '\201C';
    }

    blockquote p::after {
      content: '\201D';
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
This element\'s attributes include the [global
attributes](../global_attributes).

[`cite`](#cite)

:   A URL that designates a source document or message for the
    information quoted. This attribute is intended to point to
    information explaining the context or the reference for the quote.
:::

## Usage notes {#usage_notes}

::: section-content
To change the indentation applied to the quoted text, use the
[CSS](https://developer.mozilla.org/en-US/docs/Glossary/CSS)
[`margin-left`](https://developer.mozilla.org/en-US/docs/Web/CSS/margin-left)
and/or
[`margin-right`](https://developer.mozilla.org/en-US/docs/Web/CSS/margin-right)
properties, or the
[`margin`](https://developer.mozilla.org/en-US/docs/Web/CSS/margin)
shorthand property.

To include shorter quotes inline rather than in a separate block, use
the [`<q>`](q) (Quotation) element.
:::

## Examples

::: section-content
This example demonstrates the use of the `<blockquote>` element to quote
a passage from [RFC
1149](https://datatracker.ietf.org/doc/html/rfc1149){target="_blank"},
*A Standard for the Transmission of IP Datagrams on Avian Carriers*.

::: code-example
[html]{.language-name}

``` {signature="3scoGfNdHTCKFbINp0K+K1Bn0Bybi4uSbcB1pzqmeeA=" data-language="html"}
<blockquote cite="https://datatracker.ietf.org/doc/html/rfc1149">
  <p>
    Avian carriers can provide high delay, low throughput, and low altitude
    service. The connection topology is limited to a single point-to-point path
    for each carrier, used with standard carriers, but many carriers can be used
    without significant interference with each other, outside early spring. This
    is because of the 3D ether space available to the carriers, in contrast to
    the 1D ether used by IEEE802.3. The carriers have an intrinsic collision
    avoidance system, which increases availability.
  </p>
</blockquote>
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
<td><a href="../content_categories#flow_content">Flow content</a>,
sectioning root, palpable content.</td>
</tr>
<tr class="even">
<th scope="row">Permitted content</th>
<td><a href="../content_categories#flow_content">Flow content</a>.</td>
</tr>
<tr class="odd">
<th scope="row">Tag omission</th>
<td>None, both the starting and ending tag are mandatory.</td>
</tr>
<tr class="even">
<th scope="row">Permitted parents</th>
<td>Any element that accepts <a
href="../content_categories#flow_content">flow content</a>.</td>
</tr>
<tr class="odd">
<th scope="row">Implicit ARIA role</th>
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/structural_roles#structural_roles_with_html_equivalents"><code>blockquote</code></a></td>
</tr>
<tr class="even">
<th scope="row">Permitted ARIA roles</th>
<td>Any</td>
</tr>
<tr class="odd">
<th scope="row">DOM interface</th>
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLQuoteElement"><code>HTMLQuoteElement</code></a></td>
</tr>
</tbody>
</table>

</figure>
:::

## Specifications

::: _table
  -----------------------------------------------------------------------------------------------------------------------
  Specification
  -----------------------------------------------------------------------------------------------------------------------
  [HTML Standard\
  [\#
  the-blockquote-element]{.small}](https://html.spec.whatwg.org/multipage/grouping-content.html#the-blockquote-element)

  -----------------------------------------------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
                 Desktop                                                         Mobile                                                                                   
  -------------- --------- ------ --------- ------------------- ------- -------- ----------------- ---------------- --------------------- --------------- --------------- ------------------
                 Chrome    Edge   Firefox   Internet Explorer   Opera   Safari   WebView Android   Chrome Android   Firefox for Android   Opera Android   Safari on IOS   Samsung Internet
  `blockquote`   1         12     1         Yes                 15      ≤4       4.4               18               4                     14              ≤3.2            1.0
  `cite`         1         12     1         Yes                 15      ≤4       4.4               18               4                     14              ≤3.2            1.0
:::

## See also {#see_also}

::: section-content
-   The [`<q>`](q) element for inline quotations.
-   The [`<cite>`](cite) element for source citations.
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Element/blockquote](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/blockquote){._attribution-link}
:::
