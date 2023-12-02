

# \<script\>: type attribute



::: section-content
The `type` attribute of the [`<script>`](../script) element indicates
the *type* of script represented by the element: a classic script, an
import map, a JavaScript module, speculation rules, or a data block.
:::

## Value

::: section-content
The value of this attribute indicates the type of data represented by
the script, and will be one of the following:

[**Attribute is not set (default), an empty string, or a JavaScript MIME type**](#attribute_is_not_set_default_an_empty_string_or_a_javascript_mime_type)

:   Indicates that the script is a \"classic script\", containing
    JavaScript code. Authors are encouraged to omit the attribute if the
    script refers to JavaScript code rather than specify a MIME type.
    JavaScript MIME types are [listed in the IANA media types
    specification](https://developer.mozilla.org/en-US/docs/Web/HTTP/Basics_of_HTTP/MIME_types#textjavascript).

[`importmap`](type/importmap)

:   This value indicates that the body of the element contains an import
    map. The import map is a JSON object that developers can use to
    control how the browser resolves module specifiers when importing
    [JavaScript
    modules](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules#importing_modules_using_import_maps).

[`module`](#module)

:   This value causes the code to be treated as a JavaScript module. The
    processing of the script contents is deferred. The `charset` and
    `defer` attributes have no effect. For information on using
    `module`, see our [JavaScript
    modules](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules)
    guide. Unlike classic scripts, module scripts require the use of the
    CORS protocol for cross-origin fetching.

[`speculationrules`](type/speculationrules) [Experimental]{.visually-hidden}

:   This value indicates that the body of the element contains
    speculation rules. Speculation rules take the form of a JSON object
    that determine what resources should be prefetched or prerendered by
    the browser. This is part of the [speculation rules
    API](https://developer.mozilla.org/en-US/docs/Web/Performance/Speculative_loading#the_speculation_rules_api).

[**Any other value**](#any_other_value)

:   The embedded content is treated as a data block, and won\'t be
    processed by the browser. Developers must use a valid MIME type that
    is not a JavaScript MIME type to denote data blocks. All of the
    other attributes will be ignored, including the `src` attribute.

::: {#sect1 .notecard .note}
**Note:** In earlier browsers, the type identified the scripting
language of the embedded or imported (via the `src` attribute) code.
:::
:::

## Specifications

::: {.notecard .warning}
**No specification found**

No specification data found for `html.elements.script.type`.\
[Check for problems with this page](#on-github) or contribute a missing
`spec_url` to
[mdn/browser-compat-data](https://github.com/mdn/browser-compat-data).
Also make sure the specification is included in
[w3c/browser-specs](https://github.com/w3c/browser-specs).
:::

## Browser compatibility {#browser_compatibility}

::: _table
  --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
                       Desktop                                                                                                                                                          Mobile                                                                                                                                                
  -------------------- ------------------------------------ ------------------------------------ --------- ---------- ------------------------------------ ---------------------------- ------------------------------------ ------------------------------------ --------- ------------------------------------ ---------------------------- ------------------------------------
                       Chrome                               Edge                                 Firefox   Internet   Opera                                Safari                       WebView Android                      Chrome Android                       Firefox   Opera Android                        Safari on IOS                Samsung Internet
                                                                                                           Explorer                                                                                                                                               for                                                                         
                                                                                                                                                                                                                                                                  Android                                                                     

  `type`               1                                    12                                   1         Yes        15                                   ≤4                           4.4                                  18                                   4         14                                   ≤3.2                         1.0

  `importmap`          89                                   89                                   108       No         75                                   16.4                         89                                   89                                   108       63                                   16.4                         15.0

  `module`             61                                   79                                   60        No         48                                   10.1                         61                                   61                                   60        45                                   10.3                         8.0
                                                                                                                                                                                                                                                                                                                                              
                       Module scripts without the `async`   Module scripts without the `async`                        Module scripts without the `async`   Module scripts do not load   Module scripts without the `async`   Module scripts without the `async`             Module scripts without the `async`   Module scripts do not load   Module scripts without the `async`
                       attribute do not load when the page  attribute do not load when the page                       attribute do not load when the page  when the page is served as   attribute do not load when the page  attribute do not load when the page            attribute do not load when the page  when the page is served as   attribute do not load when the page
                       is served as XHTML                   is served as XHTML                                        is served as XHTML                   XHTML                        is served as XHTML                   is served as XHTML                             is served as XHTML                   XHTML                        is served as XHTML
                       (`application/xhtml+xml`). See [bug  (`application/xhtml+xml`). See [bug                       (`application/xhtml+xml`). See [bug  (`application/xhtml+xml`).   (`application/xhtml+xml`). See [bug  (`application/xhtml+xml`). See [bug            (`application/xhtml+xml`). See [bug  (`application/xhtml+xml`).   (`application/xhtml+xml`). See [bug
                       717643](https://crbug.com/717643).   717643](https://crbug.com/717643).                        717643](https://crbug.com/717643).                                717643](https://crbug.com/717643).   717643](https://crbug.com/717643).             717643](https://crbug.com/717643).                                717643](https://crbug.com/717643).
                                                                                                                                                                                                                                                                                                                                              
                                                            16--79                                                                                                                                                                                                                                                                            

  `speculationrules`   109                                  109                                  No        No         95                                   No                           109                                  109                                  No        74                                   No                           21.0
                                                                                                                                                                                                                                                                                                                                              
                       105                                  105                                                       91                                                                103                                  103                                            71                                                                20.0
                                                                                                                                                                                                                                                                                                                                              
                       Initial support included same-origin Initial support included same-origin                      Initial support included same-origin                              Initial support included same-origin Initial support included same-origin           Initial support included same-origin                              Initial support included same-origin
                       prerendering only.                   prerendering only.                                        prerendering only.                                                prerendering only.                   prerendering only.                             prerendering only.                                                prerendering only.
  --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Element/script/type](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/script/type){._attribution-link}
:::
