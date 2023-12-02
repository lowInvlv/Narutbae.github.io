

# \<hgroup\>



::: section-content
The `<hgroup>` [HTML](../index) element represents a heading and related
content. It groups a single [`<h1>–<h6>`](heading_elements) element with
one or more [`<p>`](p).
:::

## Try it {#try_it}

::: section-content
::: iframe
::: {.output-header .border-rounded-top}
#### HTML Demo: \<hgroup\> {#html-demo-hgroup .output-heading}

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
    <hgroup>
      <h1>Frankenstein</h1>
      <p>Or: The Modern Prometheus</p>
    </hgroup>
    <p>
      Victor Frankenstein, a Swiss scientist, has a great ambition: to create intelligent life. But when his creature first
      stirs, he realizes he has made a monster. A monster which, abandoned by his master and shunned by everyone who sees
      it, follows Dr Frankenstein to the very ends of the earth.
    </p>
:::
:::

::: {#css-panel .section .hidden tabindex="0" role="tabpanel" aria-labelledby="css" aria-hidden="true"}
::: {#css-editor}
    hgroup {
      text-align: right;
      padding-right: 16px;
      border-right: 10px solid #00c8d7;
    }

    hgroup h1 {
      margin-bottom: 0;
    }

    hgroup p {
      margin: 0;
      font-weight: bold;
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
The `<hgroup>` element allows the grouping of a heading with any
secondary content, such as subheadings, an alternative title, or
tagline. Each of these types of content represented as a `<p>` element
within the `<hgroup>`.

The `<hgroup>` itself has no impact on the document outline of a web
page. Rather, the single allowed heading within the `<hgroup>`
contributes to the document outline.
:::

## Examples

::: section-content
::: code-example
[html]{.language-name}

``` {signature="TbnItoQSXiOZuaG6zdirz0/BUHupCTlfYnzgr+hRcsU=" data-language="html"}
<!doctype html>
<title>HTML Standard</title>
<body>
  <hgroup id="document-title">
    <h1>HTML: Living Standard</h1>
    <p>Last Updated 12 July 2022</p>
  </hgroup>
  <p>Some intro to the document.</p>
  <h2>Table of contents</h2>
  <ol id="toc">
    …
  </ol>
  <h2>First section</h2>
  <p>Some intro to the first section.</p>
</body>
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

## Accessibility concerns {#accessibility_concerns}

::: section-content
The `<hgroup>` presently has no strong accessibility semantics. The
content of the element (a heading and optional paragraphs) is what is
exposed by browser accessibility APIs.
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
heading content, palpable content.</td>
</tr>
<tr class="even">
<th scope="row">Permitted content</th>
<td>Zero or more <a href="p"><code>&lt;p&gt;</code></a> elements,
followed by one <a href="heading_elements">h1</a>, <a
href="heading_elements">h2</a>, <a href="heading_elements">h3</a>, <a
href="heading_elements">h4</a>, <a href="heading_elements">h5</a>, or <a
href="heading_elements">h6</a> element, followed by zero or more <a
href="p"><code>&lt;p&gt;</code></a> elements.</td>
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
  -------------------------------------------------------------------------------------------------------
  Specification
  -------------------------------------------------------------------------------------------------------
  [HTML Standard\
  [\#
  the-hgroup-element]{.small}](https://html.spec.whatwg.org/multipage/sections.html#the-hgroup-element)

  -------------------------------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
             Desktop                                                         Mobile                                                                                   
  ---------- --------- ------ --------- ------------------- ------- -------- ----------------- ---------------- --------------------- --------------- --------------- ------------------
             Chrome    Edge   Firefox   Internet Explorer   Opera   Safari   WebView Android   Chrome Android   Firefox for Android   Opera Android   Safari on IOS   Samsung Internet
  `hgroup`   5         12     4         9                   11.1    5        2.2               18               4                     11.1            4.2             1.0
:::

## See also {#see_also}

::: section-content
-   Others section-related elements: [`<body>`](body),
    [`<article>`](article), [`<section>`](section), [`<aside>`](aside),
    [h1](heading_elements), [h2](heading_elements),
    [h3](heading_elements), [h4](heading_elements),
    [h5](heading_elements), [h6](heading_elements), [`<nav>`](nav),
    [`<header>`](header), [`<footer>`](footer), [`<address>`](address);
-   [Sections and outlines of an HTML document](heading_elements).
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Element/hgroup](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/hgroup){._attribution-link}
:::
