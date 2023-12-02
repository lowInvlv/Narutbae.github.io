

# \<body\>: The Document Body element



::: section-content
The `<body>` [HTML](../index) element represents the content of an HTML
document. There can be only one `<body>` element in a document.

<figure class="table-container">
<div class="_table">
<table class="properties">
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<th scope="row"><a href="../content_categories">Content
categories</a></th>
<td>None.</td>
</tr>
<tr class="even">
<th scope="row">Permitted content</th>
<td><a href="../content_categories#flow_content">Flow content</a>.</td>
</tr>
<tr class="odd">
<th scope="row">Tag omission</th>
<td>The start tag may be omitted if the first thing inside it is not a
space character, comment, <a
href="script"><code>&lt;script&gt;</code></a> element or <a
href="style"><code>&lt;style&gt;</code></a> element. The end tag may be
omitted if the <code>&lt;body&gt;</code> element has contents or has a
start tag, and is not immediately followed by a comment.</td>
</tr>
<tr class="even">
<th scope="row">Permitted parents</th>
<td>It must be the second element of an <a
href="html"><code>&lt;html&gt;</code></a> element.</td>
</tr>
<tr class="odd">
<th scope="row">Implicit ARIA role</th>
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/generic_role"><code>generic</code></a></td>
</tr>
<tr class="even">
<th scope="row">Permitted ARIA roles</th>
<td>No <code>role</code> permitted</td>
</tr>
<tr class="odd">
<th scope="row">DOM interface</th>
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLBodyElement"><code>HTMLBodyElement</code></a>
<ul>
<li>The <code>&lt;body&gt;</code> element exposes the <a
href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLBodyElement"><code>HTMLBodyElement</code></a>
interface.</li>
<li>You can access the <code>&lt;body&gt;</code> element through the <a
href="https://developer.mozilla.org/en-US/docs/Web/API/Document/body"><code>document.body</code></a>
property.</li>
</ul></td>
</tr>
</tbody>
</table>

</figure>
:::

## Attributes

::: section-content
This element includes the [global attributes](../global_attributes).

