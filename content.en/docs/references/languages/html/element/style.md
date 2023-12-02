

# \<style\>: The Style Information element



::: section-content
The `<style>` [HTML](../index) element contains style information for a
document, or part of a document. It contains CSS, which is applied to
the contents of the document containing the `<style>` element.
:::

## Try it {#try_it}

::: section-content
::: iframe
::: {.output-header .border-rounded-top}
#### HTML Demo: \<style\> {#html-demo-style .output-heading}

Reset
:::

::: {#warning-no-script .warning-container}
::: warning
The interactive example cannot be shown because JavaScript is disabled.
:::
:::

::: {#warning-mathml-not-supported .warning-container .hidden}
::: warning
The interactive example cannot be shown because MathML is not supported
by your browser.
:::
:::

::: {#editor-container .editor-container .tabbed-standard .hidden .border-rounded-bottom editor-type="tabbed"}
::: {#tab-container .section .tabs}
::: {#tablist .tab-list role="tablist"}
HTML

CSS

JavaScript
:::

::: {#html-panel .section .hidden tabindex="0" role="tabpanel" aria-labelledby="html" aria-hidden="true"}
::: {#html-editor}
    <style>
      p {
        color: #26b72b;
      }
    </style>

    <p>This text will be green. Inline styles take precedence over CSS included externally.</p>

    <p style="color: blue">The <code>style</code> attribute can override it, though.</p>
:::
:::

::: {#css-panel .section .hidden tabindex="0" role="tabpanel" aria-labelledby="css" aria-hidden="true"}
::: {#css-editor}
    p {
      color: #f00;
    }
:::
:::

::: {#js-panel .section .hidden tabindex="0" role="tabpanel" aria-labelledby="js" aria-hidden="true"}
::: {#js-editor}
:::
:::
:::

::: {#output .output-container}
#### Output {.output-label}
:::
:::

::: {.section .console-container .hidden aria-hidden="true"}
#### Console Output {#console-output .console-label}

![]
clear console

::: {#console .console}
:::
:::

::: {#html-output .output .editor-tabbed}
%html-content%
:::
:::

The `<style>` element must be included inside the [`<head>`](head) of
the document. In general, it is better to put your styles in external
stylesheets and apply them using [`<link>`](link) elements.

If you include multiple `<style>` and `<link>` elements in your
document, they will be applied to the DOM in the order they are included
in the document --- make sure you include them in the correct order, to
avoid unexpected cascade issues.

In the same manner as `<link>` elements, `<style>` elements can include
`media` attributes that contain [media
queries](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_media_queries),
allowing you to selectively apply internal stylesheets to your document
depending on media features such as viewport width.
:::

## Attributes

::: section-content
This element includes the [global attributes](../global_attributes).

[`blocking`](#blocking) [Experimental]{.visually-hidden}

:   This attribute explicitly indicates that certain operations should
    be blocked on the fetching of critical subresources.
    [`@import`](https://developer.mozilla.org/en-US/docs/Web/CSS/@import)-ed
    stylesheets are generally considered as critical subresources,
    whereas
    [`background-image`](https://developer.mozilla.org/en-US/docs/Web/CSS/background-image)
    and fonts are not.

    -   `render`: The rendering of content on the screen is blocked.

[`media`](#media)

:   This attribute defines which media the style should be applied to.
    Its value is a [media
    query](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_media_queries/Using_media_queries),
    which defaults to `all` if the attribute is missing.

[`nonce`](#nonce)

:   A cryptographic nonce (number used once) used to allow inline styles
    in a [style-src
    Content-Security-Policy](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Security-Policy/style-src).
    The server must generate a unique nonce value each time it transmits
    a policy. It is critical to provide a nonce that cannot be guessed
    as bypassing a resource\'s policy is otherwise trivial.

[`title`](#title)

:   This attribute specifies [alternative style
    sheet](https://developer.mozilla.org/en-US/docs/Web/CSS/Alternative_style_sheets)
    sets.
:::

### Deprecated attributes {#deprecated_attributes}

::: section-content

[`type`](#type) [Deprecated]{.visually-hidden}

:   This attribute should not be provided: if it is, the only permitted
    values are the empty string or a case-insensitive match for
    `text/css`.
:::

## Examples

### A simple stylesheet {#a_simple_stylesheet}

::: section-content
In the following example, we apply a very simple stylesheet to a
document:

::: code-example
[html]{.language-name}

``` {signature="Xp1eBLnbRbAAjqyTCFNTrBNTWck3M+5AxtWVn52AbH8=" data-language="html"}
<!doctype html>
<html lang="en-US">
  <head>
    <meta charset="UTF-8" />
    <title>Test page</title>
    <style>
      p {
        color: red;
      }
    </style>
  </head>
  <body>
    <p>This is my paragraph.</p>
  </body>
</html>
```
:::

#### Result

::: {#sect1 .code-example}
::: iframe
:::
:::
:::

### Multiple style elements {#multiple_style_elements}

::: section-content
In this example we\'ve included two `<style>` elements --- notice how
the conflicting declarations in the later `<style>` element override
those in the earlier one, if they have equal
[specificity](https://developer.mozilla.org/en-US/docs/Web/CSS/Specificity).

::: code-example
[html]{.language-name}

``` {signature="HUSNAFh8BZIdBF/hp4GoX4t+HEJOnqLW1Khlt/2VJ14=" data-language="html"}
<!doctype html>
<html lang="en-US">
  <head>
    <meta charset="UTF-8" />
    <title>Test page</title>
    <style>
      p {
        color: white;
        background-color: blue;
        padding: 5px;
        border: 1px solid black;
      }
    </style>
    <style>
      p {
        color: blue;
        background-color: yellow;
      }
    </style>
  </head>
  <body>
    <p>This is my paragraph.</p>
  </body>
</html>
```
:::

#### Result {#result_2}

::: {#sect2 .code-example}
::: iframe
:::
:::
:::

### Including a media query {#including_a_media_query}

::: section-content
In this example we build on the previous one, including a `media`
attribute on the second `<style>` element so it is only applied when the
viewport is less than 500px in width.

::: code-example
[html]{.language-name}

``` {signature="2vvFiULEGiSNCyiwFEbxjnlPzEVZXl/xwEfDs7YycdQ=" data-language="html"}
<!doctype html>
<html lang="en-US">
  <head>
    <meta charset="UTF-8" />
    <title>Test page</title>
    <style>
      p {
        color: white;
        background-color: blue;
        padding: 5px;
        border: 1px solid black;
      }
    </style>
    <style media="all and (max-width: 500px)">
      p {
        color: blue;
        background-color: yellow;
      }
    </style>
  </head>
  <body>
    <p>This is my paragraph.</p>
  </body>
</html>
```
:::

#### Result {#result_3}

::: {#sect3 .code-example}
::: iframe
:::
:::
:::

## Technical summary {#technical_summary}

::: section-content
<figure class="table-container">
<div class="_table">
<table class="properties">
<tbody>
<tr class="odd">
<th><a href="../content_categories">Content categories</a></th>
<td><a href="../content_categories#metadata_content">Metadata
content</a>, and if the <code>scoped</code> attribute is present: <a
href="../content_categories#flow_content">flow content</a>.</td>
</tr>
<tr class="even">
<th>Permitted content</th>
<td>Text content matching the <code>type</code> attribute, that is
<code>text/css</code>.</td>
</tr>
<tr class="odd">
<th>Tag omission</th>
<td>Neither tag is omissible.</td>
</tr>
<tr class="even">
<th>Permitted parents</th>
<td>Any element that accepts <a
href="../content_categories#metadata_content">metadata content</a>.</td>
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
<th>DOM interface</th>
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLStyleElement"><code>HTMLStyleElement</code></a></td>
</tr>
</tbody>
</table>

</figure>
:::

## Specifications

::: _table
  ------------------------------------------------------------------------------------------------------
  Specification
  ------------------------------------------------------------------------------------------------------
  [HTML Standard\
  [\#
  the-style-element]{.small}](https://html.spec.whatwg.org/multipage/semantics.html#the-style-element)

  ------------------------------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
  -------------------------------------------------------------------------------------------------------------------------------------
               Desktop                                                      Mobile                                           
  ------------ --------- ------ --------------- ---------- ------- -------- --------- --------- --------- --------- -------- ----------
               Chrome    Edge   Firefox         Internet   Opera   Safari   WebView   Chrome    Firefox   Opera     Safari   Samsung
                                                Explorer                    Android   Android   for       Android   on IOS   Internet
                                                                                                Android                      

  `style`      1         12     1               3          3.5     1        4.4       18        4         10.1      1        1.0

  `blocking`   105       105    No              No         91      No       105       105       No        72        No       20.0

  `media`      1         12     1               3          3.5     1        4.4       18        4         10.1      1        1.0

  `title`      1         12     1               3          3.5     1        4.4       18        4         10.1      1        1.0

  `type`       1         12     1               3          3.5     1        4.4       18        4         10.1      1        1.0
                                                                                                                             
                                Before 75,                                                                                   
                                Firefox                                                                                      
                                accepted any                                                                                 
                                CSS media                                                                                    
                                (MIME) type,                                                                                 
                                with optional                                                                                
                                parameters.                                                                                  
                                Starting in 75,                                                                              
                                this has been                                                                                
                                restricted to                                                                                
                                the string                                                                                   
                                \'text/css\',                                                                                
                                per the spec.                                                                                
  -------------------------------------------------------------------------------------------------------------------------------------
:::

## See also {#see_also}

::: section-content
-   The [`<link>`](link) element, which allows us to apply external
    stylesheets to a document.
-   [Alternative Style
    Sheets](https://developer.mozilla.org/en-US/docs/Web/CSS/Alternative_style_sheets)
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Element/style](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/style){._attribution-link}
:::
