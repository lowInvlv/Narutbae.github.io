

# \<caption\>: The Table Caption element



::: section-content
The `<caption>` [HTML](../index) element specifies the caption (or
title) of a table.
:::

## Try it {#try_it}

::: section-content
::: iframe
::: {.output-header .border-rounded-top}
#### HTML Demo: \<caption\> {#html-demo-caption .output-heading}

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
        He-Man and Skeletor facts
      </caption>
      <tr>
        <td> </td>
        <th scope="col" class="heman">He-Man</th>
        <th scope="col" class="skeletor">Skeletor</th>
      </tr>
      <tr>
        <th scope="row">Role</th>
        <td>Hero</td>
        <td>Villain</td>
      </tr>
      <tr>
        <th scope="row">Weapon</th>
        <td>Power Sword</td>
        <td>Havoc Staff</td>
      </tr>
      <tr>
        <th scope="row">Dark secret</th>
        <td>Expert florist</td>
        <td>Cries at romcoms</td>
      </tr>
    </table>
:::
:::

::: {#css-panel .section .hidden tabindex="0" role="tabpanel" aria-labelledby="css" aria-hidden="true"}
::: {#css-editor}
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
      padding: 7px 5px;
    }

    th {
      background-color: rgb(235, 235, 235);
    }

    td {
      text-align: center;
    }

    tr:nth-child(even) td {
      background-color: rgb(250, 250, 250);
    }

    tr:nth-child(odd) td {
      background-color: rgb(240, 240, 240);
    }

    .heman {
      font: 1.4rem molot;
      text-shadow:
        1px 1px 1px #fff,
        2px 2px 1px #000;
    }

    .skeletor {
      font: 1.7rem rapscallion;
      letter-spacing: 3px;
      text-shadow:
        1px 1px 0 #fff,
        0 0 9px #000;
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
    attribute indicates how the caption must be aligned with respect to
    the table. It may have one of the following values:

    [`left`](#left)

    :   The caption is displayed to the left of the table.

    [`top`](#top)

    :   The caption is displayed above the table.

    [`right`](#right)

    :   The caption is displayed to the right of the table.

    [`bottom`](#bottom)

    :   The caption is displayed below the table.

    ::: {#sect1 .notecard .warning}
    **Warning:** Do not use this attribute, as it has been deprecated.
    The [`<caption>`](caption){aria-current="page"} element should be
    styled using the
    [CSS](https://developer.mozilla.org/en-US/docs/Web/CSS) properties
    [`caption-side`](https://developer.mozilla.org/en-US/docs/Web/CSS/caption-side)
    and
    [`text-align`](https://developer.mozilla.org/en-US/docs/Web/CSS/text-align).
    :::
:::

## Usage notes {#usage_notes}

::: section-content
If used, the `<caption>` element must be the first child of its parent
[`<table>`](table) element.

When the `<table>` element that contains the `<caption>` is the only
descendant of a [`<figure>`](figure) element, you should use the
[`<figcaption>`](figcaption) element instead of `<caption>`.

A
[`background-color`](https://developer.mozilla.org/en-US/docs/Web/CSS/background-color)
on the table will not include the caption. Add a `background-color` to
the `<caption>` element as well if you want the same color to be behind
both.
:::

## Example

::: section-content
This simple example presents a table that includes a caption.

::: code-example
[html]{.language-name}

``` {signature="Qj/fk8WT+LS0IFQz7N0dFGfEQTpB9teHn1jyllNTA0c=" data-language="html"}
<table>
  <caption>
    Example Caption
  </caption>
  <tr>
    <th>Login</th>
    <th>Email</th>
  </tr>
  <tr>
    <td>user1</td>
    <td>user1@sample.com</td>
  </tr>
  <tr>
    <td>user2</td>
    <td>user2@sample.com</td>
  </tr>
</table>
```
:::

::: {#sect2 .code-example}
::: iframe
:::
:::
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
<td><a href="../content_categories#flow_content">Flow content</a>.</td>
</tr>
<tr class="odd">
<th scope="row">Tag omission</th>
<td>The end tag can be omitted if the element is not immediately
followed by ASCII whitespace or a comment.</td>
</tr>
<tr class="even">
<th scope="row">Permitted parents</th>
<td>A <a href="table"><code>&lt;table&gt;</code></a> element, as its
first descendant.</td>
</tr>
<tr class="odd">
<th scope="row">Implicit ARIA role</th>
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/structural_roles#structural_roles_with_html_equivalents"><code>caption</code></a></td>
</tr>
<tr class="even">
<th scope="row">Permitted ARIA roles</th>
<td>No <code>role</code> permitted</td>
</tr>
<tr class="odd">
<th scope="row">DOM interface</th>
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLTableCaptionElement"><code>HTMLTableCaptionElement</code></a></td>
</tr>
</tbody>
</table>

</figure>
:::

## Specifications

::: _table
  -------------------------------------------------------------------------------------------------------
  Specification
  -------------------------------------------------------------------------------------------------------
  [HTML Standard\
  [\#
  the-caption-element]{.small}](https://html.spec.whatwg.org/multipage/tables.html#the-caption-element)

  -------------------------------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
              Desktop                                                         Mobile                                                                                   
  ----------- --------- ------ --------- ------------------- ------- -------- ----------------- ---------------- --------------------- --------------- --------------- ------------------
              Chrome    Edge   Firefox   Internet Explorer   Opera   Safari   WebView Android   Chrome Android   Firefox for Android   Opera Android   Safari on IOS   Samsung Internet
  `caption`   1         12     1         Yes                 15      ≤4       4.4               18               4                     14              ≤3.2            1.0
  `align`     1         12     1         Yes                 15      ≤4       4.4               18               4                     14              ≤3.2            1.0
:::

## See also {#see_also}

::: section-content
-   CSS properties that may be specially useful to style the
    [`<caption>`](caption){aria-current="page"} element:
    -   [`text-align`](https://developer.mozilla.org/en-US/docs/Web/CSS/text-align),
        [`caption-side`](https://developer.mozilla.org/en-US/docs/Web/CSS/caption-side).
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Element/caption](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/caption){._attribution-link}
:::
