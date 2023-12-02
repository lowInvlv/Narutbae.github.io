

# \<li\>: The List Item element



::: section-content
The `<li>` [HTML](../index) element is used to represent an item in a
list. It must be contained in a parent element: an ordered list
([`<ol>`](ol)), an unordered list ([`<ul>`](ul)), or a menu
([`<menu>`](menu)). In menus and unordered lists, list items are usually
displayed using bullet points. In ordered lists, they are usually
displayed with an ascending counter on the left, such as a number or
letter.
:::

## Try it {#try_it}

::: section-content
::: iframe
::: {.output-header .border-rounded-top}
#### HTML Demo: \<li\> {#html-demo-li .output-heading}

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
    <p>Apollo astronauts:</p>

    <ul>
      <li>Neil Armstrong</li>
      <li>Alan Bean</li>
      <li>Peter Conrad</li>
      <li>Edgar Mitchell</li>
      <li>Alan Shepard</li>
    </ul>
:::
:::

::: {#css-panel .section .hidden tabindex="0" role="tabpanel" aria-labelledby="css" aria-hidden="true"}
::: {#css-editor}
    p,
    li {
      font:
        1rem 'Fira Sans',
        sans-serif;
    }

    p {
      font-weight: bold;
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

[`value`](#value)

:   This integer attribute indicates the current ordinal value of the
    list item as defined by the [`<ol>`](ol) element. The only allowed
    value for this attribute is a number, even if the list is displayed
    with Roman numerals or letters. List items that follow this one
    continue numbering from the value set. The **value** attribute has
    no meaning for unordered lists ([`<ul>`](ul)) or for menus
    ([`<menu>`](menu)).

[`type`](#type) [Deprecated]{.visually-hidden} [Non-standard]{.visually-hidden}

:   This character attribute indicates the numbering type:

    -   `a`: lowercase letters
    -   `A`: uppercase letters
    -   `i`: lowercase Roman numerals
    -   `I`: uppercase Roman numerals
    -   `1`: numbers

    This type overrides the one used by its parent [`<ol>`](ol) element,
    if any.

    ::: {#sect1 .notecard .note}
    **Note:** This attribute has been deprecated; use the CSS
    [`list-style-type`](https://developer.mozilla.org/en-US/docs/Web/CSS/list-style-type)
    property instead.
    :::
:::

## Examples

::: section-content
For more detailed examples, see the [`<ol>`](ol) and [`<ul>`](ul) pages.
:::

### Ordered list {#ordered_list}

::: section-content
::: code-example
[html]{.language-name}

``` {signature="d0aCtyTysW90QKmJ9Zpbsy1/9oiB+KCpFVk+NE2nBRk=" data-language="html"}
<ol>
  <li>first item</li>
  <li>second item</li>
  <li>third item</li>
</ol>
```
:::

#### Result

::: {#sect2 .code-example}
::: iframe
:::
:::
:::

### Ordered list with a custom value {#ordered_list_with_a_custom_value}

::: section-content
::: code-example
[html]{.language-name}

``` {signature="CS/ra7gVs/R/4xtSHYAsPjcKq4VKzpGaKpFX/ctvCuk=" data-language="html"}
<ol type="I">
  <li value="3">third item</li>
  <li>fourth item</li>
  <li>fifth item</li>
</ol>
```
:::

#### Result {#result_2}

::: {#sect3 .code-example}
::: iframe
:::
:::
:::

### Unordered list {#unordered_list}

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

#### Result {#result_3}

::: {#sect4 .code-example}
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
<td>The end tag can be omitted if the list item is immediately followed
by another <a href="li" aria-current="page"><code>&lt;li&gt;</code></a>
element, or if there is no more content in its parent element.</td>
</tr>
<tr class="even">
<th scope="row">Permitted parents</th>
<td>An <a href="ul"><code>&lt;ul&gt;</code></a>, <a
href="ol"><code>&lt;ol&gt;</code></a>, or <a
href="menu"><code>&lt;menu&gt;</code></a> element. Though not a
conforming usage, the obsolete <a
href="dir"><code>&lt;dir&gt;</code></a> can also be a parent.</td>
</tr>
<tr class="odd">
<th scope="row">Implicit ARIA role</th>
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/listitem_role"><code>listitem</code></a>
when child of an <a href="ol"><code>ol</code></a>, <a
href="ul"><code>ul</code></a> or <a
href="menu"><code>menu</code></a></td>
</tr>
<tr class="even">
<th scope="row">Permitted ARIA roles</th>
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/menuitem_role"><code>menuitem</code></a>,
<a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/menuitemcheckbox_role"><code>menuitemcheckbox</code></a>,
<a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/menuitemradio_role"><code>menuitemradio</code></a>,
<a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/option_role"><code>option</code></a>,
<a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/none_role"><code>none</code></a>,
<a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/presentation_role"><code>presentation</code></a>,
<a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/radio_role"><code>radio</code></a>,
<a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/separator_role"><code>separator</code></a>,
<a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/tab_role"><code>tab</code></a>,
<a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/treeitem_role"><code>treeitem</code></a></td>
</tr>
<tr class="odd">
<th scope="row">DOM interface</th>
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLLIElement"><code>HTMLLIElement</code></a></td>
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
  the-li-element]{.small}](https://html.spec.whatwg.org/multipage/grouping-content.html#the-li-element)

  -------------------------------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
            Desktop                                                         Mobile                                                                                   
  --------- --------- ------ --------- ------------------- ------- -------- ----------------- ---------------- --------------------- --------------- --------------- ------------------
            Chrome    Edge   Firefox   Internet Explorer   Opera   Safari   WebView Android   Chrome Android   Firefox for Android   Opera Android   Safari on IOS   Samsung Internet
  `li`      1         12     1         5.5                 ≤12.1   3        4.4               18               4                     ≤12.1           1               1.0
  `type`    1         12     1         ≤6                  ≤12.1   ≤4       4.4               18               4                     ≤12.1           ≤3.2            1.0
  `value`   1         12     1         ≤6                  ≤12.1   ≤4       4.4               18               4                     ≤12.1           ≤3.2            1.0
:::

## See also {#see_also}

::: section-content
-   Other list-related HTML Elements: [`<ul>`](ul), [`<ol>`](ol),
    [`<menu>`](menu), and the obsolete [`<dir>`](dir);
-   CSS properties that may be specially useful to style the `<li>`
    element:
    -   the
        [`list-style`](https://developer.mozilla.org/en-US/docs/Web/CSS/list-style)
        property, to choose the way the ordinal is displayed,
    -   [CSS
        counters](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_counter_styles/Using_CSS_counters),
        to handle complex nested lists,
    -   the
        [`margin`](https://developer.mozilla.org/en-US/docs/Web/CSS/margin)
        property, to control the indent of the list item.
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Element/li](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/li){._attribution-link}
:::
