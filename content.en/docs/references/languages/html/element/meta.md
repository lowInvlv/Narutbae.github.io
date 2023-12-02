

# \<meta\>: The metadata element



::: section-content
The `<meta>` [HTML](../index) element represents
[metadata](https://developer.mozilla.org/en-US/docs/Glossary/Metadata)
that cannot be represented by other HTML meta-related elements, like
[`<base>`](base), [`<link>`](link), [`<script>`](script),
[`<style>`](style) or [`<title>`](title).

<figure class="table-container">
<div class="_table">
<table class="properties">
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<th><a href="../content_categories">Content categories</a></th>
<td><a href="../content_categories#metadata_content">Metadata
content</a>. If the <a
href="../global_attributes/itemprop"><code>itemprop</code></a> attribute
is present: <a href="../content_categories#flow_content">flow
content</a>, <a href="../content_categories#phrasing_content">phrasing
content</a>.</td>
</tr>
<tr class="even">
<th>Permitted content</th>
<td>None; it is a <a
href="https://developer.mozilla.org/en-US/docs/Glossary/Void_element">void
element</a>.</td>
</tr>
<tr class="odd">
<th>Tag omission</th>
<td>As it is a void element, the start tag must be present and the end
tag must not be present.</td>
</tr>
<tr class="even">
<th>Permitted parents</th>
<td><ul>
<li><code>&lt;meta charset&gt;</code>,
<code>&lt;meta http-equiv&gt;</code>: a <a
href="head"><code>&lt;head&gt;</code></a> element. If the <a
href="meta#http-equiv" aria-current="page"><code>http-equiv</code></a>
is not an encoding declaration, it can also be inside a <a
href="noscript"><code>&lt;noscript&gt;</code></a> element, itself inside
a <code>&lt;head&gt;</code> element.</li>
<li><code>&lt;meta name&gt;</code>: any element that accepts <a
href="../content_categories#metadata_content">metadata content</a>.</li>
<li><code>&lt;meta itemprop&gt;</code>: any element that accepts <a
href="../content_categories#metadata_content">metadata content</a> or <a
href="../content_categories#flow_content">flow content</a>.</li>
</ul></td>
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
href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLMetaElement"><code>HTMLMetaElement</code></a></td>
</tr>
</tbody>
</table>

</figure>

The type of metadata provided by the `<meta>` element can be one of the
following:

-   If the [`name`](#name) attribute is set, the `<meta>` element
    provides *document-level metadata*, applying to the whole page.
-   If the [`http-equiv`](#http-equiv) attribute is set, the `<meta>`
    element is a *pragma directive*, providing information equivalent to
    what can be given by a similarly-named HTTP header.
-   If the [`charset`](#charset) attribute is set, the `<meta>` element
    is a *charset declaration*, giving the character encoding in which
    the document is encoded.
-   If the [`itemprop`](../global_attributes/itemprop) attribute is set,
    the `<meta>` element provides *user-defined metadata*.
:::

## Attributes

::: section-content
This element includes the [global attributes](../global_attributes).

::: {#sect1 .notecard .note}
**Note:** the attribute [`name`](#name) has a specific meaning for the
`<meta>` element, and the [`itemprop`](../global_attributes/itemprop)
attribute must not be set on the same `<meta>` element that has any
existing [`name`](#name), [`http-equiv`](#http-equiv) or
[`charset`](#charset) attributes.
:::

[`charset`](#charset)

:   This attribute declares the document\'s character encoding. If the
    attribute is present, its value must be an ASCII case-insensitive
    match for the string `"utf-8"`, because UTF-8 is the only valid
    encoding for HTML5 documents. `<meta>` elements which declare a
    character encoding must be located entirely within the first 1024
    bytes of the document.

[`content`](#content)

:   This attribute contains the value for the
    [`http-equiv`](#http-equiv) or [`name`](#name) attribute, depending
    on which is used.

[`http-equiv`](#http-equiv)

:   Defines a pragma directive. The attribute is named
    `http-equiv(alent)` because all the allowed values are names of
    particular HTTP headers:

    -   `content-security-policy` Allows page authors to define a
        [content
        policy](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Security-Policy)
        for the current page. Content policies mostly specify allowed
        server origins and script endpoints which help guard against
        cross-site scripting attacks.
    -   `content-type` Declares the [MIME
        type](https://developer.mozilla.org/en-US/docs/Web/HTTP/Basics_of_HTTP/MIME_types)
        and the document\'s character encoding. The `content` attribute
        must have the value `"text/html; charset=utf-8"` if specified.
        This is equivalent to a `<meta>` element with the
        [`charset`](#charset) attribute specified and carries the same
        restriction on placement within the document. **Note:** Can only
        be used in documents served with a `text/html` --- not in
        documents served with an XML MIME type.
    -   `default-style` Sets the name of the default [CSS style
        sheet](https://developer.mozilla.org/en-US/docs/Web/CSS) set.
    -   `x-ua-compatible` If specified, the `content` attribute must
        have the value `"IE=edge"`. User agents are required to ignore
        this pragma.
    -   `refresh` This instruction specifies:
        -   The number of seconds until the page should be reloaded -
            only if the [`content`](#content) attribute contains a
            non-negative integer.
        -   The number of seconds until the page should redirect to
            another - only if the [`content`](#content) attribute
            contains a non-negative integer followed by the string
            \'`;url=`\', and a valid URL.

        ::: {#sect2 .notecard .warning}
        **Warning:**

        Pages set with a `refresh` value run the risk of having the time
        interval being too short. People navigating with the aid of
        assistive technology such as a screen reader may be unable to
        read through and understand the page\'s content before being
        automatically redirected. The abrupt, unannounced updating of
        the page content may also be disorienting for people
        experiencing low vision conditions.

        -   [MDN Understanding WCAG, Guideline 2.2
            explanations](https://developer.mozilla.org/en-US/docs/Web/Accessibility/Understanding_WCAG/Operable#guideline_2.2_%E2%80%94_enough_time_provide_users_enough_time_to_read_and_use_content)
        -   [MDN Understanding WCAG, Guideline 3.2
            explanations](https://developer.mozilla.org/en-US/docs/Web/Accessibility/Understanding_WCAG/Understandable#guideline_3.2_%E2%80%94_predictable_make_web_pages_appear_and_operate_in_predictable_ways)
        -   [Understanding Success Criterion 2.2.1 \| W3C Understanding
            WCAG
            2.0](https://www.w3.org/TR/UNDERSTANDING-WCAG20/time-limits-required-behaviors.html){target="_blank"}
        -   [Understanding Success Criterion 2.2.4 \| W3C Understanding
            WCAG
            2.0](https://www.w3.org/TR/UNDERSTANDING-WCAG20/time-limits-postponed.html){target="_blank"}
        -   [Understanding Success Criterion 3.2.5 \| W3C Understanding
            WCAG
            2.0](https://www.w3.org/TR/UNDERSTANDING-WCAG20/consistent-behavior-no-extreme-changes-context.html){target="_blank"}
        :::

[`name`](#name)

:   The `name` and `content` attributes can be used together to provide
    document metadata in terms of name-value pairs, with the `name`
    attribute giving the metadata name, and the `content` attribute
    giving the value.

    See [standard metadata names](meta/name) for details about the set
    of standard metadata names defined in the HTML specification.
:::

## Examples

::: section-content
::: code-example
[html]{.language-name}

``` {signature="ZKxchLc9Rnwup9RkUsx2VD1dcdYZZLvhr67TzaYZpgM=" data-language="html"}
<meta charset="utf-8" />

<!-- Redirect page after 3 seconds -->
<meta http-equiv="refresh" content="3;url=https://www.mozilla.org" />
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
  the-meta-element]{.small}](https://html.spec.whatwg.org/multipage/semantics.html#the-meta-element)

  ----------------------------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
                 Desktop                                                         Mobile                                                                                   
  -------------- --------- ------ --------- ------------------- ------- -------- ----------------- ---------------- --------------------- --------------- --------------- ------------------
                 Chrome    Edge   Firefox   Internet Explorer   Opera   Safari   WebView Android   Chrome Android   Firefox for Android   Opera Android   Safari on IOS   Samsung Internet
  `meta`         1         12     1         Yes                 ≤12.1   1        4.4               18               4                     ≤12.1           1               1.0
  `charset`      1         12     1         Yes                 15      3        4.4               18               4                     14              2               1.0
  `content`      1         12     1         ≤6                  ≤12.1   ≤4       4.4               18               4                     ≤12.1           ≤3.2            1.0
  `http-equiv`   1         12     1         ≤6                  ≤12.1   ≤4       4.4               18               4                     ≤12.1           ≤3.2            1.0
  `name`         1         12     1         ≤6                  ≤12.1   ≤4       4.4               18               4                     ≤12.1           ≤3.2            1.0
:::

## See also {#see_also}

::: section-content
-   [Standard metadata names](meta/name)
-   [Learn:
    `<meta>`](https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/The_head_metadata_in_HTML#metadata_the_meta_element)
-   [The viewport meta tag](../viewport_meta_tag)
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Element/meta](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/meta){._attribution-link}
:::
