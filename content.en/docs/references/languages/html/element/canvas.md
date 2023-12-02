

# \<canvas\>: The Graphics Canvas element



::: section-content
Use the `<canvas>` with either the [canvas scripting
API](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API) or the
[WebGL API](https://developer.mozilla.org/en-US/docs/Web/API/WebGL_API)
to draw graphics and animations.

<figure class="table-container">
<div class="_table">
<table class="properties">
<tbody>
<tr class="odd">
<th scope="row"><a href="../content_categories">Content
categories</a></th>
<td><a href="../content_categories#flow_content">Flow content</a>, <a
href="../content_categories#phrasing_content">phrasing content</a>, <a
href="../content_categories#embedded_content">embedded content</a>,
palpable content.</td>
</tr>
<tr class="even">
<th scope="row">Permitted content</th>
<td>Transparent but with no <a
href="../content_categories#interactive_content">interactive content</a>
descendants except for <a href="a"><code>&lt;a&gt;</code></a> elements,
<a href="button"><code>&lt;button&gt;</code></a> elements, <a
href="input"><code>&lt;input&gt;</code></a> elements whose <a
href="input#type"><code>type</code></a> attribute is
<code>checkbox</code>, <code>radio</code>, or <code>button</code>.</td>
</tr>
<tr class="odd">
<th scope="row">Tag omission</th>
<td>None, both the starting and ending tag are mandatory.</td>
</tr>
<tr class="even">
<th scope="row">Permitted parents</th>
<td>Any element that accepts <a
href="../content_categories#phrasing_content">phrasing content</a>.</td>
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
href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLCanvasElement"><code>HTMLCanvasElement</code></a></td>
</tr>
</tbody>
</table>

</figure>
:::

## Attributes

::: section-content
This element\'s attributes include the [global
attributes](../global_attributes).

