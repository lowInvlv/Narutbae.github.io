

# \<ol\>: The Ordered List element



::: section-content
The `<ol>` [HTML](../index) element represents an ordered list of items
--- typically rendered as a numbered list.
:::

## Try it {#try_it}

::: section-content
::: iframe
::: {.output-header .border-rounded-top}
#### HTML Demo: \<ol\> {#html-demo-ol .output-heading}

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

::: {#editor-container .editor-container .tabbed-shorter .hidden .border-rounded-bottom editor-type="tabbed"}
::: {#tab-container .section .tabs}
::: {#tablist .tab-list role="tablist"}
HTML

CSS

JavaScript
:::

::: {#html-panel .section .hidden tabindex="0" role="tabpanel" aria-labelledby="html" aria-hidden="true"}
::: {#html-editor}
    <ol>
      <li>Mix flour, baking powder, sugar, and salt.</li>
      <li>In another bowl, mix eggs, milk, and oil.</li>
      <li>Stir both mixtures together.</li>
      <li>Fill muffin tray 3/4 full.</li>
      <li>Bake for 20 minutes.</li>
    </ol>
:::
:::

::: {#css-panel .section .hidden tabindex="0" role="tabpanel" aria-labelledby="css" aria-hidden="true"}
::: {#css-editor}
    li {
      font:
        1rem 'Fira Sans',
        sans-serif;
      margin-bottom: 0.5rem;
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
This element also accepts the [global attributes](../global_attributes).

[`reversed`](#reversed)

:   This Boolean attribute specifies that the list\'s items are in
    reverse order. Items will be numbered from high to low.

[`start`](#start)

:   An integer to start counting from for the list items. Always an
    Arabic numeral (1, 2, 3, etc.), even when the numbering `type` is
    letters or Roman numerals. For example, to start numbering elements
    from the letter \"d\" or the Roman numeral \"iv,\" use `start="4"`.

[`type`](#type)

:   Sets the numbering type:

    -   `a` for lowercase letters
    -   `A` for uppercase letters
    -   `i` for lowercase Roman numerals
    -   `I` for uppercase Roman numerals
    -   `1` for numbers (default)

    The specified type is used for the entire list unless a different
    [`type`](li#type) attribute is used on an enclosed [`<li>`](li)
    element.

    ::: {#sect1 .notecard .note}
    **Note:** Unless the type of the list number matters (like legal or
    technical documents where items are referenced by their
    number/letter), use the CSS
    [`list-style-type`](https://developer.mozilla.org/en-US/docs/Web/CSS/list-style-type)
    property instead.
    :::
:::

## Usage notes {#usage_notes}

::: section-content
Typically, ordered list items display with a preceding
[marker](https://developer.mozilla.org/en-US/docs/Web/CSS/::marker),
such as a number or letter.

The `<ol>` and [`<ul>`](ul) elements may nest as deeply as desired,
alternating between `<ol>` and `<ul>` however you like.

The `<ol>` and [`<ul>`](ul) elements both represent a list of items. The
difference is with the `<ol>` element, the order is meaningful. For
example:

-   Steps in a recipe
-   Turn-by-turn directions
-   The list of ingredients in decreasing proportion on nutrition
    information labels

To determine which list to use, try changing the order of the list
items; if the meaning changes, use the `<ol>` element --- otherwise you
can use [`<ul>`](ul).
:::

## Examples

### Simple example {#simple_example}

::: section-content
::: code-example
[html]{.language-name}

``` {signature="6kDgrEEvDkFQLRMGZhbFCFDPrbV7kZiK7yqGYt2hJko=" data-language="html"}
<ol>
  <li>Fee</li>
  <li>Fi</li>
  <li>Fo</li>
  <li>Fum</li>
</ol>
```
:::

#### Result

::: {#sect2 .code-example}
::: iframe
:::
:::
:::

### Using Roman Numeral type {#using_roman_numeral_type}

::: section-content
::: code-example
[html]{.language-name}

``` {signature="AQjfsseOztiYWvZ1s79naUgXU0qUgonoYoblPUUFI5E=" data-language="html"}
<ol type="i">
  <li>Introduction</li>
  <li>List of Grievances</li>
  <li>Conclusion</li>
</ol>
```
:::

#### Result {#result_2}

::: {#sect3 .code-example}
::: iframe
:::
:::
:::

### Using the start attribute {#using_the_start_attribute}

::: section-content
::: code-example
[html]{.language-name}

``` {signature="UsEhPVqfYPTlAgsMJpnCD6aif1rvpYG4XT3s5Dlyzlc=" data-language="html"}
<p>Finishing places of contestants not in the winners' circle:</p>

<ol start="4">
  <li>Speedwalk Stu</li>
  <li>Saunterin' Sam</li>
  <li>Slowpoke Rodriguez</li>
</ol>
```
:::

#### Result {#result_3}

::: {#sect4 .code-example}
::: iframe
:::
:::
:::

### Nesting lists {#nesting_lists}

::: section-content
::: code-example
[html]{.language-name}

``` {signature="SlmbcOxxr64zPSGcfrgmN8hBcyl0zAyqPMTZLwVzhZo=" data-language="html"}
<ol>
  <li>first item</li>
  <li>
    second item
    <!-- closing </li> tag is not here! -->
    <ol>
      <li>second item first subitem</li>
      <li>second item second subitem</li>
      <li>second item third subitem</li>
    </ol>
  </li>
  <!-- Here's the closing </li> tag -->
  <li>third item</li>
</ol>
```
:::

#### Result {#result_4}

::: {#sect5 .code-example}
::: iframe
:::
:::
:::

### Unordered list inside ordered list {#unordered_list_inside_ordered_list}

::: section-content
::: code-example
[html]{.language-name}

``` {signature="Y1nCSf2gP77BPcXkYpgSlCYzUxibFPwUK+STDipqoxQ=" data-language="html"}
<ol>
  <li>first item</li>
  <li>
    second item
    <!-- closing </li> tag is not here! -->
    <ul>
      <li>second item first subitem</li>
      <li>second item second subitem</li>
      <li>second item third subitem</li>
    </ul>
  </li>
  <!-- Here's the closing </li> tag -->
  <li>third item</li>
</ol>
```
:::

#### Result {#result_5}

::: {#sect6 .code-example}
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
if the <code>&lt;ol&gt;</code> element's children include at least one
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
<th scope="row">DOM interface</th>
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLOListElement"><code>HTMLOListElement</code></a></td>
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
  the-ol-element]{.small}](https://html.spec.whatwg.org/multipage/grouping-content.html#the-ol-element)

  -------------------------------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
               Desktop                                                         Mobile                                                                                   
  ------------ --------- ------ --------- ------------------- ------- -------- ----------------- ---------------- --------------------- --------------- --------------- ------------------
               Chrome    Edge   Firefox   Internet Explorer   Opera   Safari   WebView Android   Chrome Android   Firefox for Android   Opera Android   Safari on IOS   Samsung Internet
  `ol`         1         12     1         Yes                 15      ≤4       4.4               18               4                     14              ≤3.2            1.0
  `compact`    1         12     1         Yes                 15      3        4.4               18               4                     14              2               1.0
  `reversed`   18        ≤79    18        No                  15      6        4.4               18               18                    14              6               1.0
  `start`      1         12     1         Yes                 15      ≤4       4.4               18               4                     14              ≤3.2            1.0
  `type`       1         12     1         Yes                 15      ≤4       4.4               18               4                     14              ≤3.2            1.0
:::

## See also {#see_also}

::: section-content
-   Other list-related HTML Elements: [`<ul>`](ul), [`<li>`](li),
    [`<menu>`](menu)
-   CSS properties that may be specially useful to style the `<ol>`
    element:
    -   the
        [`list-style`](https://developer.mozilla.org/en-US/docs/Web/CSS/list-style)
        property, to choose the way the ordinal displays
    -   [CSS
        counters](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_counter_styles/Using_CSS_counters),
        to handle complex nested lists
    -   the
        [`line-height`](https://developer.mozilla.org/en-US/docs/Web/CSS/line-height)
        property, to simulate the deprecated [`compact`](#compact)
        attribute
    -   the
        [`margin`](https://developer.mozilla.org/en-US/docs/Web/CSS/margin)
        property, to control the list indentation
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Element/ol](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/ol){._attribution-link}
:::
