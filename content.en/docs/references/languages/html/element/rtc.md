

# \<rtc\>: The Ruby Text Container element



::: section-content
::: {#sect1 .notecard .deprecated}
**Deprecated:** This feature is no longer recommended. Though some
browsers might still support it, it may have already been removed from
the relevant web standards, may be in the process of being dropped, or
may only be kept for compatibility purposes. Avoid using it, and update
existing code if possible; see the [compatibility
table](#browser_compatibility) at the bottom of this page to guide your
decision. Be aware that this feature may cease to work at any time.
:::

The `<rtc>` [HTML](../index) element embraces semantic annotations of
characters presented in a ruby of [`<rb>`](rb) elements used inside of
[`<ruby>`](ruby) element. [`<rb>`](rb) elements can have both
pronunciation ([`<rt>`](rt)) and semantic
([`<rtc>`](rtc){aria-current="page"}) annotations.
:::

## Try it {#try_it}

::: section-content
::: iframe
::: {.output-header .border-rounded-top}
#### HTML Demo: \<rtc\> {#html-demo-rtc .output-heading}

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
    <ruby xml:lang="zh-Hant" style="ruby-position: under;">
        <rbc>
            <rb>馬</rb><rp>(</rp><rt>mǎ</rt><rp>)</rp>
            <rb>來</rb><rp>(</rp><rt>lái</rt><rp>)</rp>
            <rb>西</rb><rp>(</rp><rt>xī</rt><rp>)</rp>
            <rb>亞</rb><rp>(</rp><rt>yà</rt><rp>)</rp>
        </rbc>
        <rtc xml:lang="en" style="ruby-position: over;">
            <rp>(</rp><rt>Malaysia</rt><rp>)</rp>
        </rtc>
    </ruby>
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

## Examples

::: section-content
::: code-example
[html]{.language-name}

``` {signature="bECTCJitb2YbU8IZEgBWaPu7xFCVDN1M0iiPZ2bZy6Q=" data-language="html"}
<div class="info">
  <ruby>
    <rtc>
      <rb>旧</rb><rt>jiù</rt>
      <rb>金</rb><rt>jīn</rt>
      <rb>山</rb><rt>shān</rt>
    </rtc>
    <rtc>San Francisco</rtc>
  </ruby>

```
:::
:::

### Result

::: section-content
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
<td><a href="../content_categories#phrasing_content">Phrasing
content</a> or <a href="rt"><code>&lt;rt&gt;</code></a> elements.</td>
</tr>
<tr class="odd">
<th scope="row">Tag omission</th>
<td>The closing tag can be omitted if it is immediately followed by a <a
href="rb"><code>&lt;rb&gt;</code></a>, <a href="rtc"
aria-current="page"><code>&lt;rtc&gt;</code></a> or <a
href="rt"><code>&lt;rt&gt;</code></a> element opening tag or by its
parent closing tag.</td>
</tr>
<tr class="even">
<th scope="row">Permitted parents</th>
<td>A <a href="ruby"><code>&lt;ruby&gt;</code></a> element.</td>
</tr>
<tr class="odd">
<th scope="row">Permitted ARIA roles</th>
<td>Any</td>
</tr>
<tr class="even">
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
  -------------------------------------------------------------------------
  Specification
  -------------------------------------------------------------------------
  [HTML Standard\
  [\#
  rtc]{.small}](https://html.spec.whatwg.org/multipage/obsolete.html#rtc)

  -------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
          Desktop                                                         Mobile                                                                                   
  ------- --------- ------ --------- ------------------- ------- -------- ----------------- ---------------- --------------------- --------------- --------------- ------------------
          Chrome    Edge   Firefox   Internet Explorer   Opera   Safari   WebView Android   Chrome Android   Firefox for Android   Opera Android   Safari on IOS   Samsung Internet
  `rtc`   ≤80       80     33        No                  67      ≤13.1    80                80               33                    57              ≤13.4           13.0
:::

## See also {#see_also}

::: section-content
-   [`<ruby>`](ruby)
-   [`<rp>`](rp)
-   [`<rb>`](rb)
-   [`<rt>`](rt)
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Element/rtc](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/rtc){._attribution-link}
:::
