

# \<embed\>: The Embed External Content element



::: section-content
The `<embed>` [HTML](../index) element embeds external content at the
specified point in the document. This content is provided by an external
application or other source of interactive content such as a browser
plug-in.
:::

## Try it {#try_it}

::: section-content
::: iframe
::: {.output-header .border-rounded-top}
#### HTML Demo: \<embed\> {#html-demo-embed .output-heading}

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
    <embed type="video/webm" src="/media/cc0-videos/flower.mp4" width="250" height="200" />
:::
:::

::: {#css-panel .section .hidden tabindex="0" role="tabpanel" aria-labelledby="css" aria-hidden="true"}
::: {#css-editor}
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

::: {#sect1 .notecard .note}
**Note:** This topic documents only the element that is defined as part
of the [HTML Living
Standard](https://html.spec.whatwg.org/multipage/iframe-embed-object.html#the-embed-element){target="_blank"}.
It does not address earlier, non-standardized implementation of the
element.
:::

Keep in mind that most modern browsers have deprecated and removed
support for browser plug-ins, so relying upon `<embed>` is generally not
wise if you want your site to be operable on the average user\'s
browser.
:::

## Attributes

::: section-content
This element\'s attributes include the [global
attributes](../global_attributes).

[`height`](#height)

:   The displayed height of the resource, in [CSS
    pixels](https://drafts.csswg.org/css-values/#px){target="_blank"}.
    This must be an absolute value; percentages are *not* allowed.

[`src`](#src)

:   The URL of the resource being embedded.

[`type`](#type)

:   The [MIME
    type](https://developer.mozilla.org/en-US/docs/Glossary/MIME_type)
    to use to select the plug-in to instantiate.

[`width`](#width)

:   The displayed width of the resource, in [CSS
    pixels](https://drafts.csswg.org/css-values/#px){target="_blank"}.
    This must be an absolute value; percentages are *not* allowed.
:::

## Usage notes {#usage_notes}

::: section-content
You can use the
[`object-position`](https://developer.mozilla.org/en-US/docs/Web/CSS/object-position)
property to adjust the positioning of the embedded object within the
element\'s frame, and the
[`object-fit`](https://developer.mozilla.org/en-US/docs/Web/CSS/object-fit)
property to control how the object\'s size is adjusted to fit within the
frame.
:::

## Examples

::: section-content
::: code-example
[html]{.language-name}

``` {signature="tYYdqDwXFd6cdGnvO0Hh6rTFsyzUtoUyVX2rrRCgMGQ=" data-language="html"}
<embed
  type="video/quicktime"
  src="movie.mov"
  width="640"
  height="480"
  title="Title of my video" />
```
:::
:::

## Accessibility concerns {#accessibility_concerns}

::: section-content
Use the [`title` attribute](../global_attributes/title) on an `embed`
element to label its content so that people navigating with assistive
technology such as a screen reader can understand what it contains. The
title\'s value should concisely describe the embedded content. Without a
title, they may not be able to determine what its embedded content is.
This context shift can be confusing and time-consuming, especially if
the `embed` element contains interactive content like video or audio.
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
href="../content_categories#phrasing_content">phrasing content</a>,
embedded content, interactive content, <a
href="../content_categories#palpable_content">palpable content</a>.</td>
</tr>
<tr class="even">
<th scope="row">Permitted content</th>
<td>None; it is a <a
href="https://developer.mozilla.org/en-US/docs/Glossary/Void_element">void
element</a>.</td>
</tr>
<tr class="odd">
<th scope="row">Tag omission</th>
<td>Must have a start tag, and must not have an end tag.</td>
</tr>
<tr class="even">
<th scope="row">Permitted parents</th>
<td>Any element that accepts embedded content.</td>
</tr>
<tr class="odd">
<th scope="row">Implicit ARIA role</th>
<td><a href="https://www.w3.org/TR/html-aria/#dfn-no-corresponding-role"
target="_blank">No corresponding role</a></td>
</tr>
<tr class="even">
<th scope="row">Permitted ARIA roles</th>
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/application_role"><code>application</code></a>,
<a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/document_role"><code>document</code></a>,
<a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/img_role"><code>img</code></a>,
<a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/none_role"><code>none</code></a>,
<a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/presentation_role"><code>presentation</code></a></td>
</tr>
<tr class="odd">
<th scope="row">DOM interface</th>
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLEmbedElement"><code>HTMLEmbedElement</code></a></td>
</tr>
</tbody>
</table>

</figure>
:::

## Specifications

::: _table
  ----------------------------------------------------------------------------------------------------------------
  Specification
  ----------------------------------------------------------------------------------------------------------------
  [HTML Standard\
  [\#
  the-embed-element]{.small}](https://html.spec.whatwg.org/multipage/iframe-embed-object.html#the-embed-element)

  ----------------------------------------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
             Desktop                                                         Mobile                                                                                   
  ---------- --------- ------ --------- ------------------- ------- -------- ----------------- ---------------- --------------------- --------------- --------------- ------------------
             Chrome    Edge   Firefox   Internet Explorer   Opera   Safari   WebView Android   Chrome Android   Firefox for Android   Opera Android   Safari on IOS   Samsung Internet
  `embed`    1         12     1         Yes                 ≤12.1   ≤4       4.4               18               4                     ≤12.1           ≤3.2            1.0
  `align`    1         79     1         No                  ≤12.1   ≤4       4.4               18               4                     ≤12.1           ≤3.2            1.0
  `height`   1         12     1         ≤6                  ≤12.1   ≤4       4.4               18               4                     ≤12.1           ≤3.2            1.0
  `name`     1         12     1         ≤6                  ≤12.1   ≤4       4.4               18               4                     ≤12.1           ≤3.2            1.0
  `src`      1         12     1         ≤6                  ≤12.1   ≤4       4.4               18               4                     ≤12.1           ≤3.2            1.0
  `type`     1         79     1         No                  ≤12.1   ≤4       4.4               18               4                     ≤12.1           ≤3.2            1.0
  `width`    1         12     1         ≤6                  ≤12.1   ≤4       4.4               18               4                     ≤12.1           ≤3.2            1.0
:::

## See also {#see_also}

::: section-content
-   Other elements that are used for embedding content of various types
    include [`<audio>`](audio), [`<canvas>`](canvas),
    [`<iframe>`](iframe), [`<img>`](img),
    [`<math>`](https://developer.mozilla.org/en-US/docs/Web/MathML/Element/math),
    [`<object>`](object),
    [`<svg>`](https://developer.mozilla.org/en-US/docs/Web/SVG/Element/svg),
    and [`<video>`](video).
-   Positioning and sizing the embedded content within its frame:
    [`object-position`](https://developer.mozilla.org/en-US/docs/Web/CSS/object-position)
    and
    [`object-fit`](https://developer.mozilla.org/en-US/docs/Web/CSS/object-fit)
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Element/embed](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/embed){._attribution-link}
:::
