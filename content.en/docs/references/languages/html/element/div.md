

# \<div\>: The Content Division element



::: section-content
The `` [HTML](../index) element is the generic container for flow
content. It has no effect on the content or layout until styled in some
way using [CSS](https://developer.mozilla.org/en-US/docs/Glossary/CSS)
(e.g. styling is directly applied to it, or some kind of layout model
like
[Flexbox](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_flexible_box_layout)
is applied to its parent element).
:::

## Try it {#try_it}

::: section-content
::: iframe
::: {.output-header .border-rounded-top}
#### HTML Demo: \<div\> {#html-demo-div .output-heading}

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
    <div class="warning">
      <img src="/media/examples/leopard.jpg" alt="An intimidating leopard." />
      <p>Beware of the leopard</p>
    
:::
:::

::: {#css-panel .section .hidden tabindex="0" role="tabpanel" aria-labelledby="css" aria-hidden="true"}
::: {#css-editor}
    .warning {
      border: 10px ridge #f00;
      background-color: #ff0;
      padding: 0.5rem;
      display: flex;
      flex-direction: column;
    }

    .warning img {
      width: 100%;
    }

    .warning p {
      font: small-caps bold 1.2rem sans-serif;
      text-align: center;
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

As a \"pure\" container, the `` element does not inherently
represent anything. Instead, it\'s used to group content so it can be
easily styled using the [`class`](../global_attributes#class) or
[`id`](../global_attributes#id) attributes, marking a section of a
document as being written in a different language (using the
[`lang`](../global_attributes#lang) attribute), and so on.
:::

## Attributes

::: section-content
This element includes the [global attributes](../global_attributes).

::: {#sect1 .notecard .note}
**Note:** The `align` attribute is obsolete; do not use it anymore.
Instead, you should use CSS properties or techniques such as [CSS
Grid](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_grid_layout)
or [CSS
Flexbox](https://developer.mozilla.org/en-US/docs/Learn/CSS/CSS_layout/Flexbox)
to align and position `` elements on the page.
:::
:::

## Usage notes {#usage_notes}

::: section-content
-   The `` element should be used only when no other semantic
    element (such as [`<article>`](article) or [`<nav>`](nav)) is
    appropriate.
:::

## Accessibility concerns {#accessibility_concerns}

::: section-content
The `` element has [an implicit role of
`generic`](https://www.w3.org/TR/wai-aria-1.2/#generic){target="_blank"},
and not none. This may affect certain ARIA combination declarations that
expect a direct descendant element with a certain role to function
properly.
:::

## Examples

### A simple example {#a_simple_example}

::: section-content
::: code-example
[html]{.language-name}

``` {signature="36M3KELsnVnPdTx5sHKAJZGV93N/hy5EaNxr0KbJNYE=" data-language="html"}

  <p>
    Any kind of content here. Such as &lt;p&gt;, &lt;table&gt;. You name it!
  </p>

```
:::

#### Result

::: {#sect2 .code-example}
::: iframe
:::
:::
:::

### A styled example {#a_styled_example}

::: section-content
This example creates a shadowed box by applying a style to the ``
using CSS. Note the use of the [`class`](../global_attributes#class)
attribute on the `` to apply the style named `"shadowbox"` to the
element.

#### HTML

::: code-example
[html]{.language-name}

``` {signature="8Atj2IB2DUFT3/Uh5/nswsCjCj65JEBrczk84bXOqFo=" data-language="html"}
<div class="shadowbox">
  <p>Here's a very interesting note displayed in a lovely shadowed box.</p>

```
:::

#### CSS

::: code-example
[css]{.language-name}

``` {signature="Bm0kShsX2T/fBmMElg2SlJqAm6aGZr/xPRuHaFLt/u4=" data-language="css"}
.shadowbox {
  width: 15em;
  border: 1px solid #333;
  box-shadow: 8px 8px 5px #444;
  padding: 8px 12px;
  background-image: linear-gradient(180deg, #fff, #ddd 40%, #ccc);
}
```
:::

#### Result {#result_2}

::: {#sect3 .code-example}
::: iframe
:::
:::
:::

## Technical summary {#technical_summary}

::: section-content
<figure class="table-container">
<div class="_table">
<table class="properties">
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<th scope="row"><a href="../content_categories">Content
categories</a></th>
<td><a href="../content_categories#flow_content">Flow content</a>, <a
href="../content_categories#palpable_content">palpable content</a>.</td>
</tr>
<tr class="even">
<th scope="row">Permitted content</th>
<td><a href="../content_categories#flow_content">Flow content</a>.<br />
Or (in <a
href="https://developer.mozilla.org/en-US/docs/Glossary/WHATWG">WHATWG</a>
HTML): If the parent is a <a href="dl"><code>&lt;dl&gt;</code></a>
element: one or more <a href="dt"><code>&lt;dt&gt;</code></a> elements
followed by one or more <a href="dd"><code>&lt;dd&gt;</code></a>
elements, optionally intermixed with <a
href="script"><code>&lt;script&gt;</code></a> and <a
href="template"><code>&lt;template&gt;</code></a> elements.</td>
</tr>
<tr class="odd">
<th scope="row">Tag omission</th>
<td>None, both the starting and ending tag are mandatory.</td>
</tr>
<tr class="even">
<th scope="row">Permitted parents</th>
<td>Any element that accepts <a
href="../content_categories#flow_content">flow content</a>.<br />
Or (in <a
href="https://developer.mozilla.org/en-US/docs/Glossary/WHATWG">WHATWG</a>
HTML): <a href="dl"><code>&lt;dl&gt;</code></a> element.</td>
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
href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLDivElement"><code>HTMLDivElement</code></a></td>
</tr>
</tbody>
</table>

</figure>
:::

## Specifications

::: _table
  ---------------------------------------------------------------------------------------------------------
  Specification
  ---------------------------------------------------------------------------------------------------------
  [HTML Standard\
  [\#
  the-div-element]{.small}](https://html.spec.whatwg.org/multipage/grouping-content.html#the-div-element)

  ---------------------------------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
            Desktop                                                         Mobile                                                                                   
  --------- --------- ------ --------- ------------------- ------- -------- ----------------- ---------------- --------------------- --------------- --------------- ------------------
            Chrome    Edge   Firefox   Internet Explorer   Opera   Safari   WebView Android   Chrome Android   Firefox for Android   Opera Android   Safari on IOS   Samsung Internet
  `div`     1         12     1         Yes                 15      1        4.4               18               4                     14              1               1.0
  `align`   1         12     1         Yes                 15      3        4.4               18               4                     14              2               1.0
:::

## See also {#see_also}

::: section-content
-   Semantic sectioning elements: [`<section>`](section),
    [`<article>`](article), [`<nav>`](nav), [`<header>`](header),
    [`<footer>`](footer)
-   [`<span>`](span) element for styling of phrasing content
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Element/div](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/div){._attribution-link}
:::
