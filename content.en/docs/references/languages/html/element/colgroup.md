

# \<colgroup\>: The Table Column Group element



::: section-content
The `<colgroup>` [HTML](../index) element defines a group of columns
within a table.
:::

## Try it {#try_it}

::: section-content
::: iframe
::: {.output-header .border-rounded-top}
#### HTML Demo: \<colgroup\> {#html-demo-colgroup .output-heading}

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
        Superheros and sidekicks
      </caption>
      <colgroup>
        <col />
        <col span="2" class="batman" />
        <col span="2" class="flash" />
      </colgroup>
      <tr>
        <td> </td>
        <th scope="col">Batman</th>
        <th scope="col">Robin</th>
        <th scope="col">The Flash</th>
        <th scope="col">Kid Flash</th>
      </tr>
      <tr>
        <th scope="row">Skill</th>
        <td>Smarts</td>
        <td>Dex, acrobat</td>
        <td>Super speed</td>
        <td>Super speed</td>
      </tr>
    </table>
:::
:::

::: {#css-panel .section .hidden tabindex="0" role="tabpanel" aria-labelledby="css" aria-hidden="true"}
::: {#css-editor}
    .batman {
      background-color: #d7d9f2;
    }

    .flash {
      background-color: #ffe8d4;
    }

    caption {
      padding: 8px;
      caption-side: bottom;
    }

    table {
      border-collapse: collapse;
      border: 2px solid rgb(100, 100, 100);
      letter-spacing: 1px;
      font-family: sans-serif;
      font-size: 0.7rem;
    }

    td,
    th {
      border: 1px solid rgb(100, 100, 100);
      padding: 10px 10px;
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
This element\'s attributes include the [global
attributes](../global_attributes).

[`span`](#span)

:   This attribute contains a positive integer indicating the number of
    consecutive columns the `<colgroup>` element spans. If not present,
    its default value is `1`.

    The `span` attribute is not permitted if there are one or more
    [`<col>`](col) elements within the `<colgroup>`.
:::

### Deprecated attributes {#deprecated_attributes}

::: section-content
The following attributes are deprecated and should not be used. They are
documented below for reference when updating existing code and for
historical interest only.

[`align`](#align) [Deprecated]{.visually-hidden}

:   This
    [enumerated](https://developer.mozilla.org/en-US/docs/Glossary/Enumerated)
    attribute specifies how horizontal alignment of each column cell
    content will be handled. Possible values are:

    -   `left`, aligning the content to the left of the cell
    -   `center`, centering the content in the cell
    -   `right`, aligning the content to the right of the cell
    -   `justify`, inserting spaces into the textual content so that the
        content is justified in the cell
    -   `char`, aligning the textual content on a special character with
        a minimal offset, defined by the [`char`](col#char) and
        [`charoff`](col#charoff) attributes.

    If this attribute is not set, the `left` value is assumed. The
    descendant [`<col>`](col) elements may override this value using
    their own [`align`](col#align) attribute.

    ::: {#sect1 .notecard .note}
    **Note:** Do not try to set the
    [`text-align`](https://developer.mozilla.org/en-US/docs/Web/CSS/text-align)
    property on a selector giving a
    [`<colgroup>`](colgroup){aria-current="page"} element. Because
    [`<td>`](td) elements are not descendant of the
    [`<colgroup>`](colgroup){aria-current="page"} element, they won\'t
    inherit it.

    If the table doesn\'t use a [`colspan`](td#colspan) attribute, use
    one `td:nth-child(an+b)` CSS selector per column, where \'a\' is the
    total number of the columns in the table and \'b\' is the ordinal
    position of this column in the table. Only after this selector the
    `text-align` property can be used.

    If the table does use a [`colspan`](td#colspan) attribute, the
    effect can be achieved by combining adequate CSS attribute selectors
    like `[colspan=n]`, though this is not trivial.
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

:   This attribute specifies the alignment of the content in a column
    group to a character. Typical values for this include a period (.)
    when attempting to align numbers or monetary values. If
    [`align`](#align) is not set to `char`, this attribute is ignored,
    though it will still be used as the default value for the
    [`align`](col#align) of the [`<col>`](col) which are members of this
    column group.

[`charoff`](#charoff) [Deprecated]{.visually-hidden}

:   This attribute is used to indicate the number of characters to
    offset the column data from the alignment character specified by the
    `char` attribute.

[`valign`](#valign) [Deprecated]{.visually-hidden}

:   This attribute specifies the vertical alignment of the text within
    each cell of the column. Possible values for this attribute are:

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
    **Note:** Do not try to set the
    [`vertical-align`](https://developer.mozilla.org/en-US/docs/Web/CSS/vertical-align)
    property on a selector giving a `<colgroup>` element. Because
    [`<td>`](td) elements are not descendant of the `<colgroup>`
    element, they won\'t inherit it.

    If the table doesn\'t use a [`colspan`](td#colspan) attribute, use
    the `td:nth-child(an+b)` CSS selector per column, where \'a\' is the
    total number of the columns in the table and \'b\' is the ordinal
    position of the column in the table. Only after this selector the
    `vertical-align` property can be used.

    If the table does use a [`colspan`](td#colspan) attribute, the
    effect can be achieved by combining adequate CSS attribute selectors
    like `[colspan=n]`, though this is not trivial.
    :::
:::

## Examples

::: section-content
Please see the [`<table>`](table) page for examples on `<colgroup>`.
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
<td>If the <a href="colgroup#span"
aria-current="page"><code>span</code></a> attribute is present:
none.<br />
If the attribute is not present: zero or more <a
href="col"><code>&lt;col&gt;</code></a> element</td>
</tr>
<tr class="odd">
<th scope="row">Tag omission</th>
<td>The start tag may be omitted, if it has a <a
href="col"><code>&lt;col&gt;</code></a> element as its first child and
if it is not preceded by a <a href="colgroup"
aria-current="page"><code>&lt;colgroup&gt;</code></a> whose end tag has
been omitted.<br />
The end tag may be omitted, if it is not followed by a space or a
comment.</td>
</tr>
<tr class="even">
<th scope="row">Permitted parents</th>
<td>A <a href="table"><code>&lt;table&gt;</code></a> element. The <a
href="colgroup" aria-current="page"><code>&lt;colgroup&gt;</code></a>
must appear after any optional <a
href="caption"><code>&lt;caption&gt;</code></a> element but before any
<a href="thead"><code>&lt;thead&gt;</code></a>, <a
href="th"><code>&lt;th&gt;</code></a>, <a
href="tbody"><code>&lt;tbody&gt;</code></a>, <a
href="tfoot"><code>&lt;tfoot&gt;</code></a> and <a
href="tr"><code>&lt;tr&gt;</code></a> element.</td>
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
href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLTableColElement"><code>HTMLTableColElement</code></a></td>
</tr>
</tbody>
</table>

</figure>
:::

## Specifications

::: _table
  ---------------------------------------------------------------------------------------------------------
  Specification
  ---------------------------------------------------------------------------------------------------------
  [HTML Standard\
  [\#
  the-colgroup-element]{.small}](https://html.spec.whatwg.org/multipage/tables.html#the-colgroup-element)

  ---------------------------------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
               Desktop                                                         Mobile                                                                                   
  ------------ --------- ------ --------- ------------------- ------- -------- ----------------- ---------------- --------------------- --------------- --------------- ------------------
               Chrome    Edge   Firefox   Internet Explorer   Opera   Safari   WebView Android   Chrome Android   Firefox for Android   Opera Android   Safari on IOS   Samsung Internet
  `colgroup`   1         12     1         Yes                 15      ≤4       4.4               18               4                     14              ≤3.2            1.0
  `align`      1         12     1         Yes                 15      3        4.4               18               4                     14              2               1.0
  `bgcolor`    1         12     1         Yes                 15      1        4.4               18               4                     14              1               1.0
  `char`       1         12     No        Yes                 15      3        4.4               18               No                    14              2               1.0
  `charoff`    1         12     No        Yes                 15      3        4.4               18               No                    14              2               1.0
  `span`       1         12     1         Yes                 15      ≤4       4.4               18               4                     14              ≤3.2            1.0
  `valign`     1         12     1         Yes                 15      3        4.4               18               4                     14              2               1.0
  `width`      1         12     1         Yes                 15      ≤4       4.4               18               4                     14              ≤3.2            1.0
:::

## See also {#see_also}

::: section-content
-   CSS properties and
    [pseudo-classes](https://developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-classes)
    that may be specially useful to style the `<col>` element:
    -   the
        [`width`](https://developer.mozilla.org/en-US/docs/Web/CSS/width)
        property to control the width of the column;
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
[https://developer.mozilla.org/en-US/docs/Web/HTML/Element/colgroup](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/colgroup){._attribution-link}
:::
