

# rel=preload



::: section-content
The `preload` value of the [`<link>`](../../element/link) element\'s
[`rel`](../../element/link#rel) attribute lets you declare fetch
requests in the HTML\'s [`<head>`](../../element/head), specifying
resources that your page will need very soon, which you want to start
loading early in the page lifecycle, before browsers\' main rendering
machinery kicks in. This ensures they are available earlier and are less
likely to block the page\'s render, improving performance. Even though
the name contains the term *load*, it doesn\'t load and execute the
script but only schedules it to be downloaded and cached with a higher
priority.
:::

## The basics {#the_basics}

::: section-content
You most commonly use `<link>` to load a CSS file to style your page
with:

::: code-example
[html]{.language-name}

``` {signature="Fy1x8+lx2y3l/bJGL8WXEzKwA9uYxGeqeAOsICWJ844=" data-language="html"}
<link rel="stylesheet" href="styles/main.css" />
```
:::

Here however, we will use a `rel` value of `preload`, which turns
`<link>` into a preloader for any resource we want. You will also need
to specify:

-   The path to the resource in the [`href`](../../element/link#href)
    attribute.
-   The type of resource in the [`as`](../../element/link#as) attribute.

A simple example might look like this (see our [JS and CSS example
source](https://github.com/mdn/html-examples/tree/master/link-rel-preload/js-and-css){target="_blank"},
and [also
live](https://mdn.github.io/html-examples/link-rel-preload/js-and-css/){target="_blank"}):

::: code-example
[html]{.language-name}

``` {signature="3Qr0zNO79CWzpGxlBSrNPKu1pqwx/mbVVBlpM87md7M=" data-language="html"}
<head>
  <meta charset="utf-8" />
  <title>JS and CSS preload example</title>

  <link rel="preload" href="style.css" as="style" />
  <link rel="preload" href="main.js" as="script" />

  <link rel="stylesheet" href="style.css" />
</head>

<body>
  <h1>bouncing balls</h1>
  <canvas></canvas>

  <script src="main.js" defer></script>
</body>
```
:::

Here we preload our CSS and JavaScript files so they will be available
as soon as they are required for the rendering of the page later on.
This example is trivial, as the browser probably discovers the
`<link rel="stylesheet">` and `<script>` elements in the same chunk of
HTML as the preloads, but the benefits can be seen much more clearly the
later resources are discovered and the larger they are. For example:

-   Resources that are pointed to from inside CSS, like fonts or images.
-   Resources that JavaScript can request, like JSON, imported scripts,
    or web workers.
-   Larger images and video files.

`preload` has other advantages too. Using `as` to specify the type of
content to be preloaded allows the browser to:

-   Prioritize resource loading more accurately.
-   Store in the cache for future requests, reusing the resource if
    appropriate.
-   Apply the correct [content security
    policy](https://developer.mozilla.org/en-US/docs/Web/HTTP/CSP) to
    the resource.
-   Set the correct
    [`Accept`](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Accept)
    request headers for it.
:::

### What types of content can be preloaded? {#what_types_of_content_can_be_preloaded}

::: section-content
Many content types can be preloaded. The possible `as` attribute values
are:

-   `audio`: Audio file, as typically used in
    [`<audio>`](../../element/audio).
-   `document`: An HTML document intended to be embedded by a
    [`<frame>`](../../element/frame) or
    [`<iframe>`](../../element/iframe).
-   `embed`: A resource to be embedded inside an
    [`<embed>`](../../element/embed) element.
-   `fetch`: Resource to be accessed by a fetch or XHR request, such as
    an ArrayBuffer, WebAssembly binary, or JSON file.
-   `font`: Font file.
-   `image`: Image file.
-   `object`: A resource to be embedded inside an
    [`<object>`](../../element/object) element.
-   `script`: JavaScript file.
-   `style`: CSS stylesheet.
-   `track`: WebVTT file.
-   `worker`: A JavaScript web worker or shared worker.
-   `video`: Video file, as typically used in
    [`<video>`](../../element/video).

::: {#sect1 .notecard .note}
**Note:** `font` and `fetch` preloading requires the `crossorigin`
attribute to be set; see [CORS-enabled fetches](#cors-enabled_fetches)
below.
:::

::: {#sect2 .notecard .note}
**Note:** There\'s more detail about these values and the web features
they expect to be consumed by in the Preload spec --- see [link element
extensions](https://w3c.github.io/preload/#link-element-extensions){target="_blank"}.
Also note that the full list of values the `as` attribute can take is
governed by the Fetch spec --- see [request
destinations](https://fetch.spec.whatwg.org/#concept-request-destination){target="_blank"}.
:::
:::

## Including a MIME type {#including_a_mime_type}

::: section-content
`<link>` elements can accept a [`type`](../../element/link#type)
attribute, which contains the MIME type of the resource the element
points to. This is especially useful when preloading resources --- the
browser will use the `type` attribute value to work out if it supports
that resource, and will only download it if so, ignoring it if not.

You can see an example of this in our video example (see the [full
source
code](https://github.com/mdn/html-examples/tree/master/link-rel-preload/video){target="_blank"},
and also [the live
version](https://mdn.github.io/html-examples/link-rel-preload/video/){target="_blank"}),
a code snippet from which is shown below. This illustrates the core
behavior behind preloading in general.

::: code-example
[html]{.language-name}

``` {signature="bXIfM4C5rs07wKhoc8SigaJZ2k9+0Mtja1k/zpFWSlA=" data-language="html"}
<head>
  <meta charset="utf-8" />
  <title>Video preload example</title>

  <link rel="preload" href="sintel-short.mp4" as="video" type="video/mp4" />
</head>
<body>
  <video controls>
    <source src="sintel-short.mp4" type="video/mp4" />
    <source src="sintel-short.webm" type="video/webm" />
    <p>
      Your browser doesn't support HTML video. Here is a
      <a href="sintel-short.mp4">link to the video</a> instead.
    </p>
  </video>
</body>
```
:::

The code in the example above causes the `video/mp4` video to be
preloaded only in supporting browsers --- and for users who have
`video/mp4` support in their browsers, causes the `video/mp4` video to
actually be used (since it\'s the first
[`<source>`](../../element/source) specified). That makes the video
player hopefully smoother/more responsive for users who have `video/mp4`
support in their browsers.

Note that for users whose browsers have both `video/mp4` and
`video/webm` support, if in that code a
`<link rel="preload" href="sintel-short.webm" as="video" type="video/webm">`
element were also specified, then *both* the `video/mp4` and
`video/webm` videos would be preloaded --- even though only one of them
would actually be used.

Therefore, specifying preloading for multiple types of the same resource
is discouraged. Instead, the best practice is to specify preloading only
for the type the majority of your users are likely to actually use.
That\'s why the code in the example above doesn\'t specify preloading
for the `video/webm` video.

However, the lack of preloading doesn\'t prevent the `video/webm` video
from actually being used by those who need it: for users whose browsers
don\'t have `video/mp4` support but do have `video/webm` support, the
code in the example above does still cause the `video/webm` video to be
used --- but it does so without also causing it to also be preloaded
unnecessarily for the majority of other users.
:::

## CORS-enabled fetches {#cors-enabled_fetches}

::: section-content
When preloading resources that are fetched with
[CORS](https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS) enabled
(e.g.
[`fetch()`](https://developer.mozilla.org/en-US/docs/Web/API/fetch),
[`XMLHttpRequest`](https://developer.mozilla.org/en-US/docs/Web/API/XMLHttpRequest)
or
[fonts](https://developer.mozilla.org/en-US/docs/Web/CSS/@font-face)),
special care needs to be taken to setting the
[`crossorigin`](../../element/link#crossorigin) attribute on your
[`<link>`](../../element/link) element. The attribute needs to be set to
match the resource\'s CORS and credentials mode, even when the fetch is
not cross-origin.

As mentioned above, one interesting case where this applies is font
files. Because of various reasons, these have to be fetched using
anonymous-mode CORS (see [Font fetching
requirements](https://drafts.csswg.org/css-fonts/#font-fetching-requirements){target="_blank"}).

Let\'s use this case as an example. You can see the full [example source
code on
GitHub](https://github.com/mdn/html-examples/tree/master/link-rel-preload/fonts){target="_blank"}
([also see it
live](https://mdn.github.io/html-examples/link-rel-preload/fonts/){target="_blank"}):

::: code-example
[html]{.language-name}

``` {signature="/dOvrgkbrmb1VH98URZWLpCsEVUZJqkJn8Tjg9vrDuI=" data-language="html"}
<head>
  <meta charset="utf-8" />
  <title>Web font example</title>

  <link
    rel="preload"
    href="fonts/cicle_fina-webfont.woff2"
    as="font"
    type="font/woff2"
    crossorigin />
  <link
    rel="preload"
    href="fonts/zantroke-webfont.woff2"
    as="font"
    type="font/woff2"
    crossorigin />

  <link href="style.css" rel="stylesheet" />
</head>
<body>
  …
</body>
```
:::

Not only are we providing the MIME type hints in the `type` attributes,
but we are also providing the `crossorigin` attribute to make sure the
preload\'s CORS mode matches the eventual font resource request.
:::

## Including media {#including_media}

::: section-content
One nice feature of `<link>` elements is their ability to accept
[`media`](../../element/link#media) attributes. These can accept [media
types](https://developer.mozilla.org/en-US/docs/Web/CSS/@media#media_types)
or full-blown [media
queries](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_media_queries/Using_media_queries),
allowing you to do responsive preloading!

Let\'s look at an example (see it on GitHub --- [source
code](https://github.com/mdn/html-examples/tree/master/link-rel-preload/media){target="_blank"},
[live
example](https://mdn.github.io/html-examples/link-rel-preload/media/){target="_blank"}):

::: code-example
[html]{.language-name}

``` {signature="wu6VDO6qfsibEfG5ZPLvtqfLp3FD4PB5V+hEJxOI2kM=" data-language="html"}
<head>
  <meta charset="utf-8" />
  <title>Responsive preload example</title>

  <link
    rel="preload"
    href="bg-image-narrow.png"
    as="image"
    media="(max-width: 600px)" />
  <link
    rel="preload"
    href="bg-image-wide.png"
    as="image"
    media="(min-width: 601px)" />

  <link rel="stylesheet" href="main.css" />
</head>
<body>
  <header>
    <h1>My site</h1>
  </header>

  <script>
    const mediaQueryList = window.matchMedia("(max-width: 600px)");
    const header = document.querySelector("header");

    if (mediaQueryList.matches) {
      header.style.backgroundImage = "url(bg-image-narrow.png)";
    } else {
      header.style.backgroundImage = "url(bg-image-wide.png)";
    }
  </script>
</body>
```
:::

We include `media` attributes on our `<link>` elements so that a narrow
image is preloaded if the user has a narrow viewport, and a wider image
is loaded if they have a wide viewport. We use
[`Window.matchMedia`](https://developer.mozilla.org/en-US/docs/Web/API/Window/matchMedia)
/
[`MediaQueryList`](https://developer.mozilla.org/en-US/docs/Web/API/MediaQueryList)
to do this (see [Testing media
queries](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_media_queries/Testing_media_queries)
for more).

This makes it much more likely that the font will be available for the
page render, cutting down on FOUT (flash of unstyled text).

This doesn\'t have to be limited to images, or even files of the same
type --- think big! You could perhaps preload and display a simple SVG
diagram if the user is on a narrow screen where bandwidth and CPU is
potentially more limited, or preload a complex chunk of JavaScript then
use it to render an interactive 3D model if the user\'s resources are
more plentiful.
:::

## Scripting and preloads {#scripting_and_preloads}

::: section-content
::: {#sect3 .notecard .note}
**Note:** Use [`<link rel="modulepreload">`](modulepreload) instead if
you are working with [JavaScript
modules](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules).
:::

Another nice thing about these preloads is that you can execute them
with script. For example, here we create a
[`HTMLLinkElement`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLLinkElement)
instance, then attach it to the DOM:

::: code-example
[js]{.language-name}

``` {signature="8GShPYRKgV1EntJUC1XRqeGIVGlNJ4Ge2PwuSi8nS44=" data-language="js"}
const preloadLink = document.createElement("link");
preloadLink.href = "myscript.js";
preloadLink.rel = "preload";
preloadLink.as = "script";
document.head.appendChild(preloadLink);
```
:::

This means that the browser will preload the `myscript.js` file, but not
actually use it yet. To use it, you could do this:

::: code-example
[js]{.language-name}

``` {signature="4LhLTrzH4GchtbyiNlcYdN9JcBetf3+4zukpHK0nCEA=" data-language="js"}
const preloadedScript = document.createElement("script");
preloadedScript.src = "myscript.js";
document.body.appendChild(preloadedScript);
```
:::

This is useful when you want to preload a script, but then defer
execution until exactly when you need it.
:::

## Specifications

::: _table
  --------------------------------------------------------------------------------------------------
  Specification
  --------------------------------------------------------------------------------------------------
  [HTML Standard\
  [\#
  link-type-preload]{.small}](https://html.spec.whatwg.org/multipage/links.html#link-type-preload)

  --------------------------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
  -----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
              Desktop                                                                                                           Mobile                                                                                                                 
  ----------- ---------------------- ---------------------- --------------------------------------- ---------- ------- -------- ------------------------------------ ---------------------- --------------------------------------- --------- -------- ------------------------------------
              Chrome                 Edge                   Firefox                                 Internet   Opera   Safari   WebView Android                      Chrome Android         Firefox for Android                     Opera     Safari   Samsung Internet
                                                                                                    Explorer                                                                                                                        Android   on IOS   

  `preload`   50                     ≤79                    85                                      No         37      No       50                                   50                     85                                      No        No       5.0
                                                                                                                                                                                                                                                       
              Doesn't support        Doesn't support        56--57                                                              `as="document"` is unsupported. See  Doesn't support        56--57                                                     `as="document"` is unsupported. See
              `as="audio"`,          `as="audio"`,                                                                              [bug                                 `as="audio"`,                                                                     [bug
              `as="audioworklet"`,   `as="audioworklet"`,   Disabled due to various web                                         593267](https://crbug.com/593267).   `as="audioworklet"`,   Disabled due to various web                                593267](https://crbug.com/593267).
              `as="document"`,       `as="document"`,       compatibility issues (e.g. [bug                                                                          `as="document"`,       compatibility issues (e.g. [bug                            
              `as="embed"`,          `as="embed"`,          1405761](https://bugzil.la/1405761)).                                                                    `as="embed"`,          1405761](https://bugzil.la/1405761)).                      
              `as="manifest"`,       `as="manifest"`,                                                                                                                `as="manifest"`,                                                                  
              `as="object"`,         `as="object"`,                                                                                                                  `as="object"`,                                                                    
              `as="paintworklet"`,   `as="paintworklet"`,                                                                                                            `as="paintworklet"`,                                                              
              `as="report"`,         `as="report"`,                                                                                                                  `as="report"`,                                                                    
              `as="sharedworker"`,   `as="sharedworker"`,                                                                                                            `as="sharedworker"`,                                                              
              `as="video"`,          `as="video"`,                                                                                                                   `as="video"`,                                                                     
              `as="worker"`, or      `as="worker"`, or                                                                                                               `as="worker"`, or                                                                 
              `as="xslt"`.           `as="xslt"`.                                                                                                                    `as="xslt"`.                                                                      
  -----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
:::

## See also {#see_also}

::: section-content
-   [Speculative
    loading](https://developer.mozilla.org/en-US/docs/Web/Performance/Speculative_loading)
    for a comparison of `<link rel="preload">` and other similar
    performance improvement features.
-   [Preload: What Is It Good
    For?](https://www.smashingmagazine.com/2016/02/preload-what-is-it-good-for/){target="_blank"}
    by Yoav Weiss
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes/rel/preload](https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes/rel/preload){._attribution-link}
:::
