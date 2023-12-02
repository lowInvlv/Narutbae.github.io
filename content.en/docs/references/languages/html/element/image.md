

# \<image\>: The Image element



::: section-content
::: {#sect1 .notecard .deprecated}
**Deprecated:** This feature is no longer recommended. Though some
browsers might still support it, it may have already been removed from
the relevant web standards, may be in the process of being dropped, or
may only be kept for compatibility purposes. Avoid using it, and update
existing code if possible; see the [compatibility
table](#browser_compatibility) at the bottom of this page to guide your
decision. Be aware that this feature may cease to work at any time.
:::

::: {#sect2 .notecard .nonstandard}
**Non-standard:** This feature is non-standard and is not on a standards
track. Do not use it on production sites facing the Web: it will not
work for every user. There may also be large incompatibilities between
implementations and the behavior may change in the future.
:::

The `<image>` [HTML](../index) element is an ancient and poorly
supported precursor to the [`<img>`](img) element. **It should not be
used**.

Some browsers will attempt to automatically convert this into an
[`<img>`](img) element, and may succeed if the [`src`](img#src)
attribute is specified as well.
:::

## Specifications

::: section-content
This does not appear to have been part of any formal specification. It
was mentioned in [HTML+ Discussion Document - Dave Raggett, November 8,
1993](https://www.w3.org/MarkUp/HTMLPlus/htmlplus_21.html){target="_blank"}
(Section 5.9 - Images), but was not part of the first revision of
[HyperText Markup Language Specification -
2.0](https://datatracker.ietf.org/doc/html/draft-ietf-html-spec-00){target="_blank"}
in 1994.
:::

## Browser compatibility {#browser_compatibility}

::: _table
  ------------------------------------------------------------------------------------------------------------------------------------------------
            Desktop                                                          Mobile                                                     
  --------- --------- ------ ------------------- ---------- ------- -------- --------- --------- ------------------- --------- -------- ----------
            Chrome    Edge   Firefox             Internet   Opera   Safari   WebView   Chrome    Firefox for Android Opera     Safari   Samsung
                                                 Explorer                    Android   Android                       Android   on IOS   Internet

  `image`   1         79     1                   No         15      1        4.4       18        4                   14        1        1.0
                                                                                                                                        
                             Before Firefox 22,                                                  Before Firefox 22,                     
                             creating an                                                         creating an                            
                             \<image\> element                                                   \<image\> element                      
                             incorrectly                                                         incorrectly                            
                             resulted in an                                                      resulted in an                         
                             `HTMLSpanElement`                                                   `HTMLSpanElement`                      
                             object, instead of                                                  object, instead of                     
                             the expected                                                        the expected                           
                             `HTMLElement`.                                                      `HTMLElement`.                         
  ------------------------------------------------------------------------------------------------------------------------------------------------
:::

## See also {#see_also}

::: section-content
-   [`<img>`](img): The correct way to display an image in a document
-   [`<picture>`](picture): A more powerful correct way to display an
    image in a document
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Element/image](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/image){._attribution-link}
:::