[`height`](#height)

:   The height of the coordinate space in CSS pixels. Defaults to 150.

[`moz-opaque`](#moz-opaque) [Non-standard]{.visually-hidden} [Deprecated]{.visually-hidden}

:   Lets the canvas know whether translucency will be a factor. If the
    canvas knows there\'s no translucency, painting performance can be
    optimized. This is only supported by Mozilla-based browsers; use the
    standardized
    [`canvas.getContext('2d', { alpha: false })`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLCanvasElement/getContext)
    instead.

[`width`](#width)

:   The width of the coordinate space in CSS pixels. Defaults to 300.
:::

## Usage notes {#usage_notes}

### Alternative content {#alternative_content}

::: section-content
You should provide alternate content inside the `<canvas>` block. That
content will be rendered both on older browsers that don\'t support
canvas and in browsers with JavaScript disabled.
:::

### Closing `</canvas>` tag {#closing_canvas_tag}

::: section-content
Unlike the [`<img>`](img) element, the
[`<canvas>`](canvas){aria-current="page"} element **requires** the
closing tag (`</canvas>`).
:::

### Sizing the canvas using CSS versus HTML {#sizing_the_canvas_using_css_versus_html}

::: section-content
The displayed size of the canvas can be changed using CSS, but if you do
this the image is scaled during rendering to fit the styled size, which
can make the final graphics rendering end up being distorted.

It is better to specify your canvas dimensions by setting the `width`
and `height` attributes directly on the `<canvas>` elements, either
directly in the HTML or by using JavaScript.
:::

### Maximum canvas size {#maximum_canvas_size}

::: section-content
The exact maximum size of a `<canvas>` element depends on the browser
and environment. While in most cases the maximum dimensions exceed
10,000 x 10,000 pixels, notably iOS devices limit the canvas size to
only 4,096 x 4,096 pixels. See [canvas size limits in different browsers
and
devices](https://github.com/jhildenbiddle/canvas-size#test-results){target="_blank"}
(2021).

::: {#sect1 .notecard .note}
**Note:** Exceeding the maximum dimensions or area renders the canvas
unusable --- drawing commands will not work.
:::
:::

### Using an offscreen canvas {#using_an_offscreen_canvas}

::: section-content
A canvas can be rendered using the
[`OffscreenCanvas`](https://developer.mozilla.org/en-US/docs/Web/API/OffscreenCanvas)
API where the document and canvas are decoupled. The benefit is that a
[worker
thread](https://developer.mozilla.org/en-US/docs/Web/API/Web_Workers_API/Using_web_workers)
can handle canvas rendering and the main thread of your web application
is not blocked by canvas operations. By parallelizing work, other UI
elements of your web application will remain responsive even if you are
running complex graphics on an offscreen canvas. For more information,
see the
[`OffscreenCanvas`](https://developer.mozilla.org/en-US/docs/Web/API/OffscreenCanvas)
API documentation.
:::

## Examples

### HTML

::: section-content
This code snippet adds a canvas element to your HTML document. A
fallback text is provided if a browser is unable to read or render the
canvas.

::: code-example
[html]{.language-name}

``` {signature="hfa+vk8wuoyLX4dWeRBAp5cp86fF68Zrkrowp14bfkQ=" data-language="html"}
<canvas width="120" height="120">
  An alternative text describing what your canvas displays.
</canvas>
```
:::
:::

### JavaScript

::: section-content
Then in the JavaScript code, call
[`HTMLCanvasElement.getContext()`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLCanvasElement/getContext)
to get a drawing context and start drawing onto the canvas:

::: code-example
[js]{.language-name}

``` {signature="xE4OlKEN2zzp00MGD/z59mQBMoPMoR02uz/fKLi67as=" data-language="js"}
const canvas = document.querySelector("canvas");
const ctx = canvas.getContext("2d");
ctx.fillStyle = "green";
// Add a rectangle at (10, 10) with size 100x100 pixels
ctx.fillRect(10, 10, 100, 100);
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

## Accessibility concerns {#accessibility_concerns}

### Alternative content {#alternative_content_2}

::: section-content
The `<canvas>` element on its own is just a bitmap and does not provide
information about any drawn objects. Canvas content is not exposed to
accessibility tools as semantic HTML is. In general, you should avoid
using canvas in an accessible website or app. The following guides can
help to make it more accessible.

-   [Canvas accessibility use
    cases](https://www.w3.org/WAI/PF/HTML/wiki/Canvas_Accessibility_Use_Cases){target="_blank"}
-   [Canvas element accessibility
    issues](https://www.w3.org/html/wg/wiki/AddedElementCanvas){target="_blank"}
-   [HTML Canvas Accessibility in Firefox 13 -- by Steve
    Faulkner](https://www.tpgi.com/html5-canvas-accessibility-in-firefox-13/){target="_blank"}
-   [Best practices for interactive canvas
    elements](https://html.spec.whatwg.org/multipage/scripting.html#best-practices){target="_blank"}
:::

## Specifications

::: _table
  -----------------------------------------------------------------------------------------------------
  Specification
  -----------------------------------------------------------------------------------------------------
  [HTML Standard\
  [\#
  the-canvas-element]{.small}](https://html.spec.whatwg.org/multipage/canvas.html#the-canvas-element)

  -----------------------------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
  -------------------------------------------------------------------------------------------------------------------------------------------------------
                 Desktop                                                               Mobile                                                  
  -------------- --------- ------ ---------------- ---------- ------- ---------------- --------- --------- ---------------- --------- -------- ----------
                 Chrome    Edge   Firefox          Internet   Opera   Safari           WebView   Chrome    Firefox for      Opera     Safari   Samsung
                                                   Explorer                            Android   Android   Android          Android   on IOS   Internet

  `canvas`       1         12     1.5              9          9       2                37        18        4                10.1      1        1.0
                                                                                                                                               
                                  \[\"Before                          Although early                       \[\"Before                          
                                  Firefox 5, the                      versions of                          Firefox 5, the                      
                                  canvas width and                    Apple\'s Safari                      canvas width and                    
                                  height were                         browser don\'t                       height were                         
                                  signed integers                     require the                          signed integers                     
                                  instead of                          closing tag, the                     instead of                          
                                  unsigned                            specification                        unsigned                            
                                  integers.\",                        indicates that                       integers.\",                        
                                  \"Before Firefox                    it is required,                      \"Before Firefox                    
                                  6, a \<canvas\>                     so you should be                     6, a \<canvas\>                     
                                  element with a                      sure to include                      element with a                      
                                  zero width or                       it for broadest                      zero width or                       
                                  height would be                     compatibility.                       height would be                     
                                  rendered as if                      Before version                       rendered as if                      
                                  it had default                      2, Safari will                       it had default                      
                                  dimensions.\",                      render the                           dimensions.\",                      
                                  \"Before Firefox                    content of the                       \"Before Firefox                    
                                  12, if                              fallback in                          12, if                              
                                  JavaScript is                       addition to the                      JavaScript is                       
                                  disabled, the                       canvas itself                        disabled, the                       
                                  \<canvas\>                          unless you use                       \<canvas\>                          
                                  element was                         CSS tricks to                        element was                         
                                  being rendered                      mask it.                             being rendered                      
                                  instead of                                                               instead of                          
                                  showing the                                                              showing the                         
                                  fallback content                                                         fallback content                    
                                  as per the                                                               as per the                          
                                  specification.                                                           specification.                      
                                  Since then, the                                                          Since then, the                     
                                  fallback content                                                         fallback content                    
                                  is rendered                                                              is rendered                         
                                  instead.\"\]                                                             instead.\"\]                        

  `height`       1         12     1.5              9          9       2                37        18        4                10.1      1        1.0
                                                                                                                                               
                                  \[\"Before                          Although early                       \[\"Before                          
                                  Firefox 5, the                      versions of                          Firefox 5, the                      
                                  canvas width and                    Apple\'s Safari                      canvas width and                    
                                  height were                         browser don\'t                       height were                         
                                  signed integers                     require the                          signed integers                     
                                  instead of                          closing tag, the                     instead of                          
                                  unsigned                            specification                        unsigned                            
                                  integers.\",                        indicates that                       integers.\",                        
                                  \"Before Firefox                    it is required,                      \"Before Firefox                    
                                  6, a \<canvas\>                     so you should be                     6, a \<canvas\>                     
                                  element with a                      sure to include                      element with a                      
                                  zero width or                       it for broadest                      zero width or                       
                                  height would be                     compatibility.                       height would be                     
                                  rendered as if                      Before version                       rendered as if                      
                                  it had default                      2, Safari will                       it had default                      
                                  dimensions.\",                      render the                           dimensions.\",                      
                                  \"Before Firefox                    content of the                       \"Before Firefox                    
                                  12, if                              fallback in                          12, if                              
                                  JavaScript is                       addition to the                      JavaScript is                       
                                  disabled, the                       canvas itself                        disabled, the                       
                                  \<canvas\>                          unless you use                       \<canvas\>                          
                                  element was                         CSS tricks to                        element was                         
                                  being rendered                      mask it.                             being rendered                      
                                  instead of                                                               instead of                          
                                  showing the                                                              showing the                         
                                  fallback content                                                         fallback content                    
                                  as per the                                                               as per the                          
                                  specification.                                                           specification.                      
                                  Since then, the                                                          Since then, the                     
                                  fallback content                                                         fallback content                    
                                  is rendered                                                              is rendered                         
                                  instead.\"\]                                                             instead.\"\]                        

  `moz-opaque`   No        No     3.5              No         No      No               No        No        4                No        No       No

  `width`        1         12     1.5              9          9       2                37        18        4                10.1      1        1.0
                                                                                                                                               
                                  \[\"Before                          Although early                       \[\"Before                          
                                  Firefox 5, the                      versions of                          Firefox 5, the                      
                                  canvas width and                    Apple\'s Safari                      canvas width and                    
                                  height were                         browser don\'t                       height were                         
                                  signed integers                     require the                          signed integers                     
                                  instead of                          closing tag, the                     instead of                          
                                  unsigned                            specification                        unsigned                            
                                  integers.\",                        indicates that                       integers.\",                        
                                  \"Before Firefox                    it is required,                      \"Before Firefox                    
                                  6, a \<canvas\>                     so you should be                     6, a \<canvas\>                     
                                  element with a                      sure to include                      element with a                      
                                  zero width or                       it for broadest                      zero width or                       
                                  height would be                     compatibility.                       height would be                     
                                  rendered as if                      Before version                       rendered as if                      
                                  it had default                      2, Safari will                       it had default                      
                                  dimensions.\",                      render the                           dimensions.\",                      
                                  \"Before Firefox                    content of the                       \"Before Firefox                    
                                  12, if                              fallback in                          12, if                              
                                  JavaScript is                       addition to the                      JavaScript is                       
                                  disabled, the                       canvas itself                        disabled, the                       
                                  \<canvas\>                          unless you use                       \<canvas\>                          
                                  element was                         CSS tricks to                        element was                         
                                  being rendered                      mask it.                             being rendered                      
                                  instead of                                                               instead of                          
                                  showing the                                                              showing the                         
                                  fallback content                                                         fallback content                    
                                  as per the                                                               as per the                          
                                  specification.                                                           specification.                      
                                  Since then, the                                                          Since then, the                     
                                  fallback content                                                         fallback content                    
                                  is rendered                                                              is rendered                         
                                  instead.\"\]                                                             instead.\"\]                        
  -------------------------------------------------------------------------------------------------------------------------------------------------------
:::

## See also {#see_also}

::: section-content
-   [Canvas
    API](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API)
-   [Canvas
    tutorial](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API/Tutorial)
-   [Canvas-related
    demos](https://developer.mozilla.org/en-US/docs/Web/Demos#canvas)
-   [OffscreenCanvas](https://developer.mozilla.org/en-US/docs/Web/API/OffscreenCanvas)
-   [Canvas cheat
    sheet](https://simon.html5.org/dump/html5-canvas-cheat-sheet.html){target="_blank"}
    (2009)
-   [Canvas cheat
    sheet](https://websitesetup.org/wp-content/uploads/2015/11/Infopgraphic-CanvasCheatSheet-Final2.pdf){target="_blank"}
    (pdf) (2015)
-   [Canvas cheat
    sheet](https://www.coding-dude.com/wp/wp-content/uploads/2020/09/HTML5-canvas-cheat-sheet.pdf){target="_blank"}
    (pdf) (2020)
-   [Canvas introduction by
    Apple](https://developer.apple.com/library/archive/documentation/AudioVideo/Conceptual/HTML-canvas-guide/Introduction/Introduction.html){target="_blank"}
    (2013)
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Element/canvas](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/canvas){._attribution-link}
:::
