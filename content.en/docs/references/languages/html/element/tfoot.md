

# \<tfoot\>: The Table Foot element



::: section-content
The `<tfoot>` [HTML](../index) element defines a set of rows summarizing
the columns of the table.
:::

## Try it {#try_it}

::: section-content
::: iframe
::: {.output-header .border-rounded-top}
#### HTML Demo: \<tfoot\> {#html-demo-tfoot .output-heading}

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
      <thead>
        <tr>
          <th>Items</th>
          <th scope="col">Expenditure</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <th scope="row">Donuts</th>
          <td>3,000</td>
        </tr>
        <tr>
          <th scope="row">Stationery</th>
          <td>18,000</td>
        </tr>
      </tbody>
      <tfoot>
        <tr>
          <th scope="row">Totals</th>
          <td>21,000</td>
        </tr>
      </tfoot>
    </table>
:::
:::

::: {#css-panel .section .hidden tabindex="0" role="tabpanel" aria-labelledby="css" aria-hidden="true"}
::: {#css-editor}
    thead,
    tfoot {
      background-color: #3f87a6;
      color: #fff;
    }

    tbody {
      background-color: #e4f0f5;
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

    td,
    th {
      border: 1px solid rgb(190, 190, 190);
      padding: 5px 10px;
    }

    td {
      text-align: center;
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
:::

### Deprecated attributes {#deprecated_attributes}

::: section-content
The following attributes are deprecated and should not be used. They are
documented below for reference when updating existing code and for
historical interest only.

[`align`](#align) [Deprecated]{.visually-hidden}

:   This
    [enumerated](https://developer.mozilla.org/en-US/docs/Glossary/Enumerated)
    attribute specifies how horizontal alignment of each cell content
    will be handled. Possible values are:

    -   `left`, aligning the content to the left of the cell
    -   `center`, centering the content in the cell
    -   `right`, aligning the content to the right of the cell
    -   `justify`, inserting spaces into the textual content so that the
        content is justified in the cell
    -   `char`, aligning the textual content on a special character with
        a minimal offset, defined by the [`char`](#char) and
        [`charoff`](#charoff) attributes.

    If this attribute is not set, the `left` value is assumed.

    ::: {#sect1 .notecard .note}
    **Note:**

    -   To achieve the same effect as the `left`, `center`, `right` or
        `justify` values, use the CSS
        [`text-align`](https://developer.mozilla.org/en-US/docs/Web/CSS/text-align)
        property on it.
    -   To achieve the same effect as the `char` value, in CSS, you can
        use the value of the [`char`](#char) as the value of the
        [`text-align`](https://developer.mozilla.org/en-US/docs/Web/CSS/text-align)
        property.
    :::

[`bgcolor`](#bgcolor) [Deprecated]{.visually-hidden}

:   The background color of the table. It is a [6-digit hexadecimal RGB
    code](https://developer.mozilla.org/en-US/docs/Web/CSS/hex-color),
    prefixed by a \'`#`\'. One of the predefined [color
    keywords](https://developer.mozilla.org/en-US/docs/Web/CSS/named-color)
    can also be used.

    To achieve a similar effect, use the CSS
    [`background-color`](https://developer.mozilla.org/en-US/docs/Web/CSS/background-color)
    property.

[`char`](#char) [Deprecated]{.visually-hidden}

:   This attribute specifies the alignment of the content in a column to
    a character. Typical values for this include a period (.) when
    attempting to align numbers or monetary values. If [`align`](#align)
    is not set to `char`, this attribute is ignored.

[`charoff`](#charoff) [Deprecated]{.visually-hidden}

:   This attribute is used to indicate the number of characters to
    offset the column data from the alignment characters specified by
    the `char` attribute.

[`valign`](#valign) [Deprecated]{.visually-hidden}

:   This attribute specifies the vertical alignment of the text within
    each row of cells of the table footer. Possible values for this
    attribute are:

    -   `baseline`, which will put the text as close to the bottom of
        the cell as it is possible, but align it on the
        [baseline](https://en.wikipedia.org/wiki/Baseline_%28typography%29){target="_blank"}
        of the characters instead of the bottom of them. If characters
        are all of the size, this has the same effect as `bottom`.
    -   `bottom`, which will put the text as close to the bottom of the
        cell as it is possible;
    -   `middle`, which will center the text in the cell;
    -   and `top`, which will put the text as close to the top of the
        cell as it is possible.

    ::: {#sect2 .notecard .note}
    **Note:** Do not use this attribute as it is obsolete (and not
    supported) in the latest standard: instead set the CSS
    [`vertical-align`](https://developer.mozilla.org/en-US/docs/Web/CSS/vertical-align)
    property on it.
    :::
:::

## Examples

::: section-content
Please see the [`<table>`](table) page for examples on `<tfoot>`.
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
<td>Zero or more <a href="tr"><code>&lt;tr&gt;</code></a> elements.</td>
</tr>
<tr class="odd">
<th scope="row">Tag omission</th>
<td>The start tag is mandatory. The end tag may be omitted if there is
no more content in the parent <a
href="table"><code>&lt;table&gt;</code></a> element.</td>
</tr>
<tr class="even">
<th scope="row">Permitted parents</th>
<td>A <a href="table"><code>&lt;table&gt;</code></a> element. The <a
href="tfoot" aria-current="page"><code>&lt;tfoot&gt;</code></a> must
appear after any <a href="caption"><code>&lt;caption&gt;</code></a>, <a
href="colgroup"><code>&lt;colgroup&gt;</code></a>, <a
href="thead"><code>&lt;thead&gt;</code></a>, <a
href="tbody"><code>&lt;tbody&gt;</code></a>, or <a
href="tr"><code>&lt;tr&gt;</code></a> element. Note that this is the
requirement in HTML.<br />
Originally, in HTML4, the opposite was true: the <a href="tfoot"
aria-current="page"><code>&lt;tfoot&gt;</code></a> element could not be
placed after any <a href="tbody"><code>&lt;tbody&gt;</code></a> or <a
href="tr"><code>&lt;tr&gt;</code></a> element.</td>
</tr>
<tr class="odd">
<th scope="row">Implicit ARIA role</th>
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/rowgroup_role"><code>rowgroup</code></a></td>
</tr>
<tr class="even">
<th scope="row">Permitted ARIA roles</th>
<td>Any</td>
</tr>
<tr class="odd">
<th scope="row">DOM interface</th>
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLTableSectionElement"><code>HTMLTableSectionElement</code></a></td>
</tr>
</tbody>
</table>

</figure>
:::

## Specifications

::: _table
  ---------------------------------------------------------------------------------------------------
  Specification
  ---------------------------------------------------------------------------------------------------
  [HTML Standard\
  [\#
  the-tfoot-element]{.small}](https://html.spec.whatwg.org/multipage/tables.html#the-tfoot-element)

  ---------------------------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
              Desktop                                                         Mobile                                                                                   
  ----------- --------- ------ --------- ------------------- ------- -------- ----------------- ---------------- --------------------- --------------- --------------- ------------------
              Chrome    Edge   Firefox   Internet Explorer   Opera   Safari   WebView Android   Chrome Android   Firefox for Android   Opera Android   Safari on IOS   Samsung Internet
  `tfoot`     1         12     1         Yes                 ≤12.1   1        4.4               18               4                     ≤12.1           1               1.0
  `align`     1         12     1         Yes                 15      3        4.4               18               4                     14              2               1.0
  `bgcolor`   1         12     1         Yes                 ≤15     1        4.4               18               4                     ≤14             1               1.0
  `char`      1         12     No        Yes                 15      ≤4       4.4               18               No                    14              ≤3.2            1.0
  `charoff`   1         12     1         Yes                 15      ≤4       4.4               18               4                     14              ≤3.2            1.0
  `valign`    1         12     1         Yes                 15      3        4.4               18               4                     14              2               1.0
:::

## See also {#see_also}

::: section-content
-   Other table-related HTML Elements: [`<caption>`](caption),
    [`<col>`](col), [`<colgroup>`](colgroup), [`<table>`](table),
    [`<tbody>`](tbody), [`<td>`](td), [`<th>`](th), [`<thead>`](thead),
    [`<tr>`](tr);
-   CSS properties and pseudo-classes that may be specially useful to
    style the `<tfoot>` element:
    -   the
        [`:nth-child`](https://developer.mozilla.org/en-US/docs/Web/CSS/:nth-child)
        pseudo-class to set the alignment on the cells of the column;
    -   the
        [`text-align`](https://developer.mozilla.org/en-US/docs/Web/CSS/text-align)
        property to align all cells content on the same character, like
        \'.\'.
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Element/tfoot](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/tfoot){._attribution-link}
:::
