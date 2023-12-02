

# \<p\>: The Paragraph element



::: section-content
The `<p>` [HTML](../index) element represents a paragraph. Paragraphs
are usually represented in visual media as blocks of text separated from
adjacent blocks by blank lines and/or first-line indentation, but HTML
paragraphs can be any structural grouping of related content, such as
images or form fields.

Paragraphs are [block-level
elements](https://developer.mozilla.org/en-US/docs/Glossary/Block-level_content),
and notably will automatically close if another block-level element is
parsed before the closing `</p>` tag. See \"Tag omission\" below.
:::

## Try it {#try_it}

::: section-content
::: iframe
::: {.output-header .border-rounded-top}
#### HTML Demo: \<p\> {#html-demo-p .output-heading}

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
    <p>
      Geckos are a group of usually small, usually nocturnal lizards. They are found on every continent except Antarctica.
    </p>

    <p>Some species live in houses where they hunt insects attracted by artificial light.</p>
:::
:::

::: {#css-panel .section .hidden tabindex="0" role="tabpanel" aria-labelledby="css" aria-hidden="true"}
::: {#css-editor}
    p {
      margin: 10px 0;
      padding: 5px;
      border: 1px solid #999;
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

<figure class="table-container">
<div class="_table">
<table class="properties">
<tbody>
<tr class="odd">
<th scope="row"><a href="../content_categories">Content
categories</a></th>
<td><a href="../content_categories#flow_content">Flow content</a>,
palpable content.</td>
</tr>
<tr class="even">
<th scope="row">Permitted content</th>
<td><a href="../content_categories#phrasing_content">Phrasing
content</a>.</td>
</tr>
<tr class="odd">
<th scope="row">Tag omission</th>
<td>The start tag is required. The end tag may be omitted if the <a
href="p" aria-current="page"><code>&lt;p&gt;</code></a> element is
immediately followed by an <a
href="address"><code>&lt;address&gt;</code></a>, <a
href="article"><code>&lt;article&gt;</code></a>, <a
href="aside"><code>&lt;aside&gt;</code></a>, <a
href="blockquote"><code>&lt;blockquote&gt;</code></a>, <a
href="details"><code>&lt;details&gt;</code></a>, <a
href="div"><code>&lt;div&gt;</code></a>, <a
href="dl"><code>&lt;dl&gt;</code></a>, <a
href="fieldset"><code>&lt;fieldset&gt;</code></a>, <a
href="figcaption"><code>&lt;figcaption&gt;</code></a>, <a
href="figure"><code>&lt;figure&gt;</code></a>, <a
href="footer"><code>&lt;footer&gt;</code></a>, <a
href="form"><code>&lt;form&gt;</code></a>, <a
href="heading_elements">h1</a>, <a href="heading_elements">h2</a>, <a
href="heading_elements">h3</a>, <a href="heading_elements">h4</a>, <a
href="heading_elements">h5</a>, <a href="heading_elements">h6</a>, <a
href="header"><code>&lt;header&gt;</code></a>, <a
href="hgroup"><code>&lt;hgroup&gt;</code></a>, <a
href="hr"><code>&lt;hr&gt;</code></a>, <a
href="main"><code>&lt;main&gt;</code></a>, <a
href="menu"><code>&lt;menu&gt;</code></a>, <a
href="nav"><code>&lt;nav&gt;</code></a>, <a
href="ol"><code>&lt;ol&gt;</code></a>, <a
href="pre"><code>&lt;pre&gt;</code></a>, <a
href="search"><code>&lt;search&gt;</code></a>, <a
href="section"><code>&lt;section&gt;</code></a>, <a
href="table"><code>&lt;table&gt;</code></a>, <a
href="ul"><code>&lt;ul&gt;</code></a> or another <a href="p"
aria-current="page"><code>&lt;p&gt;</code></a> element, or if there is
no more content in the parent element and the parent element is not an
<a href="a"><code>&lt;a&gt;</code></a>, <a
href="audio"><code>&lt;audio&gt;</code></a>, <a
href="del"><code>&lt;del&gt;</code></a>, <a
href="ins"><code>&lt;ins&gt;</code></a>, <a
href="map"><code>&lt;map&gt;</code></a>, <a
href="noscript"><code>&lt;noscript&gt;</code></a> or <a
href="video"><code>&lt;video&gt;</code></a> element, or an autonomous
custom element.</td>
</tr>
<tr class="even">
<th scope="row">Permitted parents</th>
<td>Any element that accepts <a
href="../content_categories#flow_content">flow content</a>.</td>
</tr>
<tr class="odd">
<th scope="row">Implicit ARIA role</th>
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/structural_roles">paragraph</a></td>
</tr>
<tr class="even">
<th scope="row">Permitted ARIA roles</th>
<td>Any</td>
</tr>
<tr class="odd">
<th scope="row">DOM interface</th>
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLParagraphElement"><code>HTMLParagraphElement</code></a></td>
</tr>
</tbody>
</table>

</figure>
:::

## Attributes

::: section-content
This element only includes the [global
attributes](../global_attributes).

::: {#sect1 .notecard .note}
**Note:** The `align` attribute on `<p>` tags is obsolete and shouldn\'t
be used.
:::
:::

## Examples

### HTML

::: section-content
::: code-example
[html]{.language-name}

``` {signature="FbcvsC38VNKV5rvL7IZ3SMq4jAhh+BqGj/GGrTDVtDs=" data-language="html"}
<p>
  This is the first paragraph of text. This is the first paragraph of text. This
  is the first paragraph of text. This is the first paragraph of text.
</p>
<p>
  This is the second paragraph. This is the second paragraph. This is the second
  paragraph. This is the second paragraph.
</p>
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

## Styling paragraphs {#styling_paragraphs}

::: section-content
By default, browsers separate paragraphs with a single blank line.
Alternate separation methods, such as first-line indentation, can be
achieved with
[CSS](https://developer.mozilla.org/en-US/docs/Glossary/CSS):
:::

### HTML {#html_2}

::: section-content
::: code-example
[html]{.language-name}

``` {signature="ArLnQg2kOLl8KSZ5VpaS6wrUF8m9ge4XH+7RP3M8tfg=" data-language="html"}
<p>
  Separating paragraphs with blank lines is easiest for readers to scan, but
  they can also be separated by indenting their first lines. This is often used
  to take up less space, such as to save paper in print.
</p>

<p>
  Writing that is intended to be edited, such as school papers and rough drafts,
  uses both blank lines and indentation for separation. In finished works,
  combining both is considered redundant and amateurish.
</p>

<p>
  In very old writing, paragraphs were separated with a special character: ¶,
  the <i>pilcrow</i>. Nowadays, this is considered claustrophobic and hard to
  read.
</p>

<p>
  How hard to read? See for yourself:
  <button data-toggle-text="Oh no! Switch back!">
    Use pilcrow for paragraphs
  </button>
</p>
```
:::
:::

### CSS

::: section-content
::: code-example
[css]{.language-name}

``` {signature="vgpXjJe+JsfZeiUxmbRM7/M6B7zsSGiKQMxeZ+EhR/M=" data-language="css"}
p {
  margin: 0;
  text-indent: 3ch;
}

p.pilcrow {
  text-indent: 0;
  display: inline;
}
p.pilcrow + p.pilcrow::before {
  content: " ¶ ";
}
```
:::
:::

### JavaScript

::: section-content
::: code-example
[js]{.language-name}

``` {signature="SD7N47Qi2DXpOUk8UvzrGUIfE0FpStuKBw4sSYFJIAk=" data-language="js"}
document.querySelector("button").addEventListener("click", (event) => {
  document.querySelectorAll("p").forEach((paragraph) => {
    paragraph.classList.toggle("pilcrow");
  });

  [event.target.innerText, event.target.dataset.toggleText] = [
    event.target.dataset.toggleText,
    event.target.innerText,
  ];
});
```
:::
:::

### Result {#result_2}

::: section-content
::: {#sect3 .code-example}
::: iframe
:::
:::
:::

## Accessibility concerns {#accessibility_concerns}

::: section-content
Breaking up content into paragraphs helps make a page more accessible.
Screen-readers and other assistive technology provide shortcuts to let
their users skip to the next or previous paragraph, letting them skim
content like how white space lets visual users skip around.

Using empty `<p>` elements to add space between paragraphs is
problematic for people who navigate with screen-reading technology.
Screen readers may announce the paragraph\'s presence, but not any
content contained within it --- because there is none. This can confuse
and frustrate the person using the screen reader.

If extra space is desired, use
[CSS](https://developer.mozilla.org/en-US/docs/Glossary/CSS) properties
like [`margin`](https://developer.mozilla.org/en-US/docs/Web/CSS/margin)
to create the effect:

::: code-example
[css]{.language-name}

``` {signature="8IOLiGNqGIFy1pDARviiN2xl/VLbbo48fMURml9fhUk=" data-language="css"}
p {
  margin-bottom: 2em; /* increase white space after a paragraph */
}
```
:::
:::

## Specifications

::: _table
  -----------------------------------------------------------------------------------------------------
  Specification
  -----------------------------------------------------------------------------------------------------
  [HTML Standard\
  [\#
  the-p-element]{.small}](https://html.spec.whatwg.org/multipage/grouping-content.html#the-p-element)

  -----------------------------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
        Desktop                                                         Mobile                                                                                   
  ----- --------- ------ --------- ------------------- ------- -------- ----------------- ---------------- --------------------- --------------- --------------- ------------------
        Chrome    Edge   Firefox   Internet Explorer   Opera   Safari   WebView Android   Chrome Android   Firefox for Android   Opera Android   Safari on IOS   Samsung Internet
  `p`   1         12     1         Yes                 15      1        4.4               18               4                     14              1               1.0
:::

## See also {#see_also}

::: section-content
-   [`<hr>`](hr)
-   [`<br>`](br)
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Element/p](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/p){._attribution-link}
:::
