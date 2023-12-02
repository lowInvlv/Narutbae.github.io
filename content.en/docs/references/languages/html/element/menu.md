

# \<menu\>: The Menu element



::: section-content
The `<menu>` [HTML](../index) element is described in the HTML
specification as a semantic alternative to [`<ul>`](ul), but treated by
browsers (and exposed through the accessibility tree) as no different
than [`<ul>`](ul). It represents an unordered list of items (which are
represented by [`<li>`](li) elements).
:::

## Try it {#try_it}

::: section-content
::: iframe
::: {.output-header .border-rounded-top}
#### HTML Demo: \<menu\> {#html-demo-menu .output-heading}

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
    <div class="news">
      <a href="#">NASA’s Webb Delivers Deepest Infrared Image of Universe Yet</a>
      <menu>
        <li><button id="save">Save for later</button></li>
        <li><button id="share">Share this news</button></li>
      </menu>
    
:::
:::

::: {#css-panel .section .hidden tabindex="0" role="tabpanel" aria-labelledby="css" aria-hidden="true"}
::: {#css-editor}
    .news {
      background-color: bisque;
      padding: 1em;
      border: solid thin black;
    }

    menu {
      list-style-type: none;
      display: flex;
      padding: 0;
      margin-bottom: 0;
      gap: 1em;
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
This element only includes the [global
attributes](../global_attributes).
:::

## Usage notes {#usage_notes}

::: section-content
The `<menu>` and [`<ul>`](ul) elements both represent an unordered list
of items. The key difference is that [`<ul>`](ul) primarily contains
items for display, while `<menu>` was intended for interactive items.
The related [`<menuitem>`](menuitem) element has been deprecated.

::: {#sect1 .notecard .note}
**Note:** In early versions of the HTML specification, the `<menu>`
element had an additional use case as a context menu. This functionality
is considered obsolete and is not in the specification.
:::
:::

## Examples

### Toolbar

::: section-content
In this example, a `<menu>` is used to create a toolbar for an editing
application.

#### HTML

::: code-example
[html]{.language-name}

``` {signature="+ibiomxSB7T/tf4A98FczqPgSB1Vvo88rvgVic1oS8A=" data-language="html"}
<menu>
  <li><button onclick="copy()">Copy</button></li>
  <li><button onclick="cut()">Cut</button></li>
  <li><button onclick="paste()">Paste</button></li>
</menu>
```
:::

Note that this is functionally no different from:

::: code-example
[html]{.language-name}

``` {signature="sBEXR0ox55FC+5I8tcsv1LBFg1cqgJm/ZptNuF7UzOA=" data-language="html"}
<ul>
  <li><button onclick="copy()">Copy</button></li>
  <li><button onclick="cut()">Cut</button></li>
  <li><button onclick="paste()">Paste</button></li>
</ul>
```
:::

#### CSS

::: code-example
[css]{.language-name}

``` {signature="Ds3T2i/t1IFJChaVhw974MklLz721KI8GZ3piLe9Inw=" data-language="css"}
menu,
ul {
  display: flex;
  list-style: none;
  padding: 0;
  width: 400px;
}

li {
  flex-grow: 1;
}

button {
  width: 100%;
}
```
:::

#### Result

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
<td><p><a href="../content_categories#flow_content">Flow content</a>. If
the element's children include at least one <a
href="li"><code>&lt;li&gt;</code></a> element: <a
href="../content_categories#palpable_content">Palpable
content</a>.</p></td>
</tr>
<tr class="even">
<th scope="row">Permitted content</th>
<td><p>Zero or more occurrences of <a
href="li"><code>&lt;li&gt;</code></a>, <a
href="script"><code>&lt;script&gt;</code></a>, and <a
href="template"><code>&lt;template&gt;</code></a>.</p></td>
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
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/toolbar_role"><code>toolbar</code></a>
or <a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/tree_role"><code>tree</code></a></td>
</tr>
<tr class="odd">
<th scope="row">DOM interface</th>
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLMenuElement"><code>HTMLMenuElement</code></a></td>
</tr>
</tbody>
</table>

</figure>
:::

## Specifications

::: _table
  -----------------------------------------------------------------------------------------------------------
  Specification
  -----------------------------------------------------------------------------------------------------------
  [HTML Standard\
  [\#
  the-menu-element]{.small}](https://html.spec.whatwg.org/multipage/grouping-content.html#the-menu-element)

  -----------------------------------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
  -----------------------------------------------------------------------------------------------------------------------------------------
                   Desktop                                                   Mobile                                              
  ---------------- --------- --------- --------- ---------- ------- -------- --------- --------- ------------ --------- -------- ----------
                   Chrome    Edge      Firefox   Internet   Opera   Safari   WebView   Chrome    Firefox for  Opera     Safari   Samsung
                                                 Explorer                    Android   Android   Android      Android   on IOS   Internet

  `menu`           1         12        1         6          ≤12.1   3        4.4       18        4            ≤12.1     1        1.0

  `hr_separator`   No        No        51--85    No         No      No       No        No        51--85       No        No       No

  `label`          No        No        8--85     No         No      No       No        No        8--85        No        No       No
                                                                                                                                 
                                                                                                 Nested menus                    
                                                                                                 are not                         
                                                                                                 supported.                      

  `type_menu`      No        ≤18--79   8--85     No         No      No       No        No        8--85        No        No       No
                                                                                                                                 
                                                                                                 Nested menus                    
                                                                                                 are not                         
                                                                                                 supported.                      
  -----------------------------------------------------------------------------------------------------------------------------------------
:::

## See also {#see_also}

::: section-content
-   Other list-related HTML Elements: [`<ol>`](ol), [`<ul>`](ul), and
    [`<li>`](li).
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Element/menu](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/menu){._attribution-link}
:::
