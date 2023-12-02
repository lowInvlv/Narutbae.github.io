

# \<th\>: The Table Header element



::: section-content
The `<th>` [HTML](../index) element defines a cell as the header of a
group of table cells. The exact nature of this group is defined by the
[`scope`](#scope) and [`headers`](#headers) attributes.
:::

## Try it {#try_it}

::: section-content
::: iframe
::: {.output-header .border-rounded-top}
#### HTML Demo: \<th\> {#html-demo-th .output-heading}

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

::: {#editor-container .editor-container .tabbed-taller .hidden .border-rounded-bottom editor-type="tabbed"}
::: {#tab-container .section .tabs}
::: {#tablist .tab-list role="tablist"}
HTML

CSS

JavaScript
:::

::: {#html-panel .section .hidden tabindex="0" role="tabpanel" aria-labelledby="html" aria-hidden="true"}
::: {#html-editor}
    <table>
      <caption>
        Alien football stars
      </caption>
      <tr>
        <th scope="col">Player</th>
        <th scope="col">Gloobles</th>
        <th scope="col">Za'taak</th>
      </tr>
      <tr>
        <th scope="row">TR-7</th>
        <td>7</td>
        <td>4,569</td>
      </tr>
      <tr>
        <th scope="row">Khiresh Odo</th>
        <td>7</td>
        <td>7,223</td>
      </tr>
      <tr>
        <th scope="row">Mia Oolong</th>
        <td>9</td>
        <td>6,219</td>
      </tr>
    </table>
:::
:::

::: {#css-panel .section .hidden tabindex="0" role="tabpanel" aria-labelledby="css" aria-hidden="true"}
::: {#css-editor}
    td,
    th {
      border: 1px solid rgb(190, 190, 190);
      padding: 10px;
    }

    td {
      text-align: center;
    }

    tr:nth-child(even) {
      background-color: #eee;
    }

    th[scope='col'] {
      background-color: #696969;
      color: #fff;
    }

    th[scope='row'] {
      background-color: #d7d9f2;
    }

    caption {
      padding: 10px;
      caption-side: bottom;
    }

    table {
      border-collapse: collapse;
      border: 2px solid rgb(200, 200, 200);
      letter-spacing: 1px;
      font-family: sans-serif;
      font-size: 0.8rem;
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
:::

## Attributes

::: section-content
This element includes the [global attributes](../global_attributes).

[`abbr`](#abbr)

:   This attribute contains a short abbreviated description of the
    cell\'s content. Some user-agents, such as speech readers, may
    present this description before the content itself.

[`colspan`](#colspan)

:   This attribute contains a non-negative integer value that indicates
    for how many columns the cell extends. Its default value is `1`.
    Values higher than 1000 will be considered as incorrect and will be
    set to the default value (1).

[`headers`](#headers)

:   This attribute contains a list of space-separated strings, each
    corresponding to the **id** attribute of the
    [`<th>`](th){aria-current="page"} elements that apply to this
    element.

[`rowspan`](#rowspan)

:   This attribute contains a non-negative integer value that indicates
    for how many rows the cell extends. Its default value is `1`; if its
    value is set to `0`, it extends until the end of the table section
    ([`<thead>`](thead), [`<tbody>`](tbody), [`<tfoot>`](tfoot), even if
    implicitly defined), that the cell belongs to. Values higher than
    65534 are clipped down to 65534.

[`scope`](#scope)

:   This
    [enumerated](https://developer.mozilla.org/en-US/docs/Glossary/Enumerated)
    attribute defines the cells that the header (defined in the
    [`<th>`](th){aria-current="page"}) element relates to. It may have
    the following values:

    -   `row`: The header relates to all cells of the row it belongs to.
    -   `col`: The header relates to all cells of the column it belongs
        to.
    -   `rowgroup`: The header belongs to a rowgroup and relates to all
        of its cells.
    -   `colgroup`: The header belongs to a colgroup and relates to all
        of its cells.

    If the `scope` attribute is not specified, or its value is not
    `row`, `col`, or `rowgroup`, or `colgroup`, then browsers
    automatically select the set of cells to which the header cell
    applies.
:::

### Deprecated attributes {#deprecated_attributes}

::: section-content

[`align`](#align) [Deprecated]{.visually-hidden}

:   This enumerated attribute specifies how the cell content\'s
    horizontal alignment will be handled. Possible values are:

    -   `left`: The content is aligned to the left of the cell.
    -   `center`: The content is centered in the cell.
    -   `right`: The content is aligned to the right of the cell.
    -   `justify` (with text only): The content is stretched out inside
        the cell so that it covers its entire width.
    -   `char` (with text only): The content is aligned to a character
        inside the `<th>` element with minimal offset. This character is
        defined by the [`char`](#char) and [`charoff`](#charoff)
        attributes.

    The default value when this attribute is not specified is `left`.

    ::: {#sect1 .notecard .note}
    **Note:** Do not use this attribute as it is obsolete in the latest
    standard.

    -   To achieve the same effect as the `left`, `center`, `right` or
        `justify` values, apply the CSS
        [`text-align`](https://developer.mozilla.org/en-US/docs/Web/CSS/text-align)
        property to the element.
    -   To achieve the same effect as the `char` value, give the
        [`text-align`](https://developer.mozilla.org/en-US/docs/Web/CSS/text-align)
        property the same value you would use for the [`char`](#char).
    :::

[`axis`](#axis) [Deprecated]{.visually-hidden}

:   This attribute contains a list of space-separated strings. Each
    string is the `id` of a group of cells that this header applies to.

    ::: {#sect2 .notecard .note}
    **Note:** Do not use this attribute as it is obsolete in the latest
    standard: use the [`scope`](#scope) attribute instead.
    :::

[`bgcolor`](#bgcolor) [Deprecated]{.visually-hidden}

:   This attribute defines the background color of each cell in a
    column. It consists of a 6-digit hexadecimal code as defined in
    [sRGB](https://www.w3.org/Graphics/Color/sRGB){target="_blank"} and
    is prefixed by \'#\'.

[`char`](#char) [Deprecated]{.visually-hidden}

:   The content in the cell element is aligned to a character. Typical
    values include a period (.) to align numbers or monetary values. If
    [`align`](#align) is not set to `char`, this attribute is ignored.

    ::: {#sect3 .notecard .note}
    **Note:** Do not use this attribute as it is obsolete in the latest
    standard. To achieve the same effect, you can specify the character
    as the first value of the
    [`text-align`](https://developer.mozilla.org/en-US/docs/Web/CSS/text-align)
    property.
    :::

[`charoff`](#charoff) [Deprecated]{.visually-hidden}

:   This attribute is used to shift column data to the right of the
    character specified by the **char** attribute. Its value specifies
    the length of this shift.

    ::: {#sect4 .notecard .note}
    **Note:** Do not use this attribute as it is obsolete in the latest
    standard.
    :::

[`height`](#height) [Deprecated]{.visually-hidden}

:   This attribute is used to define a recommended cell height.

    ::: {#sect5 .notecard .note}
    **Note:** Do not use this attribute as it is obsolete in the latest
    standard: use the CSS
    [`height`](https://developer.mozilla.org/en-US/docs/Web/CSS/height)
    property instead.
    :::

[`valign`](#valign) [Deprecated]{.visually-hidden}

:   This attribute specifies how a text is vertically aligned inside a
    cell. Possible values for this attribute are:

    -   `baseline`: Positions the text near the bottom of the cell and
        aligns it with the
        [baseline](https://en.wikipedia.org/wiki/Baseline_%28typography%29){target="_blank"}
        of the characters instead of the bottom. If characters don\'t
        descend below the baseline, the baseline value achieves the same
        effect as `bottom`.
    -   `bottom`: Positions the text near the bottom of the cell.
    -   `middle`: Centers the text in the cell.
    -   and `top`: Positions the text near the top of the cell.

    ::: {#sect6 .notecard .note}
    **Note:** Do not use this attribute as it is obsolete in the latest
    standard: use the CSS
    [`vertical-align`](https://developer.mozilla.org/en-US/docs/Web/CSS/vertical-align)
    property instead.
    :::

[`width`](#width) [Deprecated]{.visually-hidden}

:   This attribute is used to define a recommended cell width.
    Additional space can be added with the
    [`cellspacing`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLTableElement/cellSpacing)
    and
    [`cellpadding`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLTableElement/cellPadding)
    properties and the width of the [`<col>`](col) element can also
    create extra width. But, if a column\'s width is too narrow to show
    a particular cell properly, it will be widened when displayed.

    ::: {#sect7 .notecard .note}
    **Note:** Do not use this attribute as it is obsolete in the latest
    standard: use the CSS
    [`width`](https://developer.mozilla.org/en-US/docs/Web/CSS/width)
    property instead.
    :::
:::

## Examples

::: section-content
See [`<table>`](table) for examples on `<th>`.
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
<td><a href="../content_categories#flow_content">Flow content</a>, but
with no header, footer, sectioning content, or heading content
descendants.</td>
</tr>
<tr class="odd">
<th scope="row">Tag omission</th>
<td>The start tag is mandatory.<br />
The end tag may be omitted, if it is immediately followed by a <a
href="th" aria-current="page"><code>&lt;th&gt;</code></a> or <a
href="td"><code>&lt;td&gt;</code></a> element or if there are no more
data in its parent element.</td>
</tr>
<tr class="even">
<th scope="row">Permitted parents</th>
<td>A <a href="tr"><code>&lt;tr&gt;</code></a> element.</td>
</tr>
<tr class="odd">
<th scope="row">Implicit ARIA role</th>
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/columnheader_role"><code>columnheader</code></a>
or <a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/rowheader_role"><code>rowheader</code></a></td>
</tr>
<tr class="even">
<th scope="row">Permitted ARIA roles</th>
<td>Any</td>
</tr>
<tr class="odd">
<th scope="row">DOM interface</th>
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLTableCellElement"><code>HTMLTableCellElement</code></a></td>
</tr>
</tbody>
</table>

</figure>
:::

## Specifications

::: _table
  ---------------------------------------------------------------------------------------------
  Specification
  ---------------------------------------------------------------------------------------------
  [HTML Standard\
  [\#
  the-th-element]{.small}](https://html.spec.whatwg.org/multipage/tables.html#the-th-element)

  ---------------------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
              Desktop                                                         Mobile                                                                                   
  ----------- --------- ------ --------- ------------------- ------- -------- ----------------- ---------------- --------------------- --------------- --------------- ------------------
              Chrome    Edge   Firefox   Internet Explorer   Opera   Safari   WebView Android   Chrome Android   Firefox for Android   Opera Android   Safari on IOS   Samsung Internet
  `th`        1         12     1         Yes                 ≤12.1   1        4.4               18               4                     ≤12.1           1               1.0
  `abbr`      1         12     1         Yes                 15      1        4.4               18               4                     14              1               1.0
  `align`     1         12     1         Yes                 15      3        4.4               18               4                     14              2               1.0
  `axis`      1         12     1         Yes                 15      1        4.4               18               4                     14              1               1.0
  `bgcolor`   1         12     1         Yes                 ≤15     1        4.4               18               4                     ≤14             1               1.0
  `char`      1         12     No        Yes                 15      ≤4       4.4               18               No                    14              ≤3.2            1.0
  `charoff`   1         12     1         Yes                 15      ≤4       4.4               18               4                     14              ≤3.2            1.0
  `colspan`   1         12     1         Yes                 15      1        4.4               18               4                     14              1               1.0
  `headers`   1         12     1         Yes                 15      1        4.4               18               4                     14              1               1.0
  `rowspan`   1         12     1         Yes                 15      1        4.4               18               4                     14              1               1.0
  `scope`     1         12     1         Yes                 15      1        4.4               18               4                     14              1               1.0
  `valign`    1         12     1         Yes                 15      3        4.4               18               4                     14              2               1.0
  `width`     1         12     1         Yes                 15      1        4.4               18               4                     14              1               1.0
:::

## See also {#see_also}

::: section-content
-   Other table-related HTML Elements: [`<caption>`](caption),
    [`<col>`](col), [`<colgroup>`](colgroup), [`<table>`](table),
    [`<tbody>`](tbody), [`<td>`](td), [`<tfoot>`](tfoot),
    [`<thead>`](thead), [`<tr>`](tr).
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Element/th](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/th){._attribution-link}
:::
