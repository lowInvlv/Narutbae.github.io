

# \<table\>: The Table element



::: section-content
The `<table>` [HTML](../index) element represents tabular data --- that
is, information presented in a two-dimensional table comprised of rows
and columns of cells containing data.
:::

## Try it {#try_it}

::: section-content
::: iframe
::: {.output-header .border-rounded-top}
#### HTML Demo: \<table\> {#html-demo-table .output-heading}

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
    <table>
      <thead>
        <tr>
          <th colspan="2">The table header</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td>The table body</td>
          <td>with two columns</td>
        </tr>
      </tbody>
    </table>
:::
:::

::: {#css-panel .section .hidden tabindex="0" role="tabpanel" aria-labelledby="css" aria-hidden="true"}
::: {#css-editor}
    table,
    td {
      border: 1px solid #333;
    }

    thead,
    tfoot {
      background-color: #333;
      color: #fff;
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
<td><a href="../content_categories#flow_content">Flow content</a></td>
</tr>
<tr class="even">
<th scope="row">Permitted content</th>
<td>In this order:
<ol>
<li>an optional <a href="caption"><code>&lt;caption&gt;</code></a>
element,</li>
<li>zero or more <a href="colgroup"><code>&lt;colgroup&gt;</code></a>
elements,</li>
<li>an optional <a href="thead"><code>&lt;thead&gt;</code></a>
element,</li>
<li>either one of the following:
<ul>
<li>zero or more <a href="tbody"><code>&lt;tbody&gt;</code></a>
elements</li>
<li>one or more <a href="tr"><code>&lt;tr&gt;</code></a> elements</li>
</ul></li>
<li>an optional <a href="tfoot"><code>&lt;tfoot&gt;</code></a>
element</li>
</ol></td>
</tr>
<tr class="odd">
<th scope="row">Tag omission</th>
<td>None, both the starting and ending tag are mandatory.</td>
</tr>
<tr class="even">
<th scope="row">Permitted parents</th>
<td>Any element that accepts flow content</td>
</tr>
<tr class="odd">
<th scope="row">Implicit ARIA role</th>
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/table_role"><code>table</code></a></td>
</tr>
<tr class="even">
<th scope="row">Permitted ARIA roles</th>
<td>Any</td>
</tr>
<tr class="odd">
<th scope="row">DOM interface</th>
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLTableElement"><code>HTMLTableElement</code></a></td>
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
    attribute indicates how the table must be aligned inside the
    containing document. It may have the following values:

    -   `left`: the table is displayed on the left side of the document;
    -   `center`: the table is displayed in the center of the document;
    -   `right`: the table is displayed on the right side of the
        document.

    Set
    [`margin-left`](https://developer.mozilla.org/en-US/docs/Web/CSS/margin-left)
    and
    [`margin-right`](https://developer.mozilla.org/en-US/docs/Web/CSS/margin-right)
    to achieve an effect that is similar to the align attribute:

    -   `left`: `margin-right: auto; margin-left: 0;`
    -   `center`: `margin-right: auto; margin-left: auto;`
    -   `right`: `margin-right: 0; margin-left: auto;`

[`bgcolor`](#bgcolor) [Deprecated]{.visually-hidden}

:   The background color of the table. It is a [6-digit hexadecimal RGB
    code](https://developer.mozilla.org/en-US/docs/Web/CSS/hex-color),
    prefixed by a \'`#`\'. One of the predefined [color
    keywords](https://developer.mozilla.org/en-US/docs/Web/CSS/named-color)
    can also be used.

    To achieve a similar effect, use the CSS
    [`background-color`](https://developer.mozilla.org/en-US/docs/Web/CSS/background-color)
    property.

[`border`](#border) [Deprecated]{.visually-hidden}

:   This integer attribute defines, in pixels, the size of the frame
    surrounding the table. If set to 0, the [`frame`](#frame) attribute
    is set to void.

    To achieve a similar effect, use the CSS
    [`border`](https://developer.mozilla.org/en-US/docs/Web/CSS/border)
    shorthand property.

[`cellpadding`](#cellpadding) [Deprecated]{.visually-hidden}

:   This attribute defines the space between the content of a cell and
    its border, displayed or not. If the cellpadding\'s length is
    defined in pixels, this pixel-sized space will be applied to all
    four sides of the cell\'s content. If the length is defined using a
    percentage value, the content will be centered and the total
    vertical space (top and bottom) will represent this value. The same
    is true for the total horizontal space (left and right).

    To achieve a similar effect, apply the
    [`border-collapse`](https://developer.mozilla.org/en-US/docs/Web/CSS/border-collapse)
    property to the `<table>` element, with its value set to collapse,
    and the
    [`padding`](https://developer.mozilla.org/en-US/docs/Web/CSS/padding)
    property to the [`<td>`](td) elements.

[`cellspacing`](#cellspacing) [Deprecated]{.visually-hidden}

:   This attribute defines the size of the space between two cells in a
    percentage value or pixels. The attribute is applied both
    horizontally and vertically, to the space between the top of the
    table and the cells of the first row, the left of the table and the
    first column, the right of the table and the last column and the
    bottom of the table and the last row.

    To achieve a similar effect, apply the
    [`border-spacing`](https://developer.mozilla.org/en-US/docs/Web/CSS/border-spacing)
    property to the `<table>` element. `border-spacing` does not have
    any effect if
    [`border-collapse`](https://developer.mozilla.org/en-US/docs/Web/CSS/border-collapse)
    is set to collapse.

[`frame`](#frame) [Deprecated]{.visually-hidden}

:   This enumerated attribute defines which side of the frame
    surrounding the table must be displayed.

    To achieve a similar effect, use the
    [`border-style`](https://developer.mozilla.org/en-US/docs/Web/CSS/border-style)
    and
    [`border-width`](https://developer.mozilla.org/en-US/docs/Web/CSS/border-width)
    properties.

[`rules`](#rules) [Deprecated]{.visually-hidden}

:   This enumerated attribute defines where rules, i.e. lines, should
    appear in a table. It can have the following values:

    -   `none`, which indicates that no rules will be displayed; it is
        the default value;
    -   `groups`, which will cause the rules to be displayed between row
        groups (defined by the [`<thead>`](thead), [`<tbody>`](tbody)
        and [`<tfoot>`](tfoot) elements) and between column groups
        (defined by the [`<col>`](col) and [`<colgroup>`](colgroup)
        elements) only;
    -   `rows`, which will cause the rules to be displayed between rows;
    -   `cols`, which will cause the rules to be displayed between
        columns;
    -   `all`, which will cause the rules to be displayed between rows
        and columns.

    To achieve a similar effect, apply the
    [`border`](https://developer.mozilla.org/en-US/docs/Web/CSS/border)
    property to the appropriate [`<thead>`](thead), [`<tbody>`](tbody),
    [`<tfoot>`](tfoot), [`<col>`](col), or [`<colgroup>`](colgroup)
    elements.

[`summary`](#summary) [Deprecated]{.visually-hidden}

:   This attribute defines an alternative text that summarizes the
    content of the table. Use the [`<caption>`](caption) element
    instead.

[`width`](#width) [Deprecated]{.visually-hidden}

:   This attribute defines the width of the table. Use the CSS
    [`width`](https://developer.mozilla.org/en-US/docs/Web/CSS/width)
    property instead.

::: {#sect1 .notecard .note}
**Note:** While no HTML specification includes `height` as a `<table>`
attribute, some browsers support a non-standard interpretation of
`height`. The unitless value sets a minimum absolute height in pixels.
If set as a percent value, the minimum table height will be relative to
the height of the parent container.
:::
:::

## Examples

### Simple table {#simple_table}

::: section-content
::: code-example
[html]{.language-name}

``` {signature="kpTqedh9NYGmaj1F12OvnMO9OKIMOL91fmyFs5Ifox8=" data-language="html"}
<table>
  <tr>
    <td>John</td>
    <td>Doe</td>
  </tr>
  <tr>
    <td>Jane</td>
    <td>Doe</td>
  </tr>
</table>
```
:::

#### Result

::: {#sect2 .code-example}
::: iframe
:::
:::
:::

### Further simple examples {#further_simple_examples}

::: section-content
::: code-example
[html]{.language-name}

``` {signature="EGFuvN15xKajLKjgia1PUuXiowlmmIbnkk/NufiVPUQ=" data-language="html"}
<p>Simple table with header</p>
<table>
  <tr>
    <th>First name</th>
    <th>Last name</th>
  </tr>
  <tr>
    <td>John</td>
    <td>Doe</td>
  </tr>
  <tr>
    <td>Jane</td>
    <td>Doe</td>
  </tr>
</table>

<p>Table with thead, tfoot, and tbody</p>
<table>
  <thead>
    <tr>
      <th>Header content 1</th>
      <th>Header content 2</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Body content 1</td>
      <td>Body content 2</td>
    </tr>
  </tbody>
  <tfoot>
    <tr>
      <td>Footer content 1</td>
      <td>Footer content 2</td>
    </tr>
  </tfoot>
</table>

<p>Table with colgroup</p>
<table>
  <colgroup span="4"></colgroup>
  <tr>
    <th>Countries</th>
    <th>Capitals</th>
    <th>Population</th>
    <th>Language</th>
  </tr>
  <tr>
    <td>USA</td>
    <td>Washington, D.C.</td>
    <td>309 million</td>
    <td>English</td>
  </tr>
  <tr>
    <td>Sweden</td>
    <td>Stockholm</td>
    <td>9 million</td>
    <td>Swedish</td>
  </tr>
</table>

<p>Table with colgroup and col</p>
<table>
  <colgroup>
    <col style="background-color: #0f0" />
    <col span="2" />
  </colgroup>
  <tr>
    <th>Lime</th>
    <th>Lemon</th>
    <th>Orange</th>
  </tr>
  <tr>
    <td>Green</td>
    <td>Yellow</td>
    <td>Orange</td>
  </tr>
</table>

<p>Simple table with caption</p>
<table>
  <caption>
    Awesome caption
  </caption>
  <tr>
    <td>Awesome data</td>
  </tr>
</table>
```
:::

#### Result {#result_2}

::: {#sect3 .code-example}
::: iframe
:::
:::
:::

### Table sorting {#table_sorting}

::: section-content
#### Sorting table rows {#sorting_table_rows}

There are no native methods for sorting the rows ([`<tr>`](tr) elements)
of an HTML table. But using
[`Array.prototype.slice()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/slice),
[`Array.prototype.sort()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/sort),
[`Node.removeChild()`](https://developer.mozilla.org/en-US/docs/Web/API/Node/removeChild),
and
[`Node.appendChild()`](https://developer.mozilla.org/en-US/docs/Web/API/Node/appendChild),
you can implement your own `sort()` function to sort an
[`HTMLCollection`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLCollection)
of `<tr>` elements.

In the below example, you can see such an example. We are attaching it
to the \<tbody\> element so that it sorts the table cells in order of
increasing value, and updates the display to suit.

##### HTML

::: code-example
[html]{.language-name}

``` {signature="VZmKtEBq36tGgDWrmDDGkf/e0pLsgVbrKCcAVGo8OhY=" data-language="html"}
<table>
  <tbody>
    <tr>
      <td>3</td>
    </tr>
    <tr>
      <td>2</td>
    </tr>
    <tr>
      <td>1</td>
    </tr>
  </tbody>
</table>
```
:::

##### JavaScript

::: code-example
[js]{.language-name}

``` {signature="dOThlPMdSGOOExVEjgO6MryPddJ1EKzlz5k0A+5FpPM=" data-language="js"}
HTMLTableSectionElement.prototype.sort = function (cb) {
  Array.from(this.rows)
    .sort(cb)
    .forEach((e) => this.appendChild(this.removeChild(e)));
};

document
  .querySelector("table")
  .tBodies[0].sort((a, b) => a.textContent.localeCompare(b.textContent));
```
:::

##### Result {#result_3}

::: {#sect4 .code-example}
::: iframe
:::
:::

#### Sorting rows with a click on the th element {#sorting_rows_with_a_click_on_the_th_element}

The following example adds an event handler to every `<th>` element of
every `<table>` in the `document`; it sorts all the `<tbody>`\'s rows,
basing the sorting on the `td` cells contained in the rows.

::: {#sect5 .notecard .note}
**Note:** This solution assumes that the `<td>` elements are populated
by raw text with no descendant elements.
:::

##### HTML {#html_2}

::: code-example
[html]{.language-name}

``` {signature="5pE6zE/QZjoBhsJjPd2Q0PFTSehUCePvBbVZ6zfoluk=" data-language="html"}
<table>
  <thead>
    <tr>
      <th>Numbers</th>
      <th>Letters</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>3</td>
      <td>A</td>
    </tr>
    <tr>
      <td>2</td>
      <td>B</td>
    </tr>
    <tr>
      <td>1</td>
      <td>C</td>
    </tr>
  </tbody>
</table>
```
:::

##### JavaScript {#javascript_2}

::: code-example
[js]{.language-name}

``` {signature="utDiAEghfzxvAuqOKqIOowGZDlmU+IxSTBH+OJvIL9k=" data-language="js"}
const allTables = document.querySelectorAll("table");

for (const table of allTables) {
  const tBody = table.tBodies[0];
  const rows = Array.from(tBody.rows);
  const headerCells = table.tHead.rows[0].cells;

  for (const th of headerCells) {
    const cellIndex = th.cellIndex;

    th.addEventListener("click", () => {
      rows.sort((tr1, tr2) => {
        const tr1Text = tr1.cells[cellIndex].textContent;
        const tr2Text = tr2.cells[cellIndex].textContent;
        return tr1Text.localeCompare(tr2Text);
      });

      tBody.append(...rows);
    });
  }
}
```
:::

##### Result {#result_4}

::: {#sect6 .code-example}
::: iframe
:::
:::
:::

### Displaying large tables in small spaces {#displaying_large_tables_in_small_spaces}

::: section-content
A common issue with tables on the web is that they don\'t natively work
very well on small screens when the amount of content is large, and the
way to make them scrollable isn\'t obvious, especially when the markup
may come from a CMS and cannot be modified to have a wrapper.

This example provides one way to display tables in small spaces. We\'ve
hidden the HTML content as it is very large, and there is nothing
remarkable about it. The CSS is more useful to inspect in this example.

When looking at these styles you\'ll notice that table\'s
[`display`](https://developer.mozilla.org/en-US/docs/Web/CSS/display)
property has been set to `block`. While this allows scrolling, the table
loses some of its integrity, and table cells try to become as small as
possible. To mitigate this issue we\'ve set
[`white-space`](https://developer.mozilla.org/en-US/docs/Web/CSS/white-space)
to `nowrap` on the `<tbody>`. However, we don\'t do this for the
`<thead>` to avoid long titles forcing columns to be wider than they
need to be to display the data.

To keep the table headers on the page while scrolling down we\'ve set
[`position`](https://developer.mozilla.org/en-US/docs/Web/CSS/position)
to sticky on the `<th>` elements. Note that we have **not** set
[`border-collapse`](https://developer.mozilla.org/en-US/docs/Web/CSS/border-collapse)
to `collapse`, as if we do the header cannot be separated correctly from
the rest of the table.

::: code-example
[css]{.language-name}

``` {signature="s30Co5tpcKfokyJYnnMST58XtkB3X/BuPKgCYy5t3FA=" data-language="css"}
table,
th,
td {
  border: 1px solid;
}

table {
  width: 100%;
  max-width: 400px;
  height: 240px;
  margin: 0 auto;
  display: block;
  overflow-x: auto;
  border-spacing: 0;
}

tbody {
  white-space: nowrap;
}

th,
td {
  padding: 5px 10px;
  border-top-width: 0;
  border-left-width: 0;
}

th {
  position: sticky;
  top: 0;
  background: #fff;
  vertical-align: bottom;
}

th:last-child,
td:last-child {
  border-right-width: 0;
}

tr:last-child td {
  border-bottom-width: 0;
}
```
:::

#### Result {#result_5}

::: {#sect7 .code-example}
::: iframe
:::
:::
:::

## Accessibility concerns {#accessibility_concerns}

### Captions

::: section-content
By supplying a [`<caption>`](caption) element whose value clearly and
concisely describes the table\'s purpose, it helps the people decide if
they need to read the rest of the table content or skip over it.

This helps people navigating with the aid of assistive technology such
as a screen reader, people experiencing low vision conditions, and
people with cognitive concerns.

-   [MDN Adding a caption to your table with
    \<caption\>](https://developer.mozilla.org/en-US/docs/Learn/HTML/Tables/Advanced#adding_a_caption_to_your_table_with_caption)
-   [Caption & Summary • Tables • W3C WAI Web Accessibility
    Tutorials](https://www.w3.org/WAI/tutorials/tables/caption-summary/){target="_blank"}
:::

### Scoping rows and columns {#scoping_rows_and_columns}

::: section-content
The [`scope`](th#scope) attribute on header elements is redundant in
simple contexts, because scope is inferred. However, some assistive
technologies may fail to draw correct inferences, so specifying header
scope may improve user experiences. In complex tables, scope can be
specified to provide necessary information about the cells related to a
header.

#### Examples {#examples_2}

::: code-example
[html]{.language-name}

``` {signature="2Sq+7iq+Zy9x7lNZSQn3XOhjEC2/Cg/dbsIBwcbE7JU=" data-language="html"}
<table>
  <caption>
    Color names and values
  </caption>
  <tbody>
    <tr>
      <th scope="col">Name</th>
      <th scope="col">HEX</th>
      <th scope="col">HSLa</th>
      <th scope="col">RGBa</th>
    </tr>
    <tr>
      <th scope="row">Teal</th>
      <td><code>#51F6F6</code></td>
      <td><code>hsl(180 90% 64% / 1)</code></td>
      <td><code>rgb(81 246 246 / 1)</code></td>
    </tr>
    <tr>
      <th scope="row">Goldenrod</th>
      <td><code>#F6BC57</code></td>
      <td><code>hsl(38 90% 65% / 1)</code></td>
      <td><code>rgba(246 188 87 / 1)</code></td>
    </tr>
  </tbody>
</table>
```
:::

##### Result {#result_6}

::: {#sect8 .code-example}
::: iframe
:::
:::

Providing a declaration of `scope="col"` on a [`<th>`](th) element will
help describe that the cell is at the top of a column. Providing a
declaration of `scope="row"` on a [`<th>`](th) element will help
describe that the cell is the first in a row.

-   [MDN Tables for visually impaired
    users](https://developer.mozilla.org/en-US/docs/Learn/HTML/Tables/Advanced#tables_for_visually_impaired_users)
-   [Tables with two headers • Tables • W3C WAI Web Accessibility
    Tutorials](https://www.w3.org/WAI/tutorials/tables/two-headers/){target="_blank"}
-   [Tables with irregular headers • Tables • W3C WAI Web Accessibility
    Tutorials](https://www.w3.org/WAI/tutorials/tables/irregular/){target="_blank"}
-   [H63: Using the scope attribute to associate header cells and data
    cells in data tables \| W3C Techniques for WCAG
    2.0](https://www.w3.org/TR/WCAG20-TECHS/H63.html){target="_blank"}
:::

### Complicated tables {#complicated_tables}

::: section-content
Assistive technology such as screen readers may have difficulty parsing
tables that are so complex that header cells can\'t be associated in a
strictly horizontal or vertical way. This is typically indicated by the
presence of the [`colspan`](td#colspan) and [`rowspan`](td#rowspan)
attributes.

Ideally, consider alternate ways to present the table\'s content,
including breaking it apart into a collection of smaller, related tables
that don\'t have to rely on using the `colspan` and `rowspan`
attributes. In addition to helping people who use assistive technology
understand the table\'s content, this may also benefit people with
cognitive concerns who may have difficulty understanding the
associations the table layout is describing.

If the table cannot be broken apart, use a combination of the
[`id`](../global_attributes#id) and [`headers`](td#headers) attributes
to programmatically associate each table cell with the header(s) the
cell is associated with.

-   [MDN Tables for visually impaired
    users](https://developer.mozilla.org/en-US/docs/Learn/HTML/Tables/Advanced#tables_for_visually_impaired_users)
-   [Tables with multi-level headers • Tables • W3C WAI Web
    Accessibility
    Tutorials](https://www.w3.org/WAI/tutorials/tables/multi-level/){target="_blank"}
-   [H43: Using id and headers attributes to associate data cells with
    header cells in data tables \| Techniques for W3C WCAG
    2.0](https://www.w3.org/TR/WCAG20-TECHS/H43.html){target="_blank"}
:::

## Specifications

::: _table
  ---------------------------------------------------------------------------------------------------
  Specification
  ---------------------------------------------------------------------------------------------------
  [HTML Standard\
  [\#
  the-table-element]{.small}](https://html.spec.whatwg.org/multipage/tables.html#the-table-element)

  ---------------------------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
                  Desktop                                                         Mobile                                                                                   
  --------------- --------- ------ --------- ------------------- ------- -------- ----------------- ---------------- --------------------- --------------- --------------- ------------------
                  Chrome    Edge   Firefox   Internet Explorer   Opera   Safari   WebView Android   Chrome Android   Firefox for Android   Opera Android   Safari on IOS   Samsung Internet
  `table`         1         12     1         Yes                 ≤12.1   1        4.4               18               4                     ≤12.1           1               1.0
  `align`         1         12     1         Yes                 ≤12.1   1        4.4               18               4                     ≤12.1           1               1.0
  `bgcolor`       1         12     1         Yes                 ≤12.1   1        4.4               18               4                     ≤12.1           1               1.0
  `border`        1         12     1         Yes                 ≤12.1   1        4.4               18               4                     ≤12.1           1               1.0
  `cellpadding`   1         12     1         Yes                 ≤12.1   1        4.4               18               4                     ≤12.1           1               1.0
  `cellspacing`   1         12     1         Yes                 ≤12.1   1        4.4               18               4                     ≤12.1           1               1.0
  `frame`         1         12     1         Yes                 ≤12.1   1        4.4               18               4                     ≤12.1           1               1.0
  `rules`         1         12     1         Yes                 ≤12.1   1        4.4               18               4                     ≤12.1           1               1.0
  `summary`       1         12     1         Yes                 ≤12.1   1        4.4               18               4                     ≤12.1           1               1.0
  `width`         1         12     1         Yes                 ≤12.1   1        4.4               18               4                     ≤12.1           1               1.0
:::

## See also {#see_also}

::: section-content
-   [HTML data table
    tutorial](https://developer.mozilla.org/en-US/docs/Learn/HTML/Tables)
-   CSS properties that may be especially useful to style the `<table>`
    element:
    -   [`width`](https://developer.mozilla.org/en-US/docs/Web/CSS/width)
        to control the width of the table;
    -   [`border`](https://developer.mozilla.org/en-US/docs/Web/CSS/border),
        [`border-style`](https://developer.mozilla.org/en-US/docs/Web/CSS/border-style),
        [`border-color`](https://developer.mozilla.org/en-US/docs/Web/CSS/border-color),
        [`border-width`](https://developer.mozilla.org/en-US/docs/Web/CSS/border-width),
        [`border-collapse`](https://developer.mozilla.org/en-US/docs/Web/CSS/border-collapse),
        [`border-spacing`](https://developer.mozilla.org/en-US/docs/Web/CSS/border-spacing)
        to control the aspect of cell borders, rules, and frame;
    -   [`margin`](https://developer.mozilla.org/en-US/docs/Web/CSS/margin)
        and
        [`padding`](https://developer.mozilla.org/en-US/docs/Web/CSS/padding)
        to style the individual cell content;
    -   [`text-align`](https://developer.mozilla.org/en-US/docs/Web/CSS/text-align)
        and
        [`vertical-align`](https://developer.mozilla.org/en-US/docs/Web/CSS/vertical-align)
        to define the alignment of text and cell content.
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Element/table](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/table){._attribution-link}
:::
