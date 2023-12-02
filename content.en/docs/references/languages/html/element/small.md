

# \<small\>: the side comment element



::: section-content
The `<small>` [HTML](../index) element represents side-comments and
small print, like copyright and legal text, independent of its styled
presentation. By default, it renders text within it one font-size
smaller, such as from `small` to `x-small`.
:::

## Try it {#try_it}

::: section-content
::: iframe
::: {.output-header .border-rounded-top}
#### HTML Demo: \<small\> {#html-demo-small .output-heading}

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
    <p>MDN Web Docs is a learning platform for Web technologies and the software that powers the Web.</p>

    <hr />

    <p><small>The content is licensed under a Creative Commons Attribution-ShareAlike 2.5 Generic License.</small></p>
:::
:::

::: {#css-panel .section .hidden tabindex="0" role="tabpanel" aria-labelledby="css" aria-hidden="true"}
::: {#css-editor}
    small {
      font-size: 0.7em;
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

### Basic usage {#basic_usage}

::: section-content
::: code-example
[html]{.language-name}

``` {signature="iXr7PDWDfNhmV0Hp6My9qslH8oO7OVoxwrGtmNEpwzo=" data-language="html"}
<p>
  This is the first sentence.
  <small>This whole sentence is in small letters.</small>
</p>
```
:::

#### Result

::: {#sect1 .code-example}
::: iframe
:::
:::
:::

### CSS alternative {#css_alternative}

::: section-content
::: code-example
[html]{.language-name}

``` {signature="zE0JR03IWtHqK6K5ed8w9QjPWNxJMVHla1OYmIKZxAM=" data-language="html"}
<p>
  This is the first sentence.
  <span style="font-size:0.8em">This whole sentence is in small letters.</span>
</p>
```
:::

#### Result {#result_2}

::: {#sect2 .code-example}
::: iframe
:::
:::
:::

## Notes

::: section-content
Although the `<small>` element, like the [`<b>`](b) and [`<i>`](i)
elements, may be perceived to violate the principle of separation
between structure and presentation, all three are valid in HTML. Authors
are encouraged to use their best judgement when determining whether to
use `<small>` or CSS.
:::

## Technical summary {#technical_summary}

::: section-content
<figure class="table-container">
<div class="_table">
<table class="properties">
<tbody>
<tr class="odd">
<th scope="row">Content categories</th>
<td><a href="../content_categories#flow_content">Flow content</a>, <a
href="../content_categories#phrasing_content">phrasing content</a></td>
</tr>
<tr class="even">
<th scope="row">Permitted content</th>
<td><a href="../content_categories#phrasing_content">Phrasing
content</a></td>
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
  -----------------------------------------------------------------------------------------------------------------
  Specification
  -----------------------------------------------------------------------------------------------------------------
  [HTML Standard\
  [\#
  the-small-element]{.small}](https://html.spec.whatwg.org/multipage/text-level-semantics.html#the-small-element)

  -----------------------------------------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
            Desktop                                                         Mobile                                                                                   
  --------- --------- ------ --------- ------------------- ------- -------- ----------------- ---------------- --------------------- --------------- --------------- ------------------
            Chrome    Edge   Firefox   Internet Explorer   Opera   Safari   WebView Android   Chrome Android   Firefox for Android   Opera Android   Safari on IOS   Samsung Internet
  `small`   1         12     1         Yes                 15      ≤4       4.4               18               4                     14              ≤3.2            1.0
:::

## See also {#see_also}

::: section-content
-   [`<b>`](b)
-   [`<sub>`](sub) and [`<sup>`](sup)
-   [`<font>`](font)
-   [`<style>`](style)
-   HTML 4.01 Specification: [Font
    Styles](https://www.w3.org/TR/html4/present/graphics.html#h-15.2){target="_blank"}
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Element/small](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/small){._attribution-link}
:::
