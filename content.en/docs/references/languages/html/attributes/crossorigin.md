

# HTML attribute: crossorigin



::: section-content
The `crossorigin` attribute, valid on the [`<audio>`](../element/audio),
[`<img>`](../element/img), [`<link>`](../element/link),
[`<script>`](../element/script), and [`<video>`](../element/video)
elements, provides support for
[CORS](https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS), defining
how the element handles cross-origin requests, thereby enabling the
configuration of the CORS requests for the element\'s fetched data.
Depending on the element, the attribute can be a CORS settings
attribute.

The `crossorigin` content attribute on media elements is a CORS settings
attribute.

These attributes are
[enumerated](https://developer.mozilla.org/en-US/docs/Glossary/Enumerated),
and have the following possible values:

[`anonymous`](#anonymous)

:   Request uses CORS headers and credentials flag is set to
    `'same-origin'`. There is no exchange of **user credentials** via
    cookies, client-side TLS certificates or HTTP authentication, unless
    destination is the same origin.

[`use-credentials`](#use-credentials)

:   Request uses CORS headers, credentials flag is set to `'include'`
    and **user credentials** are always included.

[`""`](#sect1)

:   Setting the attribute name to an empty value, like `crossorigin` or
    `crossorigin=""`, is the same as `anonymous`.

An invalid keyword and an empty string will be handled as the
`anonymous` keyword.

By default (that is, when the attribute is not specified), CORS is not
used at all. The user agent will not ask for permission for full access
to the resource and in the case of a cross-origin request, certain
limitations will be applied based on the type of element concerned:

<figure class="table-container">
<div class="_table">
<table class="no-markdown">
<tbody>
<tr class="header">
<th class="header">Element</th>
<th class="header">Restrictions</th>
</tr>

<tr class="odd">
<td><code>img</code>, <code>audio</code>, <code>video</code></td>
<td>When resource is placed in <a
href="../element/canvas"><code>&lt;canvas&gt;</code></a>, element is
marked as <a
href="../cors_enabled_image#security_and_tainted_canvases"><em>tainted</em></a>.</td>
</tr>
<tr class="even">
<td><code>script</code></td>
<td>Access to error logging via <a
href="https://developer.mozilla.org/en-US/docs/Web/API/Window/error_event"><code>window.onerror</code></a>
will be limited.</td>
</tr>
<tr class="odd">
<td><code>link</code></td>
<td>Request with no appropriate <code>crossorigin</code> header may be
discarded.</td>
</tr>
</tbody>
</table>

</figure>

::: {#sect2 .notecard .note}
**Note:** The `crossorigin` attribute is not supported for
[`rel="icon"`](rel#icon) in Chromium-based browsers. See the [open
Chromium issue](https://crbug.com/1121645){target="_blank"}.
:::
:::

### Example: `crossorigin` with the `<script>` element {#example_crossorigin_with_the_script_element}

::: section-content
You can use the following [`<script>`](../element/script) element to
tell a browser to execute the `https://example.com/example-framework.js`
script without sending user-credentials.

::: code-example
[html]{.language-name}

``` {signature="gmqRYTcssVuwG1FefnItqBu/UE7w3Jg+n1G/xD9L18g=" data-language="html"}
<script
  src="https://example.com/example-framework.js"
  crossorigin="anonymous"></script>
```
:::
:::

### Example: Web manifest with credentials {#example_web_manifest_with_credentials}

::: section-content
The `use-credentials` value must be used when fetching a
[manifest](https://developer.mozilla.org/en-US/docs/Web/Manifest) that
requires credentials, even if the file is from the same origin.

::: code-example
[html]{.language-name}

``` {signature="qUcPtbg+8FhpveA2KUhgWKnN9kHckcDS7x8ZhcAtFJA=" data-language="html"}
<link rel="manifest" href="/app.webmanifest" crossorigin="use-credentials" />
```
:::
:::

## Specifications

::: _table
  ----------------------------------------------------------------------------------------------------------------------------
  Specification
  ----------------------------------------------------------------------------------------------------------------------------
  [HTML Standard\
  [\#
  cors-settings-attributes]{.small}](https://html.spec.whatwg.org/multipage/urls-and-fetching.html#cors-settings-attributes)

  ----------------------------------------------------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
  --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
                  Desktop                                                                             Mobile                                                                        
  --------------- --------- ------ -------------------------------------- ---------- ------- -------- --------- --------- -------------------------------------- --------- -------- ----------
                  Chrome    Edge   Firefox                                Internet   Opera   Safari   WebView   Chrome    Firefox for Android                    Opera     Safari   Samsung
                                                                          Explorer                    Android   Android                                          Android   on IOS   Internet

  `crossorigin`   33        ≤18    74                                     No         20      10       4.4.3     33        79                                     20        10       2.0
                                                                                                                                                                                    
                                   12--74                                                                                 14--79                                                    
                                                                                                                                                                                    
                                   With `crossorigin="use-credentials"`,                                                  With `crossorigin="use-credentials"`,                     
                                   cookies aren\'t sent during seek. See                                                  cookies aren\'t sent during seek. See                     
                                   [bug                                                                                   [bug                                                      
                                   1532722](https://bugzil.la/1532722).                                                   1532722](https://bugzil.la/1532722).                      
  --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
:::

::: _table
  --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
                  Desktop                                                                             Mobile                                                                        
  --------------- --------- ------ --------- ---------- ------- ------------------------------------- --------- --------- --------- --------- ------------------------------------- ----------
                  Chrome    Edge   Firefox   Internet   Opera   Safari                                WebView   Chrome    Firefox   Opera     Safari on IOS                         Samsung
                                             Explorer                                                 Android   Android   for       Android                                         Internet
                                                                                                                          Android                                                   

  `crossorigin`   19        14     14        No         12      6                                     4.4       25        14        12        6                                     1.5
                                                                                                                                                                                    
                                                                The `crossorigin` attribute was                                               The `crossorigin` attribute was       
                                                                implemented in WebKit in WebKit [bug                                          implemented in WebKit in WebKit [bug  
                                                                81438](https://webkit.org/b/81438).                                           81438](https://webkit.org/b/81438).   
  --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
:::

::: _table
  ----------------------------------------------------------------------------------------------------------------------------------------------
                  Desktop                                                      Mobile                                                 
  --------------- --------- ------ --------------- ---------- ------- -------- --------- --------- --------------- --------- -------- ----------
                  Chrome    Edge   Firefox         Internet   Opera   Safari   WebView   Chrome    Firefox for     Opera     Safari   Samsung
                                                   Explorer                    Android   Android   Android         Android   on IOS   Internet

  `crossorigin`   34        17     18              No         21      10       37        34        18              21        10       2.0
                                                                                                                                      
                                   Before Firefox                                                  Before Firefox                     
                                   83,                                                             83,                                
                                   `crossorigin`                                                   `crossorigin`                      
                                   is not                                                          is not                             
                                   supported for                                                   supported for                      
                                   `rel="icon"`.                                                   `rel="icon"`.                      
  ----------------------------------------------------------------------------------------------------------------------------------------------
:::

::: _table
                  Desktop                                                         Mobile                                                                                   
  --------------- --------- ------ --------- ------------------- ------- -------- ----------------- ---------------- --------------------- --------------- --------------- ------------------
                  Chrome    Edge   Firefox   Internet Explorer   Opera   Safari   WebView Android   Chrome Android   Firefox for Android   Opera Android   Safari on IOS   Samsung Internet
  `crossorigin`   13        12     8         Yes                 15      6        4.4               18               8                     14              6               1.0
:::

### html.elements.img.crossorigin

BCD tables only load in the browser with JavaScript enabled. Enable
JavaScript to view data.

### html.elements.link.crossorigin

BCD tables only load in the browser with JavaScript enabled. Enable
JavaScript to view data.

### html.elements.script.crossorigin

BCD tables only load in the browser with JavaScript enabled. Enable
JavaScript to view data.

### html.elements.video.crossorigin

BCD tables only load in the browser with JavaScript enabled. Enable
JavaScript to view data.

## See also {#see_also}

::: section-content
-   [Cross-Origin Resource Sharing
    (CORS)](https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS)
-   [HTML attribute: `rel`](rel)
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes/crossorigin](https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes/crossorigin){._attribution-link}
:::
