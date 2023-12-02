

# rel=noopener



::: section-content
The `noopener` keyword for the [`rel`](../rel) attribute of the
[`<a>`](../../element/a), [`<area>`](../../element/area), and
[`<form>`](../../element/form) elements instructs the browser to
navigate to the target resource without granting the new browsing
context access to the document that opened it --- by not setting the
[`Window.opener`](https://developer.mozilla.org/en-US/docs/Web/API/Window/opener)
property on the opened window (it returns `null`).

This is especially useful when opening untrusted links, in order to
ensure they cannot tamper with the originating document via the
[`Window.opener`](https://developer.mozilla.org/en-US/docs/Web/API/Window/opener)
property (see [About
rel=noopener](https://mathiasbynens.github.io/rel-noopener/){target="_blank"}
for more details), while still providing the `Referer` HTTP header
(unless `noreferrer` is used as well).

Note that when `noopener` is used, nonempty target names other than
`_top`, `_self`, and `_parent` are all treated like `_blank` in terms of
deciding whether to open a new window/tab.

::: {#sect1 .notecard .note}
**Note:** Setting `target="_blank"` on `<a>` elements now implicitly
provides the same `rel` behavior as setting `rel="noopener"` which does
not set `window.opener`. See [browser
compatibility](../../element/a#browser_compatibility) for support
status.
:::
:::

## Specifications

::: _table
  ----------------------------------------------------------------------------------------------------
  Specification
  ----------------------------------------------------------------------------------------------------
  [HTML Standard\
  [\#
  link-type-noopener]{.small}](https://html.spec.whatwg.org/multipage/links.html#link-type-noopener)

  ----------------------------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
  -------------------------------------------------------------------------------------------------------------------------------------------------
               Desktop                                                         Mobile                                                    
  ------------ --------- ------ ------------------ ---------- ------- -------- --------- --------- ------------------ --------- -------- ----------
               Chrome    Edge   Firefox            Internet   Opera   Safari   WebView   Chrome    Firefox for        Opera     Safari   Samsung
                                                   Explorer                    Android   Android   Android            Android   on IOS   Internet

  `noopener`   49        79     52                 No         36      10.1     49        49        52                 36        10.3     5.0
                                                                                                                                         
                                Before Firefox 63,                                                 Before Firefox 63,                    
                                `rel="noopener"`                                                   `rel="noopener"`                      
                                created windows                                                    created windows                       
                                with all features                                                  with all features                     
                                disabled by                                                        disabled by                           
                                default. Starting                                                  default. Starting                     
                                with Firefox 63,                                                   with Firefox 63,                      
                                these windows have                                                 these windows have                    
                                the same features                                                  the same features                     
                                enabled by default                                                 enabled by default                    
                                as any other                                                       as any other                          
                                window.                                                            window.                               
  -------------------------------------------------------------------------------------------------------------------------------------------------
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes/rel/noopener](https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes/rel/noopener){._attribution-link}
:::
