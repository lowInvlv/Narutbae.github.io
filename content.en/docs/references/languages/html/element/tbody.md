

# \<tbody\>: The Table Body element



::: section-content
The `<tbody>` [HTML](../index) element encapsulates a set of table rows
([`<tr>`](tr) elements), indicating that they comprise the body of the
table ([`<table>`](table)).
:::

## Try it {#try_it}

::: section-content
::: iframe
::: {.output-header .border-rounded-top}
#### HTML Demo: \<tbody\> {#html-demo-tbody .output-heading}

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
        Council budget (in £) 2018
      </caption>
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

The `<tbody>` element, along with its related [`<thead>`](thead) and
[`<tfoot>`](tfoot) elements, provide useful semantic information that
can be used when rendering for either screen or printer.

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
<td>Zero or more <a href="tr"><code>&lt;tr&gt;</code></a> elements.</td>
</tr>
<tr class="odd">
<th scope="row">Tag omission</th>
<td>A <code>&lt;tbody&gt;</code> element's start tag can be omitted if
the first thing inside the <code>&lt;tbody&gt;</code> element is a <a
href="tr"><code>&lt;tr&gt;</code></a> element, and if the element is not
immediately preceded by a <code>&lt;tbody&gt;</code>, <a
href="thead"><code>&lt;thead&gt;</code></a>, or <a
href="tfoot"><code>&lt;tfoot&gt;</code></a> element whose end tag has
been omitted. (It can't be omitted if the element is empty.) A
<code>&lt;tbody&gt;</code> element's end tag can be omitted if the
<code>&lt;tbody&gt;</code> element is immediately followed by a
<code>&lt;tbody&gt;</code> or <a
href="tfoot"><code>&lt;tfoot&gt;</code></a> element, or if there is no
more content in the parent element.</td>
</tr>
<tr class="even">
<th scope="row">Permitted parents</th>
<td>Within the required parent <a
href="table"><code>&lt;table&gt;</code></a> element, the
<code>&lt;tbody&gt;</code> element can be added after a <a
href="caption"><code>&lt;caption&gt;</code></a>, <a
href="colgroup"><code>&lt;colgroup&gt;</code></a>, and a <a
href="thead"><code>&lt;thead&gt;</code></a> element.</td>
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

## Attributes

::: section-content
This element includes the [global attributes](../global_attributes).
:::

### Deprecated attributes {#deprecated_attributes}

::: section-content

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

    As this attribute is deprecated, use the CSS
    [`text-align`](https://developer.mozilla.org/en-US/docs/Web/CSS/text-align)
    property instead.

    ::: {#sect1 .notecard .note}
    **Note:** The equivalent `text-align` property for the
    `align="char"` is not implemented in any browsers yet. See the
    [`text-align`\'s browser compatibility
    section](https://developer.mozilla.org/en-US/docs/Web/CSS/text-align#browser_compatibility)
    for the `<string>` value.
    :::

[`bgcolor`](#bgcolor) [Deprecated]{.visually-hidden}

:   The background color of the table. It is a [6-digit hexadecimal RGB
    code](https://developer.mozilla.org/en-US/docs/Web/CSS/hex-color),
    prefixed by a \'`#`\'. One of the predefined [color
    keywords](https://developer.mozilla.org/en-US/docs/Web/CSS/named-color)
    can also be used.

    As this attribute is deprecated, use the CSS
    [`background-color`](https://developer.mozilla.org/en-US/docs/Web/CSS/background-color)
    property instead.

[`char`](#char) [Deprecated]{.visually-hidden}

:   This attribute is used to set the character to align the cells in a
    column on. Typical values for this include a period (`.`) when
    attempting to align numbers or monetary values. If [`align`](#align)
    is not set to `char`, this attribute is ignored.

[`charoff`](#charoff) [Deprecated]{.visually-hidden}

:   This attribute is used to indicate the number of characters to
    offset the column data from the alignment characters specified by
    the `char` attribute.

[`valign`](#valign) [Deprecated]{.visually-hidden}

:   This attribute specifies the vertical alignment of the text within
    each row of cells of the table header. Possible values for this
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

    As this attribute is deprecated, use the CSS
    [`vertical-align`](https://developer.mozilla.org/en-US/docs/Web/CSS/vertical-align)
    property instead.
:::

## Usage notes {#usage_notes}

::: section-content
-   If the table includes a [`<thead>`](thead) block (to semantically
    identify a row of column headers), the `<tbody>` block *must* come
    after it.
-   If [`<tr>`](tr) elements are specified outside an existing `<tbody>`
    element, as direct children of the [`<table>`](table), these
    elements will be encapsulated by a separate `<tbody>` element
    generated by the browser.
-   When printing a document, the `<thead>` and [`<tfoot>`](tfoot)
    elements specify information that may be the same---or at least very
    similar---on every page of a multipage table, while the `<tbody>`
    element\'s contents generally will differ from page to page.
-   When a table is presented in a screen context (such as a window)
    which is not large enough to display the entire table, the [user
    agent](https://developer.mozilla.org/en-US/docs/Glossary/User_agent)
    may let the user scroll the contents of the `<thead>`, `<tbody>`,
    `<tfoot>`, and [`<caption>`](caption) blocks separately from one
    another for the same parent table.
-   You *may* use more than one `<tbody>` per table as long as they are
    all consecutive. This lets you divide the rows in large tables into
    sections, each of which may be separately formatted if so desired.
    If not marked up to be consecutive elements, browsers will correct
    this author error, ensuring any `<thead>` and `<tfoot>` elements are
    rendered as the first and last elements of the table, respectively.
:::

## Examples

::: section-content
Below are some examples showing the use of the `<tbody>` element. For
more examples of this element, see the examples for
[`<table>`](table#examples).
:::

### Basic example {#basic_example}

::: section-content
In this relatively simple example, we create a table containing
information about a group of students with a [`<thead>`](thead) and a
[`<tbody>`](tbody){aria-current="page"}, with a number of rows in the
body.

#### HTML

The table\'s HTML is shown here. Note that all the body cells including
information about students are contained within a single `<tbody>`
element.

::: code-example
[html]{.language-name}

``` {signature="qFb0zN6juxeSZ2o/sDmYvfb7FbHUv+0lqI4l3lTs988=" data-language="html"}
<table>
  <thead>
    <tr>
      <th>Student ID</th>
      <th>Name</th>
      <th>Major</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>3741255</td>
      <td>Jones, Martha</td>
      <td>Computer Science</td>
    </tr>
    <tr>
      <td>3971244</td>
      <td>Nim, Victor</td>
      <td>Russian Literature</td>
    </tr>
    <tr>
      <td>4100332</td>
      <td>Petrov, Alexandra</td>
      <td>Astrophysics</td>
    </tr>
  </tbody>
</table>
```
:::

#### CSS

The CSS to style our table is shown next.

::: code-example
[css]{.language-name}

``` {signature="hu3OWAcRnwZ3uRnmFFdvxIW6hZqSWORBnD4mGP/1Gf4=" data-language="css"}
table {
  border: 2px solid #555;
  border-collapse: collapse;
  font:
    16px "Lucida Grande",
    "Helvetica",
    "Arial",
    sans-serif;
}
```
:::

First, the table\'s overall style attributes are set, configuring the
thickness, style, and color of the table\'s exterior borders and using
[`border-collapse`](https://developer.mozilla.org/en-US/docs/Web/CSS/border-collapse)
to ensure that the border lines are shared among adjacent cells rather
than each having its own borders with space in between.
[`font`](https://developer.mozilla.org/en-US/docs/Web/CSS/font) is used
to establish an initial font for the table.

::: code-example
[css]{.language-name}

``` {signature="Njc3ARIanP/NEW7S8NEZLhBb1mpHKEqJatFNXT0nizA=" data-language="css"}
th,
td {
  border: 1px solid #bbb;
  padding: 2px 8px 0;
  text-align: left;
}
```
:::

Then the style is set for the majority of the cells in the table,
including all data cells but also those styles shared between our
[`<td>`](td) and [`<th>`](th) cells. The cells are given a light gray
outline which is a single pixel thick, padding is adjusted, and all
cells are left-aligned using
[`text-align`](https://developer.mozilla.org/en-US/docs/Web/CSS/text-align)

::: code-example
[css]{.language-name}

``` {signature="pTll3YqtLNvZflvBqdRZekXMNmjPmrI9ZcSxrc+jqCY=" data-language="css"}
thead > tr > th {
  background-color: #cce;
  font-size: 18px;
  border-bottom: 2px solid #999;
}
```
:::

Finally, header cells contained within the [`<thead>`](thead) element
are given additional styling. They use a darker
[`background-color`](https://developer.mozilla.org/en-US/docs/Web/CSS/background-color),
a larger font size, and a thicker, darker bottom border than the other
cell borders.

#### Result

The resulting table looks like this:

::: {#sect2 .code-example}
::: iframe
:::
:::
:::

### Multiple bodies {#multiple_bodies}

::: section-content
You can create row groupings within a table by using multiple `<tbody>`
elements. Each may potentially have its own header row or rows; however,
*there can be only one [`<thead>`](thead) per table!* Because of that,
you need to use a [`<tr>`](tr) filled with [`<th>`](th) elements to
create headers within each `<tbody>`. Let\'s see how that\'s done.

Let\'s take the previous example, add some more students to the list,
and update the table so that instead of listing each student\'s major on
every row, the students are grouped by major, with heading rows for each
major.

#### Result {#result_2}

First, the resulting table, so you know what we\'re building:

::: {#sect3 .code-example}
::: iframe
:::
:::

#### HTML {#html_2}

The revised HTML looks like this:

::: code-example
[html]{.language-name}

``` {signature="zxZQjptYuUSiwymia6bCfo3SO7/IOIBbqyJccBvLYY4=" data-language="html"}
<table>
  <thead>
    <tr>
      <th>Student ID</th>
      <th>Name</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th colspan="2">Computer Science</th>
    </tr>
    <tr>
      <td>3741255</td>
      <td>Jones, Martha</td>
    </tr>
    <tr>
      <td>4077830</td>
      <td>Pierce, Benjamin</td>
    </tr>
    <tr>
      <td>5151701</td>
      <td>Kirk, James</td>
    </tr>
  </tbody>
  <tbody>
    <tr>
      <th colspan="2">Russian Literature</th>
    </tr>
    <tr>
      <td>3971244</td>
      <td>Nim, Victor</td>
    </tr>
  </tbody>
  <tbody>
    <tr>
      <th colspan="2">Astrophysics</th>
    </tr>
    <tr>
      <td>4100332</td>
      <td>Petrov, Alexandra</td>
    </tr>
    <tr>
      <td>8892377</td>
      <td>Toyota, Hiroko</td>
    </tr>
  </tbody>
</table>
```
:::

Notice that each major is placed in a separate `<tbody>` block, the
first row of which contains a single [`<th>`](th) element with a
[`colspan`](#colspan) attribute that spans the entire width of the
table. That heading lists the name of the major contained within the
`<tbody>`.

Then each remaining row in each major\'s `<tbody>` consists of two
cells: the first for the student\'s ID and the second for their name.

#### CSS {#css_2}

Most of the CSS is unchanged. We do, however, add a slightly more subtle
style for header cells contained directly within a `<tbody>` (as opposed
to those which reside in a [`<thead>`](thead)). This is used for the
headers indicating each table section\'s corresponding major.

::: code-example
[css]{.language-name}

``` {signature="qU/Xb0tdpYOyX1Zq/gc47rXCnzuRxf9bwtwB8PZJ1cU=" data-language="css"}
tbody > tr > th {
  background-color: #dde;
  border-bottom: 1.5px solid #bbb;
  font-weight: normal;
}
```
:::
:::

## Specifications

::: _table
  ---------------------------------------------------------------------------------------------------
  Specification
  ---------------------------------------------------------------------------------------------------
  [HTML Standard\
  [\#
  the-tbody-element]{.small}](https://html.spec.whatwg.org/multipage/tables.html#the-tbody-element)

  ---------------------------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
              Desktop                                                         Mobile                                                                                   
  ----------- --------- ------ --------- ------------------- ------- -------- ----------------- ---------------- --------------------- --------------- --------------- ------------------
              Chrome    Edge   Firefox   Internet Explorer   Opera   Safari   WebView Android   Chrome Android   Firefox for Android   Opera Android   Safari on IOS   Samsung Internet
  `tbody`     1         12     1         Yes                 ≤12.1   1        4.4               18               4                     ≤12.1           1               1.0
  `align`     1         12     1         Yes                 15      3        4.4               18               4                     14              2               1.0
  `bgcolor`   1         12     1         Yes                 ≤15     1        4.4               18               4                     ≤14             1               1.0
  `char`      1         12     No        Yes                 15      ≤4       4.4               18               No                    14              ≤3.2            1.0
  `charoff`   1         12     1         Yes                 15      ≤4       4.4               18               4                     14              ≤3.2            1.0
  `valign`    1         12     1         Yes                 15      3        4.4               18               4                     14              2               1.0
:::

## See also {#see_also}

::: section-content
-   CSS properties and
    [pseudo-classes](https://developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-classes)
    that may be specially useful to style the `<tbody>` element:
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
[https://developer.mozilla.org/en-US/docs/Web/HTML/Element/tbody](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/tbody){._attribution-link}
:::
