

# theme-color



::: section-content
The `theme-color` value for the [`name`](../../meta#name) attribute of
the [`<meta>`](../../meta) element indicates a suggested color that user
agents should use to customize the display of the page or of the
surrounding user interface. If specified, the
[`content`](../../meta#content) attribute must contain a valid CSS
[`<color>`](https://developer.mozilla.org/en-US/docs/Web/CSS/color_value).
:::

## Example

::: section-content
::: code-example
[html]{.language-name}

``` {signature="N2Mkht8+FUeDBSnvL0tGBwdP7Kvrjuo2rB+w2bJFR9w=" data-language="html"}
<meta name="theme-color" content="#4285f4" />
```
:::

The following image shows the effect that the [`<meta>`](../../meta)
element above will have on a document displayed in Chrome running on an
Android mobile device.

![Image showing the effect of using
theme-color](Image showing the effect of using.png){width="894"
height="686" loading="lazy"}

*Image credit: from [Icons & Browser
Colors](https://web.dev/articles/icons-and-browser-colors){target="_blank"},
created and shared by Google and used according to terms described in
the [Creative Commons 4.0 Attribution
License](https://creativecommons.org/licenses/by/4.0/){target="_blank"}.*

You can provide a media type or query inside the
[`media`](../../meta#media) attribute; the color will then only be set
if the media condition is true. For example:

::: code-example
[html]{.language-name}

``` {signature="PsBucUxCp6vJwg81ZVvLCvWgVsx2YPBJVG790YclcRY=" data-language="html"}
<meta name="theme-color" media="(prefers-color-scheme: light)" content="cyan" />
<meta name="theme-color" media="(prefers-color-scheme: dark)" content="black" />
```
:::
:::

## Specifications

::: _table
  ----------------------------------------------------------------------------------------------------
  Specification
  ----------------------------------------------------------------------------------------------------
  [HTML Standard\
  [\#
  meta-theme-color]{.small}](https://html.spec.whatwg.org/multipage/semantics.html#meta-theme-color)

  ----------------------------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
  ----------------------------------------------------------------------------------------------------------------------------------------------
                  Desktop                                                           Mobile                                            
  --------------- ------------- ------------- --------- ---------- ------- -------- --------- ---------- --------- --------- -------- ----------
                  Chrome        Edge          Firefox   Internet   Opera   Safari   WebView   Chrome     Firefox   Opera     Safari   Samsung
                                                        Explorer                    Android   Android    for       Android   on IOS   Internet
                                                                                                         Android                      

  `theme-color`   73            79            No        No         No      15       No        80         No        No        15       6.2
                                                                                                                                      
                  Chrome uses   Edge uses the                                                 Chrome for                              
                  the color     color only on                                                 Android                                 
                  only on       installed                                                     does not                                
                  installed     progressive                                                   use the                                 
                  progressive   web apps.                                                     color on                                
                  web apps.                                                                   devices                                 
                                                                                              with                                    
                  39--72                                                                      native                                  
                                                                                              dark mode                               
                  Chrome                                                                      enabled.                                
                  reports                                                                                                             
                  support, but                                                                                                        
                  does not                                                                                                            
                  actually use                                                                                                        
                  the color                                                                                                           
                  anywhere.                                                                                                           
  ----------------------------------------------------------------------------------------------------------------------------------------------
:::

## See also {#see_also}

::: section-content
-   [`color-scheme`](https://developer.mozilla.org/en-US/docs/Web/CSS/color-scheme)
    CSS property
-   [`prefers-color-scheme`](https://developer.mozilla.org/en-US/docs/Web/CSS/@media/prefers-color-scheme)
    media query
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Element/meta/name/theme-color](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/meta/name/theme-color){._attribution-link}
:::
