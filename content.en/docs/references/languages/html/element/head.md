

# \<head\>: The Document Metadata (Header) element



::: section-content
The `<head>` [HTML](../index) element contains machine-readable
information
([metadata](https://developer.mozilla.org/en-US/docs/Glossary/Metadata))
about the document, like its [title](title), [scripts](script), and
[style sheets](style).

::: {#sect1 .notecard .note}
**Note:** `<head>` primarily holds information for machine processing,
not human-readability. For human-visible information, like top-level
headings and listed authors, see the [`<header>`](header) element.
:::
:::

## Attributes

::: section-content
This element includes the [global attributes](../global_attributes).

[`profile`](#profile) [Deprecated]{.visually-hidden} [Non-standard]{.visually-hidden}

:   The [URI](https://developer.mozilla.org/en-US/docs/Glossary/URI)s of
    one or more metadata profiles, separated by [white
    space](https://developer.mozilla.org/en-US/docs/Glossary/Whitespace).
:::

## Examples

::: section-content
::: code-example
[html]{.language-name}

``` {signature="yXjwe/c/5BBR2/0Xj76DfRIM40/zDF5hKNrUillhYE0=" data-language="html"}
<!doctype html>
<html lang="en-US">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width" />
    <title>Document title</title>
  </head>
</html>
```
:::
:::

## Technical summary {#technical_summary}

::: section-content
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
<td><p>If the document is an <a
href="iframe"><code>&lt;iframe&gt;</code></a> <a
href="iframe#srcdoc"><code>srcdoc</code></a> document, or if title
information is available from a higher level protocol (like the subject
line in HTML email), zero or more elements of metadata content.</p>
<p>Otherwise, one or more elements of metadata content where exactly one
is a <a href="title"><code>&lt;title&gt;</code></a> element.</p></td>
</tr>
<tr class="odd">
<th scope="row">Tag omission</th>
<td>The start tag may be omitted if the first thing inside the
<code>&lt;head&gt;</code> element is an element.<br />
The end tag may be omitted if the first thing following the
<code>&lt;head&gt;</code> element is not a space character or a
comment.</td>
</tr>
<tr class="even">
<th scope="row">Permitted parents</th>
<td>An <a href="html"><code>&lt;html&gt;</code></a> element, as its
first child.</td>
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
href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLHeadElement"><code>HTMLHeadElement</code></a></td>
</tr>
</tbody>
</table>

</figure>
:::

## Specifications

::: _table
  ----------------------------------------------------------------------------------------------------
  Specification
  ----------------------------------------------------------------------------------------------------
  [HTML Standard\
  [\#
  the-head-element]{.small}](https://html.spec.whatwg.org/multipage/semantics.html#the-head-element)

  ----------------------------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
              Desktop                                                          Mobile                                                                                   
  ----------- --------- ------ --------- ------------------- ------- --------- ----------------- ---------------- --------------------- --------------- --------------- ------------------
              Chrome    Edge   Firefox   Internet Explorer   Opera   Safari    WebView Android   Chrome Android   Firefox for Android   Opera Android   Safari on IOS   Samsung Internet
  `head`      1         12     1         Yes                 15      1         4.4               18               4                     14              1               1.0
  `profile`   1         12     1         Yes                 15      1--16.4   4.4               18               4                     14              1--16.4         1.0
:::

## See also {#see_also}

::: section-content
-   Elements that can be used inside the `<head>`:
    -   [`<title>`](title)
    -   [`<base>`](base)
    -   [`<link>`](link)
    -   [`<style>`](style)
    -   [`<meta>`](meta)
    -   [`<script>`](script)
    -   [`<noscript>`](noscript)
    -   [`<template>`](template)
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Element/head](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/head){._attribution-link}
:::
