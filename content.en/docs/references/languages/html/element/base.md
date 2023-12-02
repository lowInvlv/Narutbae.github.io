

# \<base\>: The Document Base URL element



::: section-content
The `<base>` [HTML](../index) element specifies the base URL to use for
all *relative* URLs in a document. There can be only one `<base>`
element in a document.

A document\'s used base URL can be accessed by scripts with
[`Node.baseURI`](https://developer.mozilla.org/en-US/docs/Web/API/Node/baseURI).
If the document has no `<base>` elements, then `baseURI` defaults to
[`location.href`](https://developer.mozilla.org/en-US/docs/Web/API/Location/href).

<figure class="table-container">
<div class="_table">
<table class="properties">
<tbody>
<tr class="odd">
<th scope="row"><a href="../content_categories">Content
categories</a></th>
<td>Metadata content.</td>
</tr>
<tr class="even">
<th scope="row">Permitted content</th>
<td>None; it is a <a
href="https://developer.mozilla.org/en-US/docs/Glossary/Void_element">void
element</a>.</td>
</tr>
<tr class="odd">
<th scope="row">Tag omission</th>
<td>There must be no closing tag.</td>
</tr>
<tr class="even">
<th scope="row">Permitted parents</th>
<td>A <a href="head"><code>&lt;head&gt;</code></a> that doesn't contain
another <a href="base" aria-current="page"><code>&lt;base&gt;</code></a>
element.</td>
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
href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLBaseElement"><code>HTMLBaseElement</code></a></td>
</tr>
</tbody>
</table>

</figure>
:::

## Attributes

::: section-content
This element\'s attributes include the [global
attributes](../global_attributes).

::: {#sect1 .notecard .warning}
**Warning:** If either of the following attributes are specified, this
element **must** come before other elements with attribute values of
URLs, such as [`<link>`](link)\'s `href` attribute.
:::

[`href`](#href)

:   The base URL to be used throughout the document for relative URLs.
    Absolute and relative URLs are allowed.
    [`data:`](https://developer.mozilla.org/en-US/docs/Web/HTTP/Basics_of_HTTP/Data_URLs)
    and `javascript:` URLs are not allowed.

[`target`](#target)

:   A **keyword** or **author-defined name** of the default [browsing
    context](https://developer.mozilla.org/en-US/docs/Glossary/Browsing_context)
    to show the results of navigation from [`<a>`](a), [`<area>`](area),
    or [`<form>`](form) elements without explicit `target` attributes.
    The following keywords have special meanings:

    -   `_self` (default): Show the result in the current browsing
        context.
    -   `_blank`: Show the result in a new, unnamed browsing context.
    -   `_parent`: Show the result in the parent browsing context of the
        current one, if the current page is inside a frame. If there is
        no parent, acts the same as `_self`.
    -   `_top`: Show the result in the topmost browsing context (the
        browsing context that is an ancestor of the current one and has
        no parent). If there is no parent, acts the same as `_self`.
:::

## Usage notes {#usage_notes}

### Multiple \<base\> elements {#multiple_base_elements}

::: section-content
If multiple `<base>` elements are used, only the first `href` and first
`target` are obeyed --- all others are ignored.
:::

### In-page anchors {#in-page_anchors}

::: section-content
Links pointing to a fragment in the document --- e.g.
`<a href="#some-id">` --- are resolved with the `<base>`, triggering an
HTTP request to the base URL with the fragment attached.

For example, given `<base href="https://example.com/">` and this link:
`<a href="#anchor">To anchor</a>`. The link points to
`https://example.com/#anchor`.
:::

### Open Graph {#open_graph}

::: section-content
[Open Graph](https://ogp.me/){target="_blank"} tags do not acknowledge
`<base>`, and should always have full absolute URLs. For example:

::: code-example
[html]{.language-name}

``` {signature="0iJlOR554RqTmTCNFnWl8zyuzUBLJPI8BW+NuSntxSE=" data-language="html"}
<meta property="og:image" content="https://example.com/thumbnail.jpg" />
```
:::
:::

## Examples

::: section-content
::: code-example
[html]{.language-name}

``` {signature="B0MoyV8W9bW4KUhzz0Wuq1E0lI/LfFZ/ZUSqf3CHjZM=" data-language="html"}
<base href="https://www.example.com/" />
<base target="_blank" />
<base target="_top" href="https://example.com/" />
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
  the-base-element]{.small}](https://html.spec.whatwg.org/multipage/semantics.html#the-base-element)

  ----------------------------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
  -------------------------------------------------------------------------------------------------------------------------------
             Desktop                                                  Mobile                                           
  ---------- --------- ------ --------- ------------ ------- -------- --------- --------- --------- --------- -------- ----------
             Chrome    Edge   Firefox   Internet     Opera   Safari   WebView   Chrome    Firefox   Opera     Safari   Samsung
                                        Explorer                      Android   Android   for       Android   on IOS   Internet
                                                                                          Android                      

  `base`     1         12     1         Yes          15      3        4.4       18        4         14        2        1.0
                                                                                                                       
                                        Before                                                                         
                                        Internet                                                                       
                                        Explorer 7,                                                                    
                                        `<base>` can                                                                   
                                        be                                                                             
                                        positioned                                                                     
                                        anywhere in                                                                    
                                        the document                                                                   
                                        and the                                                                        
                                        nearest                                                                        
                                        value of                                                                       
                                        `<base>` is                                                                    
                                        used.                                                                          

  `href`     1         12     1         Yes          15      3        4.4       18        4         14        2        1.0

  `target`   1         12     1         Yes          15      3        4.4       18        4         14        2        1.0
  -------------------------------------------------------------------------------------------------------------------------------
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Element/base](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/base){._attribution-link}
:::
