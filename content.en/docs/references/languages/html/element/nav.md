

# \<nav\>: The Navigation Section element



::: section-content
The `<nav>` [HTML](../index) element represents a section of a page
whose purpose is to provide navigation links, either within the current
document or to other documents. Common examples of navigation sections
are menus, tables of contents, and indexes.
:::

## Try it {#try_it}

::: section-content
::: iframe
::: {.output-header .border-rounded-top}
#### HTML Demo: \<nav\> {#html-demo-nav .output-heading}

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
    <nav class="crumbs">
      <ol>
        <li class="crumb"><a href="#">Bikes</a></li>
        <li class="crumb"><a href="#">BMX</a></li>
        <li class="crumb">Jump Bike 3000</li>
      </ol>
    </nav>

    <h1>Jump Bike 3000</h1>
    <p>
      This BMX bike is a solid step into the pro world. It looks as legit as it rides and is built to polish your skills.
    </p>
:::
:::

::: {#css-panel .section .hidden tabindex="0" role="tabpanel" aria-labelledby="css" aria-hidden="true"}
::: {#css-editor}
    nav {
      border-bottom: 1px solid black;
    }

    .crumbs ol {
      list-style-type: none;
      padding-left: 0;
    }

    .crumb {
      display: inline-block;
    }

    .crumb a::after {
      display: inline-block;
      color: #000;
      content: '>';
      font-size: 80%;
      font-weight: bold;
      padding: 0 3px;
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
<tbody>
<tr class="odd">
<th scope="row"><a href="../content_categories">Content
categories</a></th>
<td><a href="../content_categories#flow_content">Flow content</a>, <a
href="../content_categories#sectioning_content">sectioning content</a>,
palpable content.</td>
</tr>
<tr class="even">
<th scope="row">Permitted content</th>
<td><a href="../content_categories#flow_content">Flow content</a>.</td>
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
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/navigation_role"><code>navigation</code></a></td>
</tr>
<tr class="even">
<th scope="row">Permitted ARIA roles</th>
<td>No <code>role</code> permitted</td>
</tr>
<tr class="odd">
<th scope="row">DOM interface</th>
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement"><code>HTMLElement</code></a></td>
</tr>
</tbody>
</table>

</figure>
:::

## Attributes

::: section-content
This element only includes the [global
attributes](../global_attributes).
:::

## Usage notes {#usage_notes}

::: section-content
-   It\'s not necessary for all links to be contained in a `<nav>`
    element. `<nav>` is intended only for a major block of navigation
    links; typically the [`<footer>`](footer) element often has a list
    of links that don\'t need to be in a
    [`<nav>`](nav){aria-current="page"} element.
-   A document may have several [`<nav>`](nav){aria-current="page"}
    elements, for example, one for site navigation and one for
    intra-page navigation.
    [`aria-labelledby`](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Attributes/aria-labelledby)
    can be used in such case to promote accessibility, see
    [example](heading_elements#labeling_section_content).
-   User agents, such as screen readers targeting disabled users, can
    use this element to determine whether to omit the initial rendering
    of navigation-only content.
:::

## Examples

::: section-content
In this example, a `<nav>` block is used to contain an unordered list
([`<ul>`](ul)) of links. With appropriate CSS, this can be presented as
a sidebar, navigation bar, or drop-down menu.

::: code-example
[html]{.language-name}

``` {signature="lvHiSO1FEwp248bp4D6V4uLSBWnonuH9Q1bJkeF/9DY=" data-language="html"}
<nav class="menu">
  <ul>
    <li><a href="#">Home</a></li>
    <li><a href="#">About</a></li>
    <li><a href="#">Contact</a></li>
  </ul>
</nav>
```
:::

The semantics of the `nav` element is that of providing links. However a
`nav` element doesn\'t have to contain a list, it can contain other
kinds of content as well. In this navigation block, links are provided
in prose:

::: code-example
[html]{.language-name}

``` {signature="NpWeQ3PZnVei0X8e1Ma+f4F87L9r2flLHqsYdUdbvbM=" data-language="html"}
<nav>
  <h2>Navigation</h2>
  <p>
    You are on my home page. To the north lies <a href="/blog">my blog</a>, from
    whence the sounds of battle can be heard. To the east you can see a large
    mountain, upon which many <a href="/school">school papers</a> are littered.
    Far up this mountain you can spy a little figure who appears to be me,
    desperately scribbling a <a href="/school/thesis">thesis</a>.
  </p>
  <p>
    To the west are several exits. One fun-looking exit is labeled
    <a href="https://games.example.com/">"games"</a>. Another more
    boring-looking exit is labeled <a href="https://isp.example.net/">ISP™</a>.
  </p>
  <p>
    To the south lies a dark and dank <a href="/about">contacts page</a>.
    Cobwebs cover its disused entrance, and at one point you see a rat run
    quickly out of the page.
  </p>
</nav>
```
:::
:::

### Result

::: section-content
::: {#sect1 .code-example}
::: iframe
:::
:::
:::

## Specifications

::: _table
  -------------------------------------------------------------------------------------------------
  Specification
  -------------------------------------------------------------------------------------------------
  [HTML Standard\
  [\#
  the-nav-element]{.small}](https://html.spec.whatwg.org/multipage/sections.html#the-nav-element)

  -------------------------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
          Desktop                                                         Mobile                                                                                   
  ------- --------- ------ --------- ------------------- ------- -------- ----------------- ---------------- --------------------- --------------- --------------- ------------------
          Chrome    Edge   Firefox   Internet Explorer   Opera   Safari   WebView Android   Chrome Android   Firefox for Android   Opera Android   Safari on IOS   Samsung Internet
  `nav`   5         12     4         9                   11.1    5        4.4               18               4                     11.1            4.2             1.0
:::

## See also {#see_also}

::: section-content
-   Other section-related elements: [`<body>`](body),
    [`<article>`](article), [`<section>`](section), [`<aside>`](aside),
    [h1](heading_elements), [h2](heading_elements),
    [h3](heading_elements), [h4](heading_elements),
    [h5](heading_elements), [h6](heading_elements),
    [`<hgroup>`](hgroup), [`<header>`](header), [`<footer>`](footer),
    [`<address>`](address);
-   [Sections and outlines of an HTML document](heading_elements).
-   [ARIA: Navigation
    role](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/navigation_role)
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Element/nav](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/nav){._attribution-link}
:::