[`alink`](#alink) [Deprecated]{.visually-hidden}

:   Color of text for hyperlinks when selected. **Do not use this
    attribute! Use the CSS
    [`color`](https://developer.mozilla.org/en-US/docs/Web/CSS/color)
    property in conjunction with the
    [`:active`](https://developer.mozilla.org/en-US/docs/Web/CSS/:active)
    pseudo-class instead.**

[`background`](#background) [Deprecated]{.visually-hidden}

:   URI of an image to use as a background. **Do not use this attribute!
    Use the CSS
    [`background`](https://developer.mozilla.org/en-US/docs/Web/CSS/background)
    property on the element instead.**

[`bgcolor`](#bgcolor) [Deprecated]{.visually-hidden}

:   Background color for the document. **Do not use this attribute! Use
    the CSS
    [`background-color`](https://developer.mozilla.org/en-US/docs/Web/CSS/background-color)
    property on the element instead.**

[`bottommargin`](#bottommargin) [Deprecated]{.visually-hidden}

:   The margin of the bottom of the body. **Do not use this attribute!
    Use the CSS
    [`margin-bottom`](https://developer.mozilla.org/en-US/docs/Web/CSS/margin-bottom)
    property on the element instead.**

[`leftmargin`](#leftmargin) [Deprecated]{.visually-hidden}

:   The margin of the left of the body. **Do not use this attribute! Use
    the CSS
    [`margin-left`](https://developer.mozilla.org/en-US/docs/Web/CSS/margin-left)
    property on the element instead.**

[`link`](#link) [Deprecated]{.visually-hidden}

:   Color of text for unvisited hypertext links. **Do not use this
    attribute! Use the CSS
    [`color`](https://developer.mozilla.org/en-US/docs/Web/CSS/color)
    property in conjunction with the
    [`:link`](https://developer.mozilla.org/en-US/docs/Web/CSS/:link)
    pseudo-class instead.**

[`onafterprint`](#onafterprint)

:   Function to call after the user has printed the document.

[`onbeforeprint`](#onbeforeprint)

:   Function to call when the user requests printing of the document.

[`onbeforeunload`](#onbeforeunload)

:   Function to call when the document is about to be unloaded.

[`onblur`](#onblur)

:   Function to call when the document loses focus.

[`onerror`](#onerror)

:   Function to call when the document fails to load properly.

[`onfocus`](#onfocus)

:   Function to call when the document receives focus.

[`onhashchange`](#onhashchange)

:   Function to call when the fragment identifier part (starting with
    the hash (`'#'`) character) of the document\'s current address has
    changed.

[`onlanguagechange`](#onlanguagechange)

:   Function to call when the preferred languages changed.

[`onload`](#onload)

:   Function to call when the document has finished loading.

[`onmessage`](#onmessage)

:   Function to call when the document has received a message.

[`onoffline`](#onoffline)

:   Function to call when network communication has failed.

[`ononline`](#ononline)

:   Function to call when network communication has been restored.

[`onpopstate`](#onpopstate)

:   Function to call when the user has navigated session history.

[`onredo`](#onredo)

:   Function to call when the user has moved forward in undo transaction
    history.

[`onresize`](#onresize)

:   Function to call when the document has been resized.

[`onstorage`](#onstorage)

:   Function to call when the storage area has changed.

[`onundo`](#onundo)

:   Function to call when the user has moved backward in undo
    transaction history.

[`onunload`](#onunload)

:   Function to call when the document is going away.

[`rightmargin`](#rightmargin) [Deprecated]{.visually-hidden}

:   The margin of the right of the body. **Do not use this attribute!
    Use the CSS
    [`margin-right`](https://developer.mozilla.org/en-US/docs/Web/CSS/margin-right)
    property on the element instead.**

[`text`](#text) [Deprecated]{.visually-hidden}

:   Foreground color of text. **Do not use this attribute! Use CSS
    [`color`](https://developer.mozilla.org/en-US/docs/Web/CSS/color)
    property on the element instead.**

[`topmargin`](#topmargin) [Deprecated]{.visually-hidden}

:   The margin of the top of the body. **Do not use this attribute! Use
    the CSS
    [`margin-top`](https://developer.mozilla.org/en-US/docs/Web/CSS/margin-top)
    property on the element instead.**

[`vlink`](#vlink) [Deprecated]{.visually-hidden}

:   Color of text for visited hypertext links. **Do not use this
    attribute! Use the CSS
    [`color`](https://developer.mozilla.org/en-US/docs/Web/CSS/color)
    property in conjunction with the
    [`:visited`](https://developer.mozilla.org/en-US/docs/Web/CSS/:visited)
    pseudo-class instead.**
:::

## Examples

::: section-content
::: code-example
[html]{.language-name}

``` {signature="H10tvIA0tw8h87d9Udg0elNUpZBIwIPLHypfbXy9j1o=" data-language="html"}
<html lang="en">
  <head>
    <title>Document title</title>
  </head>
  <body>
    <p>
      The <code>&lt;body&gt;</code> HTML element represents the content of an
      HTML document. There can be only one <code>&lt;body&gt;</code> element in
      a document.
    </p>
  </body>
</html>
```
:::
:::

### Result

::: section-content
::: {#sect1 .code-example}
::: iframe
:::
:::
:::

## Specifications

::: _table
  ---------------------------------------------------------------------------------------------------
  Specification
  ---------------------------------------------------------------------------------------------------
  [HTML Standard\
  [\#
  the-body-element]{.small}](https://html.spec.whatwg.org/multipage/sections.html#the-body-element)

  ---------------------------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
  ---------------------------------------------------------------------------------------------------------------------------------------
                   Desktop                                                  Mobile                                             
  ---------------- --------- ------ ----------- ---------- ------- -------- --------- --------- ----------- --------- -------- ----------
                   Chrome    Edge   Firefox     Internet   Opera   Safari   WebView   Chrome    Firefox for Opera     Safari   Samsung
                                                Explorer                    Android   Android   Android     Android   on IOS   Internet

  `body`           1         12     1           Yes        15      1        4.4       18        4           14        1        1.0

  `alink`          1         12     1           Yes        15      ≤4       4.4       18        4           14        ≤3.2     1.0

  `background`     1         12     1           Yes        15      ≤4       4.4       18        4           14        ≤3.2     1.0

  `bgcolor`        1         12     1           Yes        15      ≤4       4.4       18        4           14        ≤3.2     1.0

  `bottommargin`   1         79     35          No         15      ≤4       4.4       18        35          14        ≤3.2     1.0
                                                                                                                               
                                    Before                                                      Before                         
                                    Firefox 35,                                                 Firefox 35,                    
                                    it was                                                      it was                         
                                    supported                                                   supported                      
                                    in Quirks                                                   in Quirks                      
                                    Mode only.                                                  Mode only.                     

  `leftmargin`     1         79     35          No         15      ≤4       4.4       18        35          14        ≤3.2     1.0
                                                                                                                               
                                    Before                                                      Before                         
                                    Firefox 35,                                                 Firefox 35,                    
                                    it was                                                      it was                         
                                    supported                                                   supported                      
                                    in Quirks                                                   in Quirks                      
                                    Mode only.                                                  Mode only.                     

  `link`           1         12     1           Yes        15      ≤4       4.4       18        4           14        ≤3.2     1.0

  `rightmargin`    1         79     35          No         15      ≤4       4.4       18        35          14        ≤3.2     1.0
                                                                                                                               
                                    Before                                                      Before                         
                                    Firefox 35,                                                 Firefox 35,                    
                                    it was                                                      it was                         
                                    supported                                                   supported                      
                                    in Quirks                                                   in Quirks                      
                                    Mode only.                                                  Mode only.                     

  `text`           1         12     1           Yes        15      ≤4       4.4       18        4           14        ≤3.2     1.0

  `topmargin`      1         79     35          No         15      ≤4       4.4       18        35          14        ≤3.2     1.0
                                                                                                                               
                                    Before                                                      Before                         
                                    Firefox 35,                                                 Firefox 35,                    
                                    it was                                                      it was                         
                                    supported                                                   supported                      
                                    in Quirks                                                   in Quirks                      
                                    Mode only.                                                  Mode only.                     

  `vlink`          1         12     1           Yes        15      ≤4       4.4       18        4           14        ≤3.2     1.0
  ---------------------------------------------------------------------------------------------------------------------------------------
:::

## See also {#see_also}

::: section-content
-   [`<html>`](html)
-   [`<head>`](head)
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Element/body](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/body){._attribution-link}
:::
