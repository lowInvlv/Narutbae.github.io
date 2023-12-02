

# rel=noreferrer



::: section-content
The `noreferrer` keyword for the [`rel`](../rel) attribute of the
[`<a>`](../../element/a), [`<area>`](../../element/area), and
[`<form>`](../../element/form) elements instructs the browser, when
navigating to the target resource, to omit the
[`Referer`](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Referer)
header and otherwise leak no referrer information --- and additionally
to behave as if the [`noopener`](noopener) keyword were also specified.
:::

## Specifications

::: _table
  --------------------------------------------------------------------------------------------------------
  Specification
  --------------------------------------------------------------------------------------------------------
  [HTML Standard\
  [\#
  link-type-noreferrer]{.small}](https://html.spec.whatwg.org/multipage/links.html#link-type-noreferrer)

  --------------------------------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
  --------------------------------------------------------------------------------------------------------------------------------------
                 Desktop                                                     Mobile                                           
  -------------- --------- ------ --------- --------------- ------- -------- --------- --------- --------- --------- -------- ----------
                 Chrome    Edge   Firefox   Internet        Opera   Safari   WebView   Chrome    Firefox   Opera     Safari   Samsung
                                            Explorer                         Android   Android   for       Android   on IOS   Internet
                                                                                                 Android                      

  `noreferrer`   16        13     33        11              15      5        4.4       18        33        14        4.2      1.5
                                                                                                                              
                                            Only supported                                                                    
                                            in IE11 in                                                                        
                                            later versions                                                                    
                                            of Windows 10                                                                     
                                            (creators                                                                         
                                            update). (Per                                                                     
                                            caniuse.com.)                                                                     
  --------------------------------------------------------------------------------------------------------------------------------------
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes/rel/noreferrer](https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes/rel/noreferrer){._attribution-link}
:::
