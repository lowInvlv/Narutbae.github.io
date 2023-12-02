

# \<figure\>: The Figure with Optional Caption element



::: section-content
The `<figure>` [HTML](../index) element represents self-contained
content, potentially with an optional caption, which is specified using
the [`<figcaption>`](figcaption) element. The figure, its caption, and
its contents are referenced as a single unit.
:::

## Try it {#try_it}

::: section-content
::: iframe
::: {.output-header .border-rounded-top}
#### HTML Demo: \<figure\> {#html-demo-figure .output-heading}

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
    <figure>
      <img src="/media/cc0-images/elephant-660-480.jpg" alt="Elephant at sunset" />
      <figcaption>An elephant at sunset</figcaption>
    </figure>
:::
:::

::: {#css-panel .section .hidden tabindex="0" role="tabpanel" aria-labelledby="css" aria-hidden="true"}
::: {#css-editor}
    figure {
      border: thin #c0c0c0 solid;
      display: flex;
      flex-flow: column;
      padding: 5px;
      max-width: 220px;
      margin: auto;
    }

    img {
      max-width: 220px;
      max-height: 150px;
    }

    figcaption {
      background-color: #222;
      color: #fff;
      font: italic smaller sans-serif;
      padding: 3px;
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
:::

## Attributes

::: section-content
This element only includes the [global
attributes](../global_attributes).
:::

## Usage notes {#usage_notes}

::: section-content
-   Usually a `<figure>` is an image, illustration, diagram, code
    snippet, etc., that is referenced in the main flow of a document,
    but that can be moved to another part of the document or to an
    appendix without affecting the main flow.
-   A caption can be associated with the `<figure>` element by inserting
    a [`<figcaption>`](figcaption) inside it (as the first or the last
    child). The first `<figcaption>` element found in the figure is
    presented as the figure\'s caption.
:::

## Examples

### Images

::: section-content
::: code-example
[html]{.language-name}

``` {signature="o1q/E3REDLw306plzB83vO6ZWS5fNRZlDiVu0dSH0g8=" data-language="html"}
<!-- Just an image -->
<figure>
  <img src="favicon-192x192.png" alt="The beautiful MDN logo." />
</figure>

<!-- Image with a caption -->
<figure>
  <img src="favicon-192x192.png" alt="The beautiful MDN logo." />
  <figcaption>MDN Logo</figcaption>
</figure>
```
:::

#### Result

::: {#sect1 .code-example}
::: iframe
:::
:::
:::

### Code snippets {#code_snippets}

::: section-content
::: code-example
[html]{.language-name}

``` {signature="GDuA+a9AAyewocWxcj/sTXAFDnZQfnLnE9FHsWLAjQI=" data-language="html"}
<figure>
  <figcaption>Get browser details using <code>navigator</code>.</figcaption>
  <pre>
function NavigatorExample() {
  var txt;
  txt = "Browser CodeName: " + navigator.appCodeName + "; ";
  txt+= "Browser Name: " + navigator.appName + "; ";
  txt+= "Browser Version: " + navigator.appVersion  + "; ";
  txt+= "Cookies Enabled: " + navigator.cookieEnabled  + "; ";
  txt+= "Platform: " + navigator.platform  + "; ";
  txt+= "User-agent header: " + navigator.userAgent  + "; ";
  console.log("NavigatorExample", txt);
}
  </pre>
</figure>
```
:::

#### Result {#result_2}

::: {#sect2 .code-example}
::: iframe
:::
:::
:::

### Quotations

::: section-content
::: code-example
[html]{.language-name}

``` {signature="OZ8Q0s04Ec8i2OJkcJBQ76Rwn77YWkYDvhFMv+3C+p8=" data-language="html"}
<figure>
  <figcaption><b>Edsger Dijkstra:</b></figcaption>
  <blockquote>
    If debugging is the process of removing software bugs, then programming must
    be the process of putting them in.
  </blockquote>
</figure>
```
:::

#### Result {#result_3}

::: {#sect3 .code-example}
::: iframe
:::
:::
:::

### Poems

::: section-content
::: code-example
[html]{.language-name}

``` {signature="uZnRPtdU8Eyp3yfKjlVSlx26f8+8+F+pKKTtqrR+blk=" data-language="html"}
<figure>
  <p style="white-space:pre">
    Bid me discourse, I will enchant thine ear, Or like a fairy trip upon the
    green, Or, like a nymph, with long dishevelled hair, Dance on the sands, and
    yet no footing seen: Love is a spirit all compact of fire, Not gross to
    sink, but light, and will aspire.
  </p>
  <figcaption><cite>Venus and Adonis</cite>, by William Shakespeare</figcaption>
</figure>
```
:::

#### Result {#result_4}

::: {#sect4 .code-example}
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
href="../content_categories#palpable_content">palpable content</a>.</td>
</tr>
<tr class="even">
<th scope="row">Permitted content</th>
<td>A <a href="figcaption"><code>&lt;figcaption&gt;</code></a> element,
followed by <a href="../content_categories#flow_content">flow
content</a>; or flow content followed by a <a
href="figcaption"><code>&lt;figcaption&gt;</code></a> element; or flow
content.</td>
</tr>
<tr class="odd">
<th scope="row">Tag omission</th>
<td>None, both the starting and ending tag are mandatory.</td>
</tr>
<tr class="even">
<th scope="row">Permitted parents</th>
<td>Any element that accepts <a
href="../content_categories#flow_content">Flow content</a>.</td>
</tr>
<tr class="odd">
<th scope="row">Implicit ARIA role</th>
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/figure_role">figure</a></td>
</tr>
<tr class="even">
<th scope="row">Permitted ARIA roles</th>
<td>With no <a href="figcaption">figcaption</a> descendant: <a
href="https://www.w3.org/TR/html-aria/#dfn-any-role"
target="_blank">any</a>, otherwise no permitted roles</td>
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
  ---------------------------------------------------------------------------------------------------------------
  Specification
  ---------------------------------------------------------------------------------------------------------------
  [HTML Standard\
  [\#
  the-figure-element]{.small}](https://html.spec.whatwg.org/multipage/grouping-content.html#the-figure-element)

  ---------------------------------------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
             Desktop                                                         Mobile                                                                                   
  ---------- --------- ------ --------- ------------------- ------- -------- ----------------- ---------------- --------------------- --------------- --------------- ------------------
             Chrome    Edge   Firefox   Internet Explorer   Opera   Safari   WebView Android   Chrome Android   Firefox for Android   Opera Android   Safari on IOS   Samsung Internet
  `figure`   8         12     4         9                   11      5.1      4.4               18               4                     11              5               1.0
:::

## See also {#see_also}

::: section-content
-   The [`<figcaption>`](figcaption) element.
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Element/figure](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/figure){._attribution-link}
:::
