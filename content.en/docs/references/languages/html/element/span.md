

# \<span\>: The Content Span element



::: section-content
The `<span>` [HTML](../index) element is a generic inline container for
phrasing content, which does not inherently represent anything. It can
be used to group elements for styling purposes (using the
[`class`](../global_attributes#class) or [`id`](../global_attributes#id)
attributes), or because they share attribute values, such as
[`lang`](../global_attributes#lang). It should be used only when no
other semantic element is appropriate. `<span>` is very much like a
[``](div) element, but [``](div) is a [block-level
element](https://developer.mozilla.org/en-US/docs/Glossary/Block-level_content)
whereas a `<span>` is an [inline-level
element](https://developer.mozilla.org/en-US/docs/Glossary/Inline-level_content).
:::

## Try it {#try_it}

::: section-content
::: iframe
::: {.output-header .border-rounded-top}
#### HTML Demo: \<span\> {#html-demo-span .output-heading}

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
      Add the <span class="ingredient">basil</span>, <span class="ingredient">pine nuts</span> and
      <span class="ingredient">garlic</span> to a blender and blend into a paste.
    </p>

    <p>Gradually add the <span class="ingredient">olive oil</span> while running the blender slowly.</p>
:::
:::

::: {#css-panel .section .hidden tabindex="0" role="tabpanel" aria-labelledby="css" aria-hidden="true"}
::: {#css-editor}
    span.ingredient {
      color: #f00;
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

## Example

### Example 1 {#example_1}

::: section-content
#### HTML

::: code-example
[html]{.language-name}

``` {signature="/1LifhEX+VZAZChGdanvRaMz9IOFdGLznGSZgB7uqcQ=" data-language="html"}
<p><span>Some text</span></p>
```
:::

#### Result

::: {#sect1 .code-example}
::: iframe
:::
:::
:::

### Example 2 {#example_2}

::: section-content
#### HTML {#html_2}

::: code-example
[html]{.language-name}

``` {signature="TJk3cIEcJaKZMyjoC3Vr9HJa3XPVT86AqoXZzXKe8MU=" data-language="html"}
<li>
  <span>
    <a href="portfolio.html" target="_blank">See my portfolio</a>
  </span>
</li>
```
:::

#### CSS

::: code-example
[css]{.language-name}

``` {signature="CZUYCNVTUsHBcMNtifZGz3xxQNKn5otdoJ7UlA9rzuw=" data-language="css"}
li span {
  background: gold;
}
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
href="../content_categories#phrasing_content">phrasing content</a>.</td>
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
href="../content_categories#phrasing_content">phrasing content</a>, or
any element that accepts <a
href="../content_categories#flow_content">flow content</a>.</td>
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
href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLSpanElement"><code>HTMLSpanElement</code></a></td>
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
  the-span-element]{.small}](https://html.spec.whatwg.org/multipage/text-level-semantics.html#the-span-element)

  ---------------------------------------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
           Desktop                                                         Mobile                                                                                   
  -------- --------- ------ --------- ------------------- ------- -------- ----------------- ---------------- --------------------- --------------- --------------- ------------------
           Chrome    Edge   Firefox   Internet Explorer   Opera   Safari   WebView Android   Chrome Android   Firefox for Android   Opera Android   Safari on IOS   Samsung Internet
  `span`   1         12     1         Yes                 15      1        4.4               18               4                     14              1               1.0
:::

## See also {#see_also}

::: section-content
-   HTML [``](div) element
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Element/span](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/span){._attribution-link}
:::
