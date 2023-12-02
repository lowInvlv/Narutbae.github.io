

# \<source\>: The Media or Image Source element



::: section-content
The `<source>` [HTML](../index) element specifies multiple media
resources for the [`<picture>`](picture), the [`<audio>`](audio)
element, or the [`<video>`](video) element. It is a [void
element](https://developer.mozilla.org/en-US/docs/Glossary/Void_element),
meaning that it has no content and does not have a closing tag. It is
commonly used to offer the same media content in multiple file formats
in order to provide compatibility with a broad range of browsers given
their differing support for [image file
formats](https://developer.mozilla.org/en-US/docs/Web/Media/Formats/Image_types)
and [media file
formats](https://developer.mozilla.org/en-US/docs/Web/Media/Formats).
:::

## Try it {#try_it}

::: section-content
::: iframe
::: {.output-header .border-rounded-top}
#### HTML Demo: \<source\> {#html-demo-source .output-heading}

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
    <video controls width="250" height="200" muted>
      <source src="/media/cc0-videos/flower.webm" type="video/webm" />
      <source src="/media/cc0-videos/flower.mp4" type="video/mp4" />
      Download the
      <a href="/media/cc0-videos/flower.webm">WEBM</a>
      or
      <a href="/media/cc0-videos/flower.mp4">MP4</a>
      video.
    </video>
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
<td>None; it is a <a
href="https://developer.mozilla.org/en-US/docs/Glossary/Void_element">void
element</a>.</td>
</tr>
<tr class="odd">
<th scope="row">Tag omission</th>
<td>It must have a start tag, but must not have an end tag.</td>
</tr>
<tr class="even">
<th scope="row">Permitted parents</th>
<td>A media element—<a href="audio"><code>&lt;audio&gt;</code></a> or <a
href="video"><code>&lt;video&gt;</code></a>—and it must be placed before
any <a href="../content_categories#flow_content">flow content</a> or <a
href="track"><code>&lt;track&gt;</code></a> element. A <a
href="picture"><code>&lt;picture&gt;</code></a> element, and it must be
placed before the <a href="img"><code>&lt;img&gt;</code></a>
element.</td>
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
href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLSourceElement"><code>HTMLSourceElement</code></a></td>
</tr>
</tbody>
</table>

</figure>
:::

## Attributes

::: section-content
This element includes the [global attributes](../global_attributes).

[`type`](#type)

:   The [MIME media type of the
    image](https://developer.mozilla.org/en-US/docs/Web/Media/Formats/Image_types)
    or [other media
    type](https://developer.mozilla.org/en-US/docs/Web/Media/Formats/Containers),
    optionally with a [`codecs`
    parameter](https://developer.mozilla.org/en-US/docs/Web/Media/Formats/codecs_parameter).

[`src`](#src)

:   Required if the `source` element\'s parent is an [`<audio>`](audio)
    and [`<video>`](video) element, but not allowed if the `source`
    element\'s parent is a [`<picture>`](picture) element.

    Address of the media resource.

[`srcset`](#srcset)

:   Required if the `source` element\'s parent is a
    [`<picture>`](picture) element, but not allowed if the `source`
    element\'s parent is an [`<audio>`](audio) or [`<video>`](video)
    element.

    A list of one or more strings, separated by commas, indicating a set
    of possible images represented by the source for the browser to use.
    Each string is composed of:

    1.  One URL specifying an image.
    2.  A width descriptor, which consists of a string containing a
        positive integer directly followed by `"w"`, such as `300w`. The
        default value, if missing, is the infinity.
    3.  A pixel density descriptor, that is a positive floating number
        directly followed by `"x"`. The default value, if missing, is
        `1x`.

    Each string in the list must have at least a width descriptor or a
    pixel density descriptor to be valid. The two types of descriptors
    should not be mixed together and only one should be used
    consistently throughout the list. Among the list, the value of each
    descriptor must be unique. The browser chooses the most adequate
    image to display at a given point of time. If the `sizes` attribute
    is present, then a width descriptor must be specified for each
    string. If the browser does not support `srcset`, then `src` will be
    used for the default source.

[`sizes`](#sizes)

:   Allowed if the `source` element\'s parent is a
    [`<picture>`](picture) element, but not allowed if the `source`
    element\'s parent is an [`<audio>`](audio) or [`<video>`](video)
    element.

    A list of source sizes that describes the final rendered width of
    the image represented by the source. Each source size consists of a
    comma-separated list of media condition-length pairs. Before laying
    the page out, the browser uses this information to determine which
    image is defined in [`srcset`](#srcset) to use. Please note that
    `sizes` will have its effect only if width dimension descriptors are
    provided with `srcset` instead of pixel ratio values (200w instead
    of 2x for example).

[`media`](#media)

:   [Media
    query](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_media_queries)
    of the resource\'s intended media.

[`height`](#height)

:   Allowed if the `source` element\'s parent is a
    [`<picture>`](picture) element, but not allowed if the `source`
    element\'s parent is an [`<audio>`](audio) or [`<video>`](video)
    element.

    The intrinsic height of the image, in pixels. Must be an integer
    without a unit.

[`width`](#width)

:   Allowed if the `source` element\'s parent is a
    [`<picture>`](picture) element, but not allowed if the `source`
    element\'s parent is an [`<audio>`](audio) or [`<video>`](video)
    element.

    The intrinsic width of the image in pixels. Must be an integer
    without a unit.

If the `type` attribute isn\'t specified, the media\'s type is retrieved
from the server and checked to see if the user agent can handle it; if
it can\'t be rendered, the next `<source>` is checked. If the `type`
attribute is specified, it\'s compared against the types the user agent
can present, and if it\'s not recognized, the server doesn\'t even get
queried; instead, the next `<source>` element is checked at once.

When used in the context of a `<picture>` element, the browser will fall
back to using the image specified by the `<picture>` element\'s
[`<img>`](img) child if it is unable to find a suitable image to use
after examining every provided `<source>`.
:::

## Usage notes {#usage_notes}

::: section-content
The `<source>` element is a **[void
element](https://developer.mozilla.org/en-US/docs/Glossary/Void_element)**,
which means that it not only has no content but also has no closing tag.
That is, you *never* use \"`</source>`\" in your HTML.

For information about image formats supported by web browsers and
guidance on selecting appropriate formats to use, see our [Image file
type and format
guide](https://developer.mozilla.org/en-US/docs/Web/Media/Formats/Image_types)
on the web. For details on the video and audio media types you can use,
see the [Guide to media types formats used on the
web](https://developer.mozilla.org/en-US/docs/Web/Media/Formats).
:::

## Examples

### Video with type attribute example {#video_with_type_attribute_example}

::: section-content
This example demonstrates how to offer a video in WebM format for users
whose browsers support WebM format, Ogg format for users whose browsers
support Ogg format, and a QuickTime format video for users whose
browsers support that. If the `audio` or `video` element is not
supported by the browser, a notice is displayed instead. If the browser
supports the element but does not support any of the specified formats,
an `error` event is raised and the default media controls (if enabled)
will indicate an error. Be sure to reference our [guide to media types
and formats on the
web](https://developer.mozilla.org/en-US/docs/Web/Media/Formats) for
details on what media file formats you can use and how well they\'re
supported by browsers.

::: code-example
[html]{.language-name}

``` {signature="5HgJzmO/ATQufwctR1n74/oGvm60F5LN3zH9tHa9hjs=" data-language="html"}
<video controls>
  <source src="foo.webm" type="video/webm" />
  <source src="foo.ogg" type="video/ogg" />
  <source src="foo.mov" type="video/quicktime" />
  I'm sorry; your browser doesn't support HTML video.
</video>
```
:::
:::

### Video with media attribute example {#video_with_media_attribute_example}

::: section-content
This example demonstrates how to offer an alternate source file for
viewports at or above a certain width. When a user\'s browsing
environment meets the specified `media` condition, the associated
`<source>` element is chosen, and the contents of its `src` attribute
are requested and rendered. If the `media` condition does not match, the
user agent will move on to the next `<source>` in the source order. The
second source option in the below code has no `media` condition, so will
be selected for all other browsing contexts.

::: code-example
[html]{.language-name}

``` {signature="oNc/X6GxAcHQeegr8jv739lOrUerZcpTkZ2Uu+nIu8g=" data-language="html"}
<video controls>
  <source src="foo-large.webm" media="(min-width: 800px)" />
  <source src="foo.webm" />
  I'm sorry; your browser doesn't support HTML video.
</video>
```
:::

For more examples, the learning area article [Video and audio
content](https://developer.mozilla.org/en-US/docs/Learn/HTML/Multimedia_and_embedding/Video_and_audio_content)
is a great resource.
:::

### Picture example {#picture_example}

::: section-content
In this example, two `<source>` elements are included within the
[`<picture>`](picture), providing versions of an image to use when the
available space exceeds certain widths. If the available width is less
than the smallest of these widths, the user agent will fall back to the
image given by the [`<img>`](img) element.

::: code-example
[html]{.language-name}

``` {signature="zM8C3BUibuoydUljMfnaVhaTCvG878n1ry9zY3SAGkU=" data-language="html"}
<picture>
  <source srcset="mdn-logo-wide.png" media="(min-width: 800px)" />
  <source srcset="mdn-logo-medium.png" media="(min-width: 600px)" />
  <img src="mdn-logo-narrow.png" alt="MDN Web Docs" />
</picture>
```
:::

With the `<picture>` element, you must always include an `<img>` with a
fallback image, with an `alt` attribute to ensure accessibility (unless
the image is an irrelevant background decorative image).
:::

### Picture with height & width attributes example {#picture_with_height_width_attributes_example}

::: section-content
In this example, three `<source>` elements with `height` and `width`
attributes are included in a [`<picture>`](picture) element. A [media
query](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_media_queries/Using_media_queries)
allows the browser to select an image to display with the `height` and
`width` attributes based on the
[viewport](https://developer.mozilla.org/en-US/docs/Glossary/Viewport)
size.

::: code-example
[html]{.language-name}

``` {signature="4ABBCazrHHu8u1BhZYxILQlaD6KVGPjtX+m+m/K9TZs=" data-language="html"}
<picture>
  <source
    srcset="landscape.png"
    media="(min-width: 1000px)"
    width="1000"
    height="400" />
  <source
    srcset="square.png"
    media="(min-width: 800px)"
    width="800"
    height="800" />
  <source
    srcset="portrait.png"
    media="(min-width: 600px)"
    width="600"
    height="800" />
  <img
    src="fallback.png"
    alt="Image used when the browser does not support the sources"
    width="500"
    height="400" />
</picture>
```
:::
:::

## Specifications

::: _table
  ---------------------------------------------------------------------------------------------------------------
  Specification
  ---------------------------------------------------------------------------------------------------------------
  [HTML Standard\
  [\#
  the-source-element]{.small}](https://html.spec.whatwg.org/multipage/embedded-content.html#the-source-element)

  ---------------------------------------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
  ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
             Desktop                                                                                      Mobile                                                                                    
  ---------- -------------- ------ ----------------------------------- ---------- -------------- -------- -------------- -------------- ----------------------------------- -------------- -------- --------------
             Chrome         Edge   Firefox                             Internet   Opera          Safari   WebView        Chrome Android Firefox for Android                 Opera Android  Safari   Samsung
                                                                       Explorer                           Android                                                                          on IOS   Internet

  `source`   3              12     3.5                                 9          15             3.1      4.4            18             4                                   14             2        1.0
                                                                                                                                                                                                    
                                   Until Firefox 15, Firefox picked                                                                     Until Firefox 15, Firefox picked                            
                                   the first source element that has a                                                                  the first source element that has a                         
                                   type matching the MIME-type of a                                                                     type matching the MIME-type of a                            
                                   supported media format; see [bug                                                                     supported media format; see [bug                            
                                   449363](https://bugzil.la/449363)                                                                    449363](https://bugzil.la/449363)                           
                                   for details.                                                                                         for details.                                                

  `height`   90             90     108                                 9          76             15       90             90             108                                 64             15       15.0

  `media`    3              12     15                                  9          15             3.1      4.4            18             15                                  14             2        1.0

  `sizes`    38             ≤18    38                                  No         25             9.1      38             38             38                                  25             9.3      3.0
                                                                                                                                                                                                    
             34--38                                                               21--25                  37--38         34--38                                             21--25                  2.0--3.0
                                                                                                                                                                                                    
             Supports a                                                           Supports a              Supports a     Supports a                                         Supports a              Supports a
             subset of the                                                        subset of the           subset of the  subset of the                                      subset of the           subset of the
             syntax for                                                           syntax for              syntax for     syntax for                                         syntax for              syntax for
             resolution                                                           resolution              resolution     resolution                                         resolution              resolution
             switching                                                            switching               switching      switching                                          switching               switching
             (using the `x`                                                       (using the `x`          (using the `x` (using the `x`                                     (using the `x`          (using the `x`
             descriptor),                                                         descriptor),            descriptor),   descriptor),                                       descriptor),            descriptor),
             but not the                                                          but not the             but not the    but not the                                        but not the             but not the
             full syntax                                                          full syntax             full syntax    full syntax                                        full syntax             full syntax
             that can be                                                          that can be             that can be    that can be                                        that can be             that can be
             used with                                                            used with               used with      used with                                          used with               used with
             `sizes` (using                                                       `sizes` (using          `sizes` (using `sizes` (using                                     `sizes` (using          `sizes` (using
             the `w`                                                              the `w`                 the `w`        the `w`                                            the `w`                 the `w`
             descriptor).                                                         descriptor).            descriptor).   descriptor).                                       descriptor).            descriptor).

  `src`      3              12     3.5                                 9          15             3.1      4.4            18             4                                   14             2        1.0

  `srcset`   38             ≤18    38                                  No         25             9.1      38             38             38                                  25             9.3      3.0
                                                                                                                                                                                                    
             34--38                                                               21--25                  37--38         34--38                                             21--25                  2.0--3.0
                                                                                                                                                                                                    
             Supports a                                                           Supports a              Supports a     Supports a                                         Supports a              Supports a
             subset of the                                                        subset of the           subset of the  subset of the                                      subset of the           subset of the
             syntax for                                                           syntax for              syntax for     syntax for                                         syntax for              syntax for
             resolution                                                           resolution              resolution     resolution                                         resolution              resolution
             switching                                                            switching               switching      switching                                          switching               switching
             (using the `x`                                                       (using the `x`          (using the `x` (using the `x`                                     (using the `x`          (using the `x`
             descriptor),                                                         descriptor),            descriptor),   descriptor),                                       descriptor),            descriptor),
             but not the                                                          but not the             but not the    but not the                                        but not the             but not the
             full syntax                                                          full syntax             full syntax    full syntax                                        full syntax             full syntax
             that can be                                                          that can be             that can be    that can be                                        that can be             that can be
             used with                                                            used with               used with      used with                                          used with               used with
             `sizes` (using                                                       `sizes` (using          `sizes` (using `sizes` (using                                     `sizes` (using          `sizes` (using
             the `w`                                                              the `w`                 the `w`        the `w`                                            the `w`                 the `w`
             descriptor).                                                         descriptor).            descriptor).   descriptor).                                       descriptor).            descriptor).

  `type`     3              12     3.5                                 9          15             3.1      4.4            18             4                                   14             2        1.0

  `width`    90             90     108                                 9          76             15       90             90             108                                 64             15       15.0
  ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
:::

## See also {#see_also}

::: section-content
-   [Guide to media types and formats on the
    web](https://developer.mozilla.org/en-US/docs/Web/Media/Formats)
-   [Image file type and format
    guide](https://developer.mozilla.org/en-US/docs/Web/Media/Formats/Image_types)
-   [`<picture>`](picture) element
-   [`<audio>`](audio) element
-   [`<video>`](video) element
-   [Web
    Performance](https://developer.mozilla.org/en-US/docs/Learn/Performance)
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Element/source](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/source){._attribution-link}
:::
