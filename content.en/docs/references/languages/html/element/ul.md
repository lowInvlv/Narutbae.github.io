

# \<ul\>: The Unordered List element



::: section-content
The `<ul>` [HTML](../index) element represents an unordered list of
items, typically rendered as a bulleted list.
:::

## Try it {#try_it}

::: section-content
::: iframe
::: {.output-header .border-rounded-top}
#### HTML Demo: \<ul\> {#html-demo-ul .output-heading}

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
    <ul>
      <li>Milk</li>
      <li>
        Cheese
        <ul>
          <li>Blue cheese</li>
          <li>Feta</li>
        </ul>
      </li>
    </ul>
:::
:::

::: {#css-panel .section .hidden tabindex="0" role="tabpanel" aria-labelledby="css" aria-hidden="true"}
::: {#css-editor}
    li {
      list-style-type: circle;
    }

    li li {
      list-style-type: square;
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

[`compact`](#compact) [Deprecated]{.visually-hidden} [Non-standard]{.visually-hidden}

:   This Boolean attribute hints that the list should be rendered in a
    compact style. The interpretation of this attribute depends on the
    [user
    agent](https://developer.mozilla.org/en-US/docs/Glossary/User_agent),
    and it doesn\'t work in all browsers.

    ::: {#sect1 .notecard .warning}
    **Warning:** Do not use this attribute, as it has been deprecated:
    use [CSS](https://developer.mozilla.org/en-US/docs/Web/CSS) instead.
    To give a similar effect as the `compact` attribute, the CSS
    property
    [`line-height`](https://developer.mozilla.org/en-US/docs/Web/CSS/line-height)
    can be used with a value of `80%`.
    :::

[`type`](#type) [Deprecated]{.visually-hidden} [Non-standard]{.visually-hidden}

:   This attribute sets the bullet style for the list. The values
    defined under HTML3.2 and the transitional version of HTML 4.0/4.01
    are:

    -   `circle`
    -   `disc`
    -   `square`

    A fourth bullet type has been defined in the WebTV interface, but
    not all browsers support it: `triangle`.

    If not present and if no
    [CSS](https://developer.mozilla.org/en-US/docs/Web/CSS)
    [`list-style-type`](https://developer.mozilla.org/en-US/docs/Web/CSS/list-style-type)
    property applies to the element, the user agent selects a bullet
    type depending on the nesting level of the list.

    ::: {#sect2 .notecard .warning}
    **Warning:** Do not use this attribute, as it has been deprecated;
    use the [CSS](https://developer.mozilla.org/en-US/docs/Web/CSS)
    [`list-style-type`](https://developer.mozilla.org/en-US/docs/Web/CSS/list-style-type)
    property instead.
    :::
:::

## Usage notes {#usage_notes}

::: section-content
-   The `<ul>` element is for grouping a collection of items that do not
    have a numerical ordering, and their order in the list is
    meaningless. Typically, unordered-list items are displayed with a
    bullet, which can be of several forms, like a dot, a circle, or a
    square. The bullet style is not defined in the HTML description of
    the page, but in its associated CSS, using the
    [`list-style-type`](https://developer.mozilla.org/en-US/docs/Web/CSS/list-style-type)
    property.
-   The `<ul>` and [`<ol>`](ol) elements may be nested as deeply as
    desired. Moreover, the nested lists may alternate between `<ol>` and
    `<ul>` without restriction.
-   The [`<ol>`](ol) and `<ul>` elements both represent a list of items.
    They differ in that, with the [`<ol>`](ol) element, the order is
    meaningful. To determine which one to use, try changing the order of
    the list items; if the meaning is changed, the [`<ol>`](ol) element
    should be used, otherwise you can use `<ul>`.
:::

## Examples

### Simple example {#simple_example}

::: section-content
::: code-example
[html]{.language-name}

``` {signature="n7kxjao4feyxWliQCMdrMcy8RxCttlQhOI9lg8Od7fc=" data-language="html"}
<ul>
  <li>first item</li>
  <li>second item</li>
  <li>third item</li>
</ul>
```
:::

#### Result

::: {#sect3 .code-example}
::: iframe
:::
:::
:::

### Nesting a list {#nesting_a_list}

::: section-content
::: code-example
[html]{.language-name}

``` {signature="Ef2xrtueYGdwFrkYsNih7qpMDxieHEhLc8zNyPC6pKU=" data-language="html"}
<ul>
  <li>first item</li>
  <li>
    second item
    <!-- Look, the closing </li> tag is not placed here! -->
    <ul>
      <li>second item first subitem</li>
      <li>
        second item second subitem
        <!-- Same for the second nested unordered list! -->
        <ul>
          <li>second item second subitem first sub-subitem</li>
          <li>second item second subitem second sub-subitem</li>
          <li>second item second subitem third sub-subitem</li>
        </ul>
      </li>
      <!-- Closing </li> tag for the li that
                  contains the third unordered list -->
      <li>second item third subitem</li>
    </ul>
    <!-- Here is the closing </li> tag -->
  </li>
  <li>third item</li>
</ul>
```
:::

#### Result {#result_2}

::: {#sect4 .code-example}
::: iframe
:::
:::
:::

### Ordered list inside unordered list {#ordered_list_inside_unordered_list}

::: section-content
::: code-example
[html]{.language-name}

``` {signature="y5o6lzTwRMBraQs976S7Wkpb7WHu4FJ2B/4onFdPcc4=" data-language="html"}
<ul>
  <li>first item</li>
  <li>
    second item
    <!-- Look, the closing </li> tag is not placed here! -->
    <ol>
      <li>second item first subitem</li>
      <li>second item second subitem</li>
      <li>second item third subitem</li>
    </ol>
    <!-- Here is the closing </li> tag -->
  </li>
  <li>third item</li>
</ul>
```
:::

#### Result {#result_3}

::: {#sect5 .code-example}
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
<td><a href="../content_categories#flow_content">Flow content</a>, and
if the <code>&lt;ul&gt;</code> element's children include at least one
<a href="li"><code>&lt;li&gt;</code></a> element, <a
href="../content_categories#palpable_content">palpable content</a>.</td>
</tr>
<tr class="even">
<th scope="row">Permitted content</th>
<td>Zero or more <a href="li"><code>&lt;li&gt;</code></a>, <a
href="script"><code>&lt;script&gt;</code></a> and <a
href="template"><code>&lt;template&gt;</code></a> elements.</td>
</tr>
<tr class="odd">
<th scope="row">Tag omission</th>
<td>None, both the starting and ending tag are mandatory.</td>
</tr>
<tr class="even">
<th scope="row">Permitted parents</th>
<td>Any element that accepts <a
href="../content_categories#flow_content">flow content</a>.</td>
</tr>
<tr class="odd">
<th scope="row">Implicit ARIA role</th>
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/list_role"><code>list</code></a></td>
</tr>
<tr class="even">
<th scope="row">Permitted ARIA roles</th>
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/directory_role"><code>directory</code></a>,
<a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/group_role"><code>group</code></a>,
<a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/listbox_role"><code>listbox</code></a>,
<a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/menu_role"><code>menu</code></a>,
<a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/menubar_role"><code>menubar</code></a>,
<a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/none_role"><code>none</code></a>,
<a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/presentation_role"><code>presentation</code></a>,
<a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/radiogroup_role"><code>radiogroup</code></a>,
<a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/tablist_role"><code>tablist</code></a>,
<a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/toolbar_role"><code>toolbar</code></a>,
<a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/tree_role"><code>tree</code></a></td>
</tr>
<tr class="odd">
<th scope="row">DOM Interface</th>
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLUListElement"><code>HTMLUListElement</code></a></td>
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
  the-ul-element]{.small}](https://html.spec.whatwg.org/multipage/grouping-content.html#the-ul-element)

  -------------------------------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
              Desktop                                                         Mobile                                                                                   
  ----------- --------- ------ --------- ------------------- ------- -------- ----------------- ---------------- --------------------- --------------- --------------- ------------------
              Chrome    Edge   Firefox   Internet Explorer   Opera   Safari   WebView Android   Chrome Android   Firefox for Android   Opera Android   Safari on IOS   Samsung Internet
  `ul`        1         12     1         Yes                 15      ≤4       4.4               18               4                     14              ≤3.2            1.0
  `compact`   1         12     1         Yes                 15      3        4.4               18               4                     14              2               1.0
  `type`      1         12     1         Yes                 15      ≤4       4.4               18               4                     14              ≤3.2            1.0
:::

## See also {#see_also}

::: section-content
-   Other list-related HTML Elements: [`<ol>`](ol), [`<li>`](li),
    [`<menu>`](menu)
-   CSS properties that may be specially useful to style the `<ul>`
    element:
    -   the
        [`list-style`](https://developer.mozilla.org/en-US/docs/Web/CSS/list-style)
        property, to choose the way the ordinal displays.
    -   [CSS
        counters](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_counter_styles/Using_CSS_counters),
        to handle complex nested lists.
    -   the
        [`line-height`](https://developer.mozilla.org/en-US/docs/Web/CSS/line-height)
        property, to simulate the deprecated [`compact`](#compact)
        attribute.
    -   the
        [`margin`](https://developer.mozilla.org/en-US/docs/Web/CSS/margin)
        property, to control the list indentation.
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Element/ul](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/ul){._attribution-link}
:::
