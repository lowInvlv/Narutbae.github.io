

# \<script\>: The Script element



::: section-content
The `<script>` [HTML](../index) element is used to embed executable code
or data; this is typically used to embed or refer to JavaScript code.
The `<script>` element can also be used with other languages, such as
[WebGL](https://developer.mozilla.org/en-US/docs/Web/API/WebGL_API)\'s
GLSL shader programming language and
[JSON](https://developer.mozilla.org/en-US/docs/Glossary/JSON).

<figure class="table-container">
<div class="_table">
<table class="properties">
<tbody>
<tr class="odd">
<th scope="row"><a href="../content_categories">Content
categories</a></th>
<td><a href="../content_categories#metadata_content">Metadata
content</a>, <a href="../content_categories#flow_content">Flow
content</a>, <a href="../content_categories#phrasing_content">Phrasing
content</a>.</td>
</tr>
<tr class="even">
<th scope="row">Permitted content</th>
<td>Dynamic script such as <code>text/javascript</code>.</td>
</tr>
<tr class="odd">
<th scope="row">Tag omission</th>
<td>None, both the starting and ending tag are mandatory.</td>
</tr>
<tr class="even">
<th scope="row">Permitted parents</th>
<td>Any element that accepts <a
href="../content_categories#metadata_content">metadata content</a>, or
any element that accepts <a
href="../content_categories#phrasing_content">phrasing content</a>.</td>
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
href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLScriptElement"><code>HTMLScriptElement</code></a></td>
</tr>
</tbody>
</table>

</figure>
:::

## Attributes

::: section-content
This element includes the [global attributes](../global_attributes).

[`async`](#async)

:   For classic scripts, if the `async` attribute is present, then the
    classic script will be fetched in parallel to parsing and evaluated
    as soon as it is available.

    For [module
    scripts](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules),
    if the `async` attribute is present then the scripts and all their
    dependencies will be fetched in parallel to parsing and evaluated as
    soon as they are available.

    This attribute allows the elimination of **parser-blocking
    JavaScript** where the browser would have to load and evaluate
    scripts before continuing to parse. `defer` has a similar effect in
    this case.

    This is a boolean attribute: the presence of a boolean attribute on
    an element represents the true value, and the absence of the
    attribute represents the false value.

    See [Browser compatibility](#browser_compatibility) for notes on
    browser support. See also [Async scripts for
    asm.js](https://developer.mozilla.org/en-US/docs/Games/Techniques/Async_scripts).

[`blocking`](#blocking) [Experimental]{.visually-hidden}

:   This attribute explicitly indicates that certain operations should
    be blocked on the fetching of the script. The operations that are to
    be blocked must be a space-separated list of blocking attributes
    listed below.

    -   `render`: The rendering of content on the screen is blocked.

[`crossorigin`](#crossorigin)

:   Normal `script` elements pass minimal information to the
    [`window.onerror`](https://developer.mozilla.org/en-US/docs/Web/API/Window/error_event)
    for scripts which do not pass the standard
    [CORS](https://developer.mozilla.org/en-US/docs/Glossary/CORS)
    checks. To allow error logging for sites which use a separate domain
    for static media, use this attribute. See [CORS settings
    attributes](../attributes/crossorigin) for a more descriptive
    explanation of its valid arguments.

[`defer`](#defer)

:   This Boolean attribute is set to indicate to a browser that the
    script is meant to be executed after the document has been parsed,
    but before firing
    [`DOMContentLoaded`](https://developer.mozilla.org/en-US/docs/Web/API/Document/DOMContentLoaded_event).

    Scripts with the `defer` attribute will prevent the
    `DOMContentLoaded` event from firing until the script has loaded and
    finished evaluating.

    ::: {#sect1 .notecard .warning}
    **Warning:** This attribute must not be used if the `src` attribute
    is absent (i.e. for inline scripts), in this case it would have no
    effect.

    The `defer` attribute has no effect on [module
    scripts](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules)
    --- they defer by default.
    :::

    Scripts with the `defer` attribute will execute in the order in
    which they appear in the document.

    This attribute allows the elimination of **parser-blocking
    JavaScript** where the browser would have to load and evaluate
    scripts before continuing to parse. `async` has a similar effect in
    this case.

[`fetchpriority`](#fetchpriority) [Experimental]{.visually-hidden}

:   Provides a hint of the relative priority to use when fetching an
    external script. Allowed values:

    [`high`](#high)

    :   Signals a high-priority fetch relative to other external
        scripts.

    [`low`](#low)

    :   Signals a low-priority fetch relative to other external scripts.

    [`auto`](#auto)

    :   Default: Signals automatic determination of fetch priority
        relative to other external scripts.

[`integrity`](#integrity)

:   This attribute contains inline metadata that a user agent can use to
    verify that a fetched resource has been delivered free of unexpected
    manipulation. See [Subresource
    Integrity](https://developer.mozilla.org/en-US/docs/Web/Security/Subresource_Integrity).

[`nomodule`](#nomodule)

:   This Boolean attribute is set to indicate that the script should not
    be executed in browsers that support [ES
    modules](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules)
    --- in effect, this can be used to serve fallback scripts to older
    browsers that do not support modular JavaScript code.

[`nonce`](#nonce)

:   A cryptographic nonce (number used once) to allow scripts in a
    [script-src
    Content-Security-Policy](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Security-Policy/script-src).
    The server must generate a unique nonce value each time it transmits
    a policy. It is critical to provide a nonce that cannot be guessed
    as bypassing a resource\'s policy is otherwise trivial.

[`referrerpolicy`](#referrerpolicy)

:   Indicates which
    [referrer](https://developer.mozilla.org/en-US/docs/Web/API/Document/referrer)
    to send when fetching the script, or resources fetched by the
    script:

    -   `no-referrer`: The
        [`Referer`](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Referer)
        header will not be sent.
    -   `no-referrer-when-downgrade`: The
        [`Referer`](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Referer)
        header will not be sent to
        [origin](https://developer.mozilla.org/en-US/docs/Glossary/Origin)s
        without
        [TLS](https://developer.mozilla.org/en-US/docs/Glossary/TLS)
        ([HTTPS](https://developer.mozilla.org/en-US/docs/Glossary/HTTPS)).
    -   `origin`: The sent referrer will be limited to the origin of the
        referring page: its
        [scheme](https://developer.mozilla.org/en-US/docs/Learn/Common_questions/Web_mechanics/What_is_a_URL),
        [host](https://developer.mozilla.org/en-US/docs/Glossary/Host),
        and
        [port](https://developer.mozilla.org/en-US/docs/Glossary/Port).
    -   `origin-when-cross-origin`: The referrer sent to other origins
        will be limited to the scheme, the host, and the port.
        Navigations on the same origin will still include the path.
    -   `same-origin`: A referrer will be sent for [same
        origin](https://developer.mozilla.org/en-US/docs/Glossary/Same-origin_policy),
        but cross-origin requests will contain no referrer information.
    -   `strict-origin`: Only send the origin of the document as the
        referrer when the protocol security level stays the same
        (HTTPS→HTTPS), but don\'t send it to a less secure destination
        (HTTPS→HTTP).
    -   `strict-origin-when-cross-origin` (default): Send a full URL
        when performing a same-origin request, only send the origin when
        the protocol security level stays the same (HTTPS→HTTPS), and
        send no header to a less secure destination (HTTPS→HTTP).
    -   `unsafe-url`: The referrer will include the origin *and* the
        path (but not the
        [fragment](https://developer.mozilla.org/en-US/docs/Web/API/HTMLAnchorElement/hash),
        [password](https://developer.mozilla.org/en-US/docs/Web/API/HTMLAnchorElement/password),
        or
        [username](https://developer.mozilla.org/en-US/docs/Web/API/HTMLAnchorElement/username)).
        **This value is unsafe**, because it leaks origins and paths
        from TLS-protected resources to insecure origins.

    ::: {#sect2 .notecard .note}
    **Note:** An empty string value (`""`) is both the default value,
    and a fallback value if `referrerpolicy` is not supported. If
    `referrerpolicy` is not explicitly specified on the `<script>`
    element, it will adopt a higher-level referrer policy, i.e. one set
    on the whole document or domain. If a higher-level policy is not
    available, the empty string is treated as being equivalent to
    `strict-origin-when-cross-origin`.
    :::

[`src`](#src)

:   This attribute specifies the URI of an external script; this can be
    used as an alternative to embedding a script directly within a
    document.

[`type`](script/type)

:   This attribute indicates the type of script represented. The value
    of this attribute will be one of the following:

    [**Attribute is not set (default), an empty string, or a JavaScript MIME type**](#attribute_is_not_set_default_an_empty_string_or_a_javascript_mime_type)

    :   Indicates that the script is a \"classic script\", containing
        JavaScript code. Authors are encouraged to omit the attribute if
        the script refers to JavaScript code rather than specify a MIME
        type. JavaScript MIME types are [listed in the IANA media types
        specification](https://developer.mozilla.org/en-US/docs/Web/HTTP/Basics_of_HTTP/MIME_types#textjavascript).

    [`importmap`](script/type/importmap)

    :   This value indicates that the body of the element contains an
        import map. The import map is a JSON object that developers can
        use to control how the browser resolves module specifiers when
        importing [JavaScript
        modules](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules#importing_modules_using_import_maps).

    [`module`](#module)

    :   This value causes the code to be treated as a JavaScript module.
        The processing of the script contents is deferred. The `charset`
        and `defer` attributes have no effect. For information on using
        `module`, see our [JavaScript
        modules](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules)
        guide. Unlike classic scripts, module scripts require the use of
        the CORS protocol for cross-origin fetching.

    [`speculationrules`](script/type/speculationrules) [Experimental]{.visually-hidden}

    :   This value indicates that the body of the element contains
        speculation rules. Speculation rules take the form of a JSON
        object that determine what resources should be prefetched or
        prerendered by the browser. This is part of the [speculation
        rules
        API](https://developer.mozilla.org/en-US/docs/Web/Performance/Speculative_loading#the_speculation_rules_api).

    [**Any other value**](#any_other_value)

    :   The embedded content is treated as a data block, and won\'t be
        processed by the browser. Developers must use a valid MIME type
        that is not a JavaScript MIME type to denote data blocks. All of
        the other attributes will be ignored, including the `src`
        attribute.
:::

### Deprecated attributes {#deprecated_attributes}

::: section-content

[`charset`](#charset) [Deprecated]{.visually-hidden}

:   If present, its value must be an
    [ASCII](https://developer.mozilla.org/en-US/docs/Glossary/ASCII)
    case-insensitive match for \"`utf-8`\". It\'s unnecessary to specify
    the `charset` attribute, because documents must use UTF-8, and the
    `script` element inherits its character encoding from the document.

[`language`](#language) [Deprecated]{.visually-hidden} [Non-standard]{.visually-hidden}

:   Like the `type` attribute, this attribute identifies the scripting
    language in use. Unlike the `type` attribute, however, this
    attribute\'s possible values were never standardized. The `type`
    attribute should be used instead.
:::

## Notes

::: section-content
Scripts without [`async`](#async), [`defer`](#defer) or `type="module"`
attributes, as well as inline scripts without the `type="module"`
attribute, are fetched and executed immediately before the browser
continues to parse the page.

The script should be served with the `text/javascript` MIME type, but
browsers are lenient and only block them if the script is served with an
image type (`image/*`), a video type (`video/*`), an audio type
(`audio/*`), or `text/csv`. If the script is blocked, an
[`error`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/error_event)
event is sent to the element; otherwise, a
[`load`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/load_event)
event is sent.
:::

## Examples

### Basic usage {#basic_usage}

::: section-content
These examples show how to import (an external) script using the
`<script>` element.

::: code-example
[html]{.language-name}

``` {signature="WL2iP3PQXAZ7+c2DL76Ujc0rBQRjIoXq8yrlyvGe1QA=" data-language="html"}
<script src="javascript.js"></script>
```
:::

And the following examples show how to put (an inline) script inside the
`<script>` element.

::: code-example
[html]{.language-name}

``` {signature="BRn57YYY+rm8KCGVZjolEHCsoPX4ykNAhPEpQnAZTCE=" data-language="html"}
<script>
  alert("Hello World!");
</script>
```
:::
:::

### Module fallback {#module_fallback}

::: section-content
Browsers that support the `module` value for the [`type`](#type)
attribute ignore any script with a `nomodule` attribute. That enables
you to use module scripts while providing `nomodule`-marked fallback
scripts for non-supporting browsers.

::: code-example
[html]{.language-name}

``` {signature="cp7LD7t7m517wr8IDlzKh1px9BlCJoE88rX3TMBj62E=" data-language="html"}
<script type="module" src="main.js"></script>
<script nomodule src="fallback.js"></script>
```
:::
:::

### Importing modules with importmap {#importing_modules_with_importmap}

::: section-content
When importing modules in scripts, if you don\'t use the
[`type=importmap`](#importmap) feature, then each module must be
imported using a module specifier that is either an absolute or relative
URL. In the example below, the first module specifier
(\"./shapes/square.js\") resolves relative to the base URL of the
document, while the second is an absolute URL.

::: code-example
[js]{.language-name}

``` {signature="gXEqEUrcNVdR5bCiOj+b10q6mo7U7GGs1744i1SZZ8c=" data-language="js"}
import { name as squareName, draw } from "./shapes/square.js";
import { name as circleName } from "https://example.com/shapes/circle.js";
```
:::

An import map allows you to provide a mapping that, if matched, can
replace the text in the module specifier. The import map below defines
keys `square` and `circle` that can be used as aliases for the module
specifiers shown above.

::: code-example
[html]{.language-name}

``` {signature="kKMjrUvbBdFWOvRxvt29mabORhnBe+DFdAVIGFVYGoo=" data-language="html"}
<script type="importmap">
  {
    "imports": {
      "square": "./shapes/square.js",
      "circle": "https://example.com/shapes/circle.js"
    }
  }
</script>
```
:::

This allows us to import modules using names in the module specifier
(rather than absolute or relative URLs).

::: code-example
[js]{.language-name}

``` {signature="3z7KTwOPwElmzvBo8T4qhEwW/oNOKzGT6BYzM4NAgYc=" data-language="js"}
import { name as squareName, draw } from "square";
import { name as circleName } from "circle";
```
:::

For more examples of what you can do with import maps, see the
[Importing modules using import
maps](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules#importing_modules_using_import_maps)
section in the JavaScript modules guide.
:::

### Embedding data in HTML {#embedding_data_in_html}

::: section-content
You can also use the `<script>` element to embed data in HTML with
server-side rendering by specifying a valid non-JavaScript MIME type in
the `type` attribute.

::: code-example
[html]{.language-name}

``` {signature="vJ7NhD1+ZiLSNtkVUK7FZEKoZXdtTfmqsXE7k+0s/7Y=" data-language="html"}
<!-- Generated by the server -->
<script id="data" type="application/json">
  {
    "userId": 1234,
    "userName": "Maria Cruz",
    "memberSince": "2000-01-01T00:00:00.000Z"
  }
</script>

<!-- Static -->
<script>
  const userInfo = JSON.parse(document.getElementById("data").text);
  console.log("User information: %o", userInfo);
</script>
```
:::
:::

### Blocking rendering till a script is fetched and executed {#blocking_rendering_till_a_script_is_fetched_and_executed}

::: section-content
You can include `render` token inside a `blocking` attribute; the
rendering of the page will be blocked till the script is fetched and
executed. In the example below, we block rendering on an async script,
so that the script doesn\'t block parsing but is guaranteed to be
evaluated before rendering starts.

::: code-example
[html]{.language-name}

``` {signature="NFlvDEcAnmljjkrp0QZcV/2PS7k6J6Vzu5lNMxxYlpY=" data-language="html"}
<script blocking="render" async src="async-script.js"></script>
```
:::
:::

## Specifications

::: _table
  --------------------------------------------------------------------------------------------------------
  Specification
  --------------------------------------------------------------------------------------------------------
  [HTML Standard\
  [\#
  the-script-element]{.small}](https://html.spec.whatwg.org/multipage/scripting.html#the-script-element)

  --------------------------------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
  ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
                     Desktop                                                                                                                                                                        Mobile                                                                                                                                                            
  ------------------ ------------------------------------- ------ ------------------------------------ ---------------- ------------------------------------- ------------------------------------- ------------------------------------- ------------------------------------- --------- ------------------------------------- ------------------------------------- -------------------------------------
                     Chrome                                Edge   Firefox                              Internet         Opera                                 Safari                                WebView Android                       Chrome Android                        Firefox   Opera Android                         Safari on IOS                         Samsung Internet
                                                                                                       Explorer                                                                                                                                                                 for                                                                                   
                                                                                                                                                                                                                                                                                Android                                                                               

  `script`           1                                     12     1                                    Yes              ≤12.1                                 3                                     4.4                                   18                                    4         ≤12.1                                 2                                     1.0
                                                                                                                                                                                                                                                                                                                                                                      
                                                                  Starting in Firefox 4, inserting                                                                                                                                                                                                                                                                    
                                                                  \<script\> elements that have been                                                                                                                                                                                                                                                                  
                                                                  created by calling                                                                                                                                                                                                                                                                                  
                                                                  `document.createElement("script")`                                                                                                                                                                                                                                                                  
                                                                  no longer enforces execution in                                                                                                                                                                                                                                                                     
                                                                  insertion order. This change lets                                                                                                                                                                                                                                                                   
                                                                  Firefox properly abide by the                                                                                                                                                                                                                                                                       
                                                                  specification. To make                                                                                                                                                                                                                                                                              
                                                                  script-inserted external scripts                                                                                                                                                                                                                                                                    
                                                                  execute in their insertion order,                                                                                                                                                                                                                                                                   
                                                                  set `.async=false` on them.                                                                                                                                                                                                                                                                         

  `async`            1                                     12     1                                    Yes              15                                    ≤4                                    4.4                                   18                                    4         14                                    ≤3.2                                  1.0

  `attributionsrc`   117                                   117    No                                   No               103                                   No                                    117                                   117                                   No        No                                    No                                    No

  `blocking`         105                                   105    No                                   No               91                                    No                                    105                                   105                                   No        72                                    No                                    20.0

  `crossorigin`      19                                    14     14                                   No               12                                    6                                     4.4                                   25                                    14        12                                    6                                     1.5
                                                                                                                                                                                                                                                                                                                                                                      
                                                                                                                                                              The `crossorigin` attribute was                                                                                                                                   The `crossorigin` attribute was       
                                                                                                                                                              implemented in WebKit in WebKit [bug                                                                                                                              implemented in WebKit in WebKit [bug  
                                                                                                                                                              81438](https://webkit.org/b/81438).                                                                                                                               81438](https://webkit.org/b/81438).   

  `defer`            1                                     12     3.5                                  10               15                                    3                                     4.4                                   18                                    4         14                                    2                                     1.0
                                                                                                                                                                                                                                                                                                                                                                      
                     Chrome does not defer scripts with           Since Firefox 3.6, the `defer`       Before version   Opera does not defer scripts with the                                       Chrome does not defer scripts with    Chrome does not defer scripts with              Opera does not defer scripts with the                                       Samsung Internet does not defer
                     the `defer` attribute when the page          attribute is ignored on scripts that 10, Internet     `defer` attribute when the page is                                          the `defer` attribute when the page   the `defer` attribute when the page             `defer` attribute when the page is                                          scripts with the `defer` attribute
                     is served as XHTML                           don\'t have the `src` attribute.     Explorer         served as XHTML                                                             is served as XHTML                    is served as XHTML                              served as XHTML                                                             when the page is served as XHTML
                     (`application/xhtml+xml`) - [Chromium        However, in Firefox 3.5 even inline  implemented      (`application/xhtml+xml`) - [Chromium                                       (`application/xhtml+xml`) - [Chromium (`application/xhtml+xml`) - [Chromium           (`application/xhtml+xml`) - [Chromium                                       (`application/xhtml+xml`) - [Chromium
                     Issue                                        scripts are deferred if the `defer`  `defer` by a     Issue                                                                       Issue                                 Issue                                           Issue                                                                       Issue
                     #611136](https://crbug.com/611136),          attribute is set.                    proprietary      #611136](https://crbug.com/611136),                                         #611136](https://crbug.com/611136),   #611136](https://crbug.com/611136),             #611136](https://crbug.com/611136),                                         #611136](https://crbug.com/611136),
                     [Chromium Issue                                                                   specification.   [Chromium Issue                                                             [Chromium Issue                       [Chromium Issue                                 [Chromium Issue                                                             [Chromium Issue
                     #874749](https://crbug.com/874749)                                                Since version 10 #874749](https://crbug.com/874749)                                          #874749](https://crbug.com/874749)    #874749](https://crbug.com/874749)              #874749](https://crbug.com/874749)                                          #874749](https://crbug.com/874749)
                                                                                                       it conforms to                                                                                                                                                                                                                                                 
                                                                                                       the W3C                                                                                                                                                                                                                                                        
                                                                                                       specification.                                                                                                                                                                                                                                                 

  `fetchpriority`    101                                   101    No                                   No               No                                    preview                               101                                   101                                   No        70                                    No                                    19.0

  `integrity`        45                                    17     43                                   No               32                                    11.1                                  45                                    45                                    43        No                                    11.3                                  5.0

  `language`         1                                     12     1                                    Yes              15                                    ≤4                                    4.4                                   18                                    4         14                                    ≤3.2                                  1.0

  `nomodule`         61                                    16     60                                   No               48                                    11                                    61                                    61                                    60        45                                    11                                    8.0

  `referrerpolicy`   70                                    ≤79    65                                   No               57                                    14                                    70                                    70                                    65        No                                    14                                    10.0

  `src`              1                                     12     1                                    Yes              15                                    ≤4                                    4.4                                   18                                    4         14                                    ≤3.2                                  1.0

  `text`             1                                     12     1                                    Yes              15                                    ≤4                                    4.4                                   18                                    4         14                                    ≤3.2                                  1.0

  `type`             1                                     12     1                                    Yes              15                                    ≤4                                    4.4                                   18                                    4         14                                    ≤3.2                                  1.0
  ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
:::

## See also {#see_also}

::: section-content
-   [`document.currentScript`](https://developer.mozilla.org/en-US/docs/Web/API/Document/currentScript)
-   [Flavio Copes\' article on loading JavaScript efficiently and
    explaining the differences between `async` and
    `defer`](https://flaviocopes.com/javascript-async-defer/){target="_blank"}
-   [JavaScript
    modules](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules)
    guide
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Element/script](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/script){._attribution-link}
:::
