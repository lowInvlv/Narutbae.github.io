

# rel=preconnect



::: section-content
The `preconnect` keyword for the [`rel`](../../element/link#rel)
attribute of the [`<link>`](../../element/link) element is a hint to
browsers that the user is likely to need resources from the target
resource\'s origin, and therefore the browser can likely improve the
user experience by preemptively initiating a connection to that origin.
Preconnecting speeds up future loads from a given origin by preemptively
performing part or all of the handshake (DNS+TCP for HTTP, and
DNS+TCP+TLS for HTTPS origins).

`<link rel="preconnect">` will provide a benefit to any future
cross-origin HTTP request, navigation or subresource. It has no benefit
on same-origin requests because the connection is already open.

If a page needs to make connections to many third-party domains,
preconnecting them all can be counterproductive. The
`<link rel="preconnect">` hint is best used for only the most critical
connections. For the others, just use
[`<link rel="dns-prefetch">`](dns-prefetch) to save time on the first
step --- the DNS lookup.
:::

## Examples

::: section-content
::: code-example
[html]{.language-name}

``` {signature="PYT4/2ue7hu0mrX90lIY7QK5OYVdsVtH/UE3L5jMOuA=" data-language="html"}
<link rel="preconnect" href="https://example.com" />
```
:::

You can also implement preconnect as an HTTP
[Link](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Link)
header, for example:

::: code-example
[http]{.language-name}

``` {signature="U963iZTksn1xospr3idfnUb+T9AbbIbtg/1wWsgVgiE=" data-language="http"}
Link: <https://example.com>; rel="preconnect"
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
  link-type-preconnect]{.small}](https://html.spec.whatwg.org/multipage/links.html#link-type-preconnect)

  --------------------------------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
  ---------------------------------------------------------------------------------------------------------------------------------------------
                 Desktop                                                      Mobile                                                 
  -------------- --------- ------ --------------- ---------- ------- -------- --------- --------- --------------- --------- -------- ----------
                 Chrome    Edge   Firefox         Internet   Opera   Safari   WebView   Chrome    Firefox for     Opera     Safari   Samsung
                                                  Explorer                    Android   Android   Android         Android   on IOS   Internet

  `preconnect`   46        79     39              No         33      11.1     46        46        39              33        11.3     4.0
                                                                                                                                     
                                  Before Firefox                                                  Before Firefox                     
                                  41, it doesn\'t                                                 41, it doesn\'t                    
                                  obey the                                                        obey the                           
                                  `crossorigin`                                                   `crossorigin`                      
                                  attribute.                                                      attribute.                         
  ---------------------------------------------------------------------------------------------------------------------------------------------
:::

## See also {#see_also}

::: section-content
-   [Speculative
    loading](https://developer.mozilla.org/en-US/docs/Web/Performance/Speculative_loading)
    for a comparison of `<link rel="preconnect">` and other similar
    performance improvement features.
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes/rel/preconnect](https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes/rel/preconnect){._attribution-link}
:::
