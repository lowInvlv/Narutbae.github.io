

# \<object\>: The External Object element



::: section-content
The `<object>` [HTML](../index) element represents an external resource,
which can be treated as an image, a nested browsing context, or a
resource to be handled by a plugin.
:::

## Try it {#try_it}

::: section-content
::: iframe
::: {.output-header .border-rounded-top}
#### HTML Demo: \<object\> {#html-demo-object .output-heading}

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
    <object type="application/pdf" data="/media/examples/In-CC0.pdf" width="250" height="200"></object>
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
:::

## Attributes

::: section-content
This element includes the [global attributes](../global_attributes).

[`archive`](#archive) [Deprecated]{.visually-hidden}

:   A space-separated list of URIs for archives of resources for the
    object.

[`border`](#border) [Deprecated]{.visually-hidden}

:   The width of a border around the control, in pixels.

[`classid`](#classid) [Deprecated]{.visually-hidden}

:   The URI of the object\'s implementation. It can be used together
    with, or in place of, the **data** attribute.

[`codebase`](#codebase) [Deprecated]{.visually-hidden}

:   The base path used to resolve relative URIs specified by
    **classid**, **data**, or **archive**. If not specified, the default
    is the base URI of the current document.

[`codetype`](#codetype) [Deprecated]{.visually-hidden}

:   The content type of the data specified by **classid**.

[`data`](#data)

:   The address of the resource as a valid URL. At least one of **data**
    and **type** must be defined.

[`declare`](#declare) [Deprecated]{.visually-hidden}

:   The presence of this Boolean attribute makes this element a
    declaration only. The object must be instantiated by a subsequent
    `<object>` element. Repeat the `<object>` element completely each
    time the resource is reused.

[`form`](#form)

:   The form element, if any, that the object element is associated with
    (its *form owner*). The value of the attribute must be an ID of a
    [`<form>`](form) element in the same document.

[`height`](#height)

:   The height of the displayed resource, in [CSS
    pixels](https://drafts.csswg.org/css-values/#px){target="_blank"}.
    --- (Absolute values only. [NO
    percentages](https://html.spec.whatwg.org/multipage/embedded-content.html#dimension-attributes){target="_blank"})

[`name`](#name)

:   The name of valid browsing context (HTML5), or the name of the
    control (HTML 4).

[`standby`](#standby) [Deprecated]{.visually-hidden}

:   A message that the browser can show while loading the object\'s
    implementation and data.

[`type`](#type)

:   The [content
    type](https://developer.mozilla.org/en-US/docs/Glossary/MIME_type)
    of the resource specified by **data**. At least one of **data** and
    **type** must be defined.

[`usemap`](#usemap)

:   A hash-name reference to a [`<map>`](map) element; that is a \'#\'
    followed by the value of a [`name`](map#name) of a map element.

[`width`](#width)

:   The width of the display resource, in [CSS
    pixels](https://drafts.csswg.org/css-values/#px){target="_blank"}.
    --- (Absolute values only. [NO
    percentages](https://html.spec.whatwg.org/multipage/embedded-content.html#dimension-attributes){target="_blank"})
:::

## Examples

### Embed a video {#embed_a_video}

::: section-content
#### HTML

::: code-example
[html]{.language-name}

``` {signature="u94sPWtd4wCI83rEScsFhbgO+s6tZ/Art1Ewe55cJZs=" data-language="html"}
<object
  type="video/mp4"
  data="https://interactive-examples.mdn.mozilla.net/media/cc0-videos/flower.webm"
  width="600"
  height="140">
  <img src="path/image.jpg" alt="useful image description" />
</object>
```
:::

#### Result

::: {#sect1 .code-example}
::: iframe
:::
:::

If the video in the example fails to load, the user will be provided
with an image as fallback content. The [`<img>`](img) tag is used to
display an image. We include the `src` attribute set to the path to the
image we want to embed. We also include the `alt` attribute, which
provides the image with an accessible name. If the image also fails to
load, the content of the `alt` attribute will be displayed.
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
<td><a href="../content_categories#flow_content">Flow content</a>; <a
href="../content_categories#phrasing_content">phrasing content</a>; <a
href="../content_categories#embedded_content">embedded content</a>,
palpable content; if the element has a <a href="object#usemap"
aria-current="page"><code>usemap</code></a> attribute, <a
href="../content_categories#interactive_content">interactive
content</a>; <a href="../content_categories#form_listed">listed</a>, <a
href="../content_categories#form_submittable">submittable</a> <a
href="../content_categories#form-associated_content">form-associated</a>
element.</td>
</tr>
<tr class="even">
<th scope="row">Permitted content</th>
<td>zero or more <a href="param"><code>&lt;param&gt;</code></a>
elements, then <a
href="../content_categories#transparent_content_model">transparent</a>.</td>
</tr>
<tr class="odd">
<th scope="row">Tag omission</th>
<td>None, both the starting and ending tag are mandatory.</td>
</tr>
<tr class="even">
<th scope="row">Permitted parents</th>
<td>Any element that accepts <a
href="../content_categories#embedded_content">embedded content</a>.</td>
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
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/img_role"><code>img</code></a></td>
</tr>
<tr class="odd">
<th scope="row">DOM interface</th>
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLObjectElement"><code>HTMLObjectElement</code></a></td>
</tr>
</tbody>
</table>

</figure>
:::

## Specifications

::: _table
  ------------------------------------------------------------------------------------------------------------------
  Specification
  ------------------------------------------------------------------------------------------------------------------
  [HTML Standard\
  [\#
  the-object-element]{.small}](https://html.spec.whatwg.org/multipage/iframe-embed-object.html#the-object-element)

  ------------------------------------------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
               Desktop                                                         Mobile                                                                                   
  ------------ --------- ------ --------- ------------------- ------- -------- ----------------- ---------------- --------------------- --------------- --------------- ------------------
               Chrome    Edge   Firefox   Internet Explorer   Opera   Safari   WebView Android   Chrome Android   Firefox for Android   Opera Android   Safari on IOS   Samsung Internet
  `object`     1         12     1         Yes                 15      3        4.4               18               4                     14              2               1.0
  `archive`    1         12     1         Yes                 15      3        4.4               18               4                     14              2               1.0
  `border`     1         12     1         Yes                 15      3        4.4               18               4                     14              2               1.0
  `classid`    Yes       12     1         Yes                 Yes     Yes      Yes               Yes              4                     Yes             Yes             Yes
  `codebase`   1         12     1         Yes                 15      3        4.4               18               4                     14              2               1.0
  `codetype`   1         12     1         Yes                 15      3        4.4               18               4                     14              2               1.0
  `data`       1         12     1         Yes                 15      3        4.4               18               4                     14              2               1.0
  `declare`    1         12     1         Yes                 15      3        4.4               18               4                     14              2               1.0
  `form`       1         12     1         Yes                 15      3        4.4               18               4                     14              2               1.0
  `height`     1         12     1         Yes                 15      3        4.4               18               4                     14              2               1.0
  `name`       1         12     1         Yes                 15      3        4.4               18               4                     14              2               1.0
  `standby`    1         12     1         Yes                 15      3        4.4               18               4                     14              2               1.0
  `tabindex`   1         12     1         Yes                 15      3.1      4.4               18               4                     14              2               1.0
  `type`       1         12     1         Yes                 15      3        4.4               18               4                     14              2               1.0
  `usemap`     1         12     1         Yes                 15      3        4.4               18               4                     14              2               1.0
  `width`      1         12     1         Yes                 15      3        4.4               18               4                     14              2               1.0
:::

## See also {#see_also}

::: section-content
-   [`<embed>`](embed)
-   [`<param>`](param)
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Element/object](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/object){._attribution-link}
:::
