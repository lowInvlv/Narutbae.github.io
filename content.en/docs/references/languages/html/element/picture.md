

# \<picture\>: The Picture element



::: section-content
The `<picture>` [HTML](../index) element contains zero or more
[`<source>`](source) elements and one [`<img>`](img) element to offer
alternative versions of an image for different display/device scenarios.

The browser will consider each child `<source>` element and choose the
best match among them. If no matches are found---or the browser doesn\'t
support the `<picture>` element---the URL of the `<img>` element\'s
[`src`](img#src) attribute is selected. The selected image is then
presented in the space occupied by the `<img>` element.
:::

## Try it {#try_it}

::: section-content
::: iframe
::: {.output-header .border-rounded-top}
#### HTML Demo: \<picture\> {#html-demo-picture .output-heading}

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
    <!--Change the browser window width to see the image change.-->

    <picture>
      <source srcset="/media/cc0-images/surfer-240-200.jpg" media="(orientation: portrait)" />
      <img src="/media/cc0-images/painted-hand-298-332.jpg" alt="" />
    </picture>
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

To decide which URL to load, the [user
agent](https://developer.mozilla.org/en-US/docs/Glossary/User_agent)
examines each `<source>`\'s [`srcset`](source#srcset),
[`media`](source#media), and [`type`](source#type) attributes to select
a compatible image that best matches the current layout and capabilities
of the display device.

The `<img>` element serves two purposes:

1.  It describes the size and other attributes of the image and its
    presentation.
2.  It provides a fallback in case none of the offered `<source>`
    elements are able to provide a usable image.

Common use cases for `<picture>`:

-   **Art direction.** Cropping or modifying images for different
    `media` conditions (for example, loading a simpler version of an
    image which has too many details, on smaller displays).
-   **Offering alternative image formats**, for cases where certain
    formats are not supported.

    ::: {#sect1 .notecard .note}
    **Note:** For example, newer formats like
    [AVIF](https://developer.mozilla.org/en-US/docs/Web/Media/Formats/Image_types#avif_image)
    or
    [WEBP](https://developer.mozilla.org/en-US/docs/Web/Media/Formats/Image_types#webp_image)
    have many advantages, but might not be supported by the browser. A
    list of supported image formats can be found in: [Image file type
    and format
    guide](https://developer.mozilla.org/en-US/docs/Web/Media/Formats/Image_types).
    :::
-   **Saving bandwidth and speeding page load times** by loading the
    most appropriate image for the viewer\'s display.

If providing higher-density versions of an image for high-DPI (Retina)
display, use [`srcset`](img#srcset) on the `<img>` element instead. This
lets browsers opt for lower-density versions in data-saving modes, and
you don\'t have to write explicit `media` conditions.

<figure class="table-container">
<div class="_table">
<table class="properties">
<tbody>
<tr class="odd">
<th scope="row"><a href="../content_categories">Content
categories</a></th>
<td><a href="../content_categories#flow_content">Flow content</a>,
phrasing content, embedded content</td>
</tr>
<tr class="even">
<th scope="row">Permitted content</th>
<td>Zero or more <a href="source"><code>&lt;source&gt;</code></a>
elements, followed by one <a href="img"><code>&lt;img&gt;</code></a>
element, optionally intermixed with script-supporting elements.</td>
</tr>
<tr class="odd">
<th scope="row">Tag omission</th>
<td>None, both the starting and ending tag are mandatory.</td>
</tr>
<tr class="even">
<th scope="row">Permitted parents</th>
<td>Any element that allows embedded content.</td>
</tr>
<tr class="odd">
<th scope="row">Implicit ARIA role</th>
<td><a href="https://www.w3.org/TR/html-aria/#dfn-no-corresponding-role"
target="_blank">No corresponding role</a></td>
</tr>
<tr class="even">
<th scope="row">Permitted ARIA roles</th>
<td>No <code>role</code> permitted</td>
</tr>
<tr class="odd">
<th scope="row">DOM interface</th>
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLPictureElement"><code>HTMLPictureElement</code></a></td>
</tr>
</tbody>
</table>

</figure>
:::

## Attributes

::: section-content
This element includes only [global attributes](../global_attributes).
:::

## Usage notes {#usage_notes}

::: section-content
You can use the
[`object-position`](https://developer.mozilla.org/en-US/docs/Web/CSS/object-position)
property to adjust the positioning of the image within the element\'s
frame, and the
[`object-fit`](https://developer.mozilla.org/en-US/docs/Web/CSS/object-fit)
property to control how the image is resized to fit within the frame.

::: {#sect2 .notecard .note}
**Note:** Use these properties on the child `<img>` element, **not** the
`<picture>` element.
:::
:::

## Examples

::: section-content
These examples demonstrate how different attributes of the
[`<source>`](source) element change the selection of the image inside
`<picture>`.
:::

### The media attribute {#the_media_attribute}

::: section-content
The `media` attribute specifies a media condition (similar to a media
query) that the user agent will evaluate for each [`<source>`](source)
element.

If the [`<source>`](source)\'s media condition evaluates to `false`, the
browser skips it and evaluates the next element inside `<picture>`.

::: code-example
[html]{.language-name}

``` {signature="HTS5sj9/JeZxfgCJb0vNnD+K4YSJezBpfY1Kw5ewzc8=" data-language="html"}
<picture>
  <source srcset="mdn-logo-wide.png" media="(min-width: 600px)" />
  <img src="mdn-logo-narrow.png" alt="MDN" />
</picture>
```
:::
:::

### The srcset attribute {#the_srcset_attribute}

::: section-content
The [srcset](source#srcset) attribute is used to offer a list of
possible images based on size or the display\'s pixel density.

It is composed of a comma-separated list of image descriptors. Each
image descriptor is composed of a URL of the image, and *either*:

-   a *width descriptor*, followed by a `w` (such as `300w`); *OR*
-   a *pixel density descriptor*, followed by an `x` (such as `2x`) to
    serve a high-res image for high-DPI screens.

Make sure to note that:

-   width and pixel density descriptors should not be used together
-   a missing pixel density descriptor implies 1x
-   duplicate descriptor values are not allowed (2x & 2x, 100w & 100w)

The following example illustrates the usage of `srcset` attribute with
the `<source>` element to specify a high-density and standard-resolution
image:

::: code-example
[html]{.language-name}

``` {signature="piVj3EaNmHh22ivhAi5wxIZezPeTfc7z0UGtxPKdqgU=" data-language="html"}
<picture>
  <source srcset="logo.png, logo-1.5x.png 1.5x" />
  <img src="logo.png" alt="MDN Web Docs logo" height="320" width="320" />
</picture>
```
:::

The `srcset` attribute can also be used on the `<img>` element without
needing the `<picture>` element. The following example demonstrates how
to use the `srcset` attribute to specify standard-resolution and
high-density images, respectively:

::: code-example
[html]{.language-name}

``` {signature="/4d78HncYXCoBXsvxJLw9D8Sky64SxzK2n6NHR3WL10=" data-language="html"}
<img
  srcset="logo.png, logo-2x.png 2x"
  src="logo.png"
  height="320"
  width="320"
  alt="MDN Web Docs logo" />
```
:::

The `sizes` attribute is not mandatory when using srcset, but it is
recommended to use it in order to provide additional information to the
browser to help it select the best image source.

Without sizes, the browser will use the default size of the image as
specified by its dimensions in pixels. This may not be the best fit for
all devices, especially if the image is displayed on different screen
sizes or in different contexts.

Please note that sizes will have its effect only if width dimension
descriptors are provided with srcset instead of pixel ratio values (200w
instead of 2x for example). For more information on using `srcset`, see
the [Responsive
images](https://developer.mozilla.org/en-US/docs/Learn/HTML/Multimedia_and_embedding/Responsive_images)
documentation.
:::

### The type attribute {#the_type_attribute}

::: section-content
The `type` attribute specifies a [MIME
type](https://developer.mozilla.org/en-US/docs/Web/HTTP/Basics_of_HTTP/MIME_types)
for the resource URL(s) in the [`<source>`](source) element\'s `srcset`
attribute. If the user agent does not support the given type, the
[`<source>`](source) element is skipped.

::: code-example
[html]{.language-name}

``` {signature="zVNOyNoqC/eoScJZQdVdBQnuXcLhZ8ZB/GfEmIpVD5s=" data-language="html"}
<picture>
  <source srcset="photo.avif" type="image/avif" />
  <source srcset="photo.webp" type="image/webp" />
  <img src="photo.jpg" alt="photo" />
</picture>
```
:::
:::

## Specifications

::: _table
  -----------------------------------------------------------------------------------------------------------------
  Specification
  -----------------------------------------------------------------------------------------------------------------
  [HTML Standard\
  [\#
  the-picture-element]{.small}](https://html.spec.whatwg.org/multipage/embedded-content.html#the-picture-element)

  -----------------------------------------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
              Desktop                                                         Mobile                                                                                   
  ----------- --------- ------ --------- ------------------- ------- -------- ----------------- ---------------- --------------------- --------------- --------------- ------------------
              Chrome    Edge   Firefox   Internet Explorer   Opera   Safari   WebView Android   Chrome Android   Firefox for Android   Opera Android   Safari on IOS   Samsung Internet
  `picture`   38        13     38        No                  25      9.1      38                38               38                    25              9.3             3.0
:::

## See also {#see_also}

::: section-content
-   [`<img>`](img) element
-   [`<source>`](source) element
-   Positioning and sizing the picture within its frame:
    [`object-position`](https://developer.mozilla.org/en-US/docs/Web/CSS/object-position)
    and
    [`object-fit`](https://developer.mozilla.org/en-US/docs/Web/CSS/object-fit)
-   [Image file type and format
    guide](https://developer.mozilla.org/en-US/docs/Web/Media/Formats/Image_types)
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Element/picture](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/picture){._attribution-link}
:::
