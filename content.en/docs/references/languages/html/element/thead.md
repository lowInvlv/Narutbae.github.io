

# \<thead\>: The Table Head element



::: section-content
The `<thead>` [HTML](../index) element defines a set of rows defining
the head of the columns of the table.
:::

## Try it {#try_it}

::: section-content
::: iframe
::: {.output-header .border-rounded-top}
#### HTML Demo: \<thead\> {#html-demo-thead .output-heading}

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
          <th scope="col">Items</th>
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

    ::: {#sect1 .notecard .warning}
    **Warning:** Do not use this attribute as it is obsolete (not
    supported) in the latest standard.

    -   To align values, use the CSS
        [`text-align`](https://developer.mozilla.org/en-US/docs/Web/CSS/text-align)
        property instead.
    :::

[`bgcolor`](#bgcolor) [Deprecated]{.visually-hidden}

:   This attribute defines the background color of each column cell. It
    accepts a 6-digit hexadecimal color or a named color. Alpha
    transparency is not supported.

    ::: {#sect2 .notecard .note}
    **Note:** Do not use this attribute, as it is non-standard. The
    `thead` element should be styled using the CSS
    [`background-color`](https://developer.mozilla.org/en-US/docs/Web/CSS/background-color)
    property, which can be applied to any element, including the
    `thead`, [`<tr>`](tr), [`<td>`](td) and [`<th>`](th) elements.
    :::

[`char`](#char) [Deprecated]{.visually-hidden}

:   This attribute is used to set the character to align the cells in a
    column on. Typical values for this include a period (.) when
    attempting to align numbers or monetary values. If [`align`](#align)
    is not set to `char`, this attribute is ignored.

    ::: {#sect3 .notecard .note}
    **Note:** Do not use this attribute as it is obsolete (and not
    supported) in the latest standard.
    :::

[`charoff`](#charoff) [Deprecated]{.visually-hidden}

:   This attribute is used to indicate the number of characters to
    offset the column data from the alignment characters specified by
    the **char** attribute.

    ::: {#sect4 .notecard .note}
    **Note:** Do not use this attribute as it is obsolete (and not
    supported) in the latest standard.
    :::

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
    -   `top`, which will put the text as close to the top of the cell
        as it is possible.

    ::: {#sect5 .notecard .note}
    **Note:** Do not use this attribute as it is obsolete (and not
    supported) in the latest standard: instead set the CSS
    [`vertical-align`](https://developer.mozilla.org/en-US/docs/Web/CSS/vertical-align)
    property on it.
    :::
:::

## Examples

::: section-content
See [`<table>`](table) for examples on `<thead>`.
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
<td>Zero or more <a href="tr"><code>&lt;tr&gt;</code></a> elements.</td>
</tr>
<tr class="odd">
<th scope="row">Tag omission</th>
<td>The start tag is mandatory. The end tag may be omitted if the <a
href="thead" aria-current="page"><code>&lt;thead&gt;</code></a> element
is immediately followed by a <a
href="tbody"><code>&lt;tbody&gt;</code></a> or <a
href="tfoot"><code>&lt;tfoot&gt;</code></a> element.</td>
</tr>
<tr class="even">
<th scope="row">Permitted parents</th>
<td>A <a href="table"><code>&lt;table&gt;</code></a> element. The <a
href="thead" aria-current="page"><code>&lt;thead&gt;</code></a> must
appear after any <a href="caption"><code>&lt;caption&gt;</code></a> or
<a href="colgroup"><code>&lt;colgroup&gt;</code></a> element, even
implicitly defined, but before any <a
href="tbody"><code>&lt;tbody&gt;</code></a>, <a
href="tfoot"><code>&lt;tfoot&gt;</code></a> and <a
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
  the-thead-element]{.small}](https://html.spec.whatwg.org/multipage/tables.html#the-thead-element)

  ---------------------------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
  ----------------------------------------------------------------------------------------------------------------------------------------------------------------
              Desktop                                                                 Mobile                                                            
  ----------- --------- ------ --------- ---------- ------- ------------------------- --------- --------- --------- --------- ------------------------- ----------
              Chrome    Edge   Firefox   Internet   Opera   Safari                    WebView   Chrome    Firefox   Opera     Safari on IOS             Samsung
                                         Explorer                                     Android   Android   for       Android                             Internet
                                                                                                          Android                                       

  `thead`     1         12     1         Yes        ≤12.1   1                         4.4       18        4         ≤12.1     1                         1.0
                                                                                                                                                        
                                                            Backgrounds applied to                                            Backgrounds applied to    
                                                            `<thead>` elements will                                           `<thead>` elements will   
                                                            be applied to each table                                          be applied to each table  
                                                            cell, rather than the                                             cell, rather than the     
                                                            entire header. To mimic                                           entire header. To mimic   
                                                            the behavior of other                                             the behavior of other     
                                                            browsers, set the                                                 browsers, set the         
                                                            `background-attachment`                                           `background-attachment`   
                                                            CSS property to `fixed`.                                          CSS property to `fixed`.  

  `align`     1         12     1         Yes        15      3                         4.4       18        4         14        2                         1.0

  `bgcolor`   1         12     1         Yes        ≤15     1                         4.4       18        4         ≤14       1                         1.0

  `char`      1         12     No        Yes        15      ≤4                        4.4       18        No        14        ≤3.2                      1.0

  `charoff`   1         12     1         Yes        15      ≤4                        4.4       18        4         14        ≤3.2                      1.0

  `valign`    1         12     1         Yes        15      3                         4.4       18        4         14        2                         1.0
  ----------------------------------------------------------------------------------------------------------------------------------------------------------------
:::

## See also {#see_also}

::: section-content
-   Other table-related HTML Elements: [`<caption>`](caption),
    [`<col>`](col), [`<colgroup>`](colgroup), [`<table>`](table),
    [`<tbody>`](tbody), [`<td>`](td), [`<tfoot>`](tfoot), [`<th>`](th),
    [`<tr>`](tr);
-   CSS properties and pseudo-classes that may be specially useful to
    style the `<thead>` element:
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
[https://developer.mozilla.org/en-US/docs/Web/HTML/Element/thead](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/thead){._attribution-link}
:::
