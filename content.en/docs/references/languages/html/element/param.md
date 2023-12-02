

# \<param\>: The Object Parameter element



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

The `<param>` [HTML](../index) element defines parameters for an
[`<object>`](object) element.
:::

## Attributes

::: section-content
This element includes the [global attributes](../global_attributes).

[`name`](#name) [Deprecated]{.visually-hidden}

:   Name of the parameter.

[`value`](#value) [Deprecated]{.visually-hidden}

:   Specifies the value of the parameter.

[`type`](#type) [Deprecated]{.visually-hidden}

:   Only used if the `valuetype` is set to `ref`. Specifies the MIME
    type of values found at the URI specified by value.

[`valuetype`](#valuetype) [Deprecated]{.visually-hidden}

:   Specifies the type of the `value` attribute. Possible values are:

    -   `data`: Default value. The value is passed to the object\'s
        implementation as a string.
    -   `ref`: The value is a URI to a resource where run-time values
        are stored.
    -   `object`: An ID of another [`<object>`](object) in the same
        document.
:::

## Technical summary {#technical_summary}

::: section-content
<figure class="table-container">
<div class="_table">
<table class="properties">
<tbody>
<tr class="odd">
<th scope="row"><a href="../content_categories">Content
categories</a></th>
<td>None.</td>
</tr>
<tr class="even">
<th scope="row">Permitted content</th>
<td>None; it is a <a
href="https://developer.mozilla.org/en-US/docs/Glossary/Void_element">void
element</a>.</td>
</tr>
<tr class="odd">
<th scope="row">Tag omission</th>
<td>As it is a void element, the start tag must be present and the end
tag must not be present.</td>
</tr>
<tr class="even">
<th scope="row">Permitted parents</th>
<td>An <a href="object"><code>&lt;object&gt;</code></a> before any <a
href="../content_categories#flow_content">flow content</a>.</td>
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
href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLParamElement"><code>HTMLParamElement</code></a></td>
</tr>
</tbody>
</table>

</figure>
:::

## Specifications

::: _table
  -----------------------------------------------------------------------------------------------------
  Specification
  -----------------------------------------------------------------------------------------------------
  [HTML Standard\
  [\#
  the-param-element]{.small}](https://html.spec.whatwg.org/multipage/obsolete.html#the-param-element)

  -----------------------------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
                Desktop                                                         Mobile                                                                                   
  ------------- --------- ------ --------- ------------------- ------- -------- ----------------- ---------------- --------------------- --------------- --------------- ------------------
                Chrome    Edge   Firefox   Internet Explorer   Opera   Safari   WebView Android   Chrome Android   Firefox for Android   Opera Android   Safari on IOS   Samsung Internet
  `param`       1         12     1         Yes                 15      ≤4       4.4               18               4                     14              ≤3.2            1.0
  `name`        1         12     1         Yes                 15      ≤4       4.4               18               4                     14              ≤3.2            1.0
  `type`        1         12     1         Yes                 15      ≤4       4.4               18               4                     14              ≤3.2            1.0
  `value`       1         12     1         Yes                 15      ≤4       4.4               18               4                     14              ≤3.2            1.0
  `valuetype`   1         12     1         Yes                 15      ≤4       4.4               18               4                     14              ≤3.2            1.0
:::

## See also {#see_also}

::: section-content
-   [`<object>`](object)
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Element/param](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/param){._attribution-link}
:::
