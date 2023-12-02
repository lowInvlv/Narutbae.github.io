

# \<section\>: The Generic Section element



::: section-content
The `<section>` [HTML](../index) element represents a generic standalone
section of a document, which doesn\'t have a more specific semantic
element to represent it. Sections should always have a heading, with
very few exceptions.
:::

## Try it {#try_it}

::: section-content
::: iframe
::: {.output-header .border-rounded-top}
#### HTML Demo: \<section\> {#html-demo-section .output-heading}

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
    <h1>Choosing an Apple</h1>
    <section>
      <h2>Introduction</h2>
      <p>This document provides a guide to help with the important task of choosing the correct Apple.</p>
    </section>

    <section>
      <h2>Criteria</h2>
      <p>
        There are many different criteria to be considered when choosing an Apple — size, color, firmness, sweetness,
        tartness...
      </p>
    </section>
:::
:::

::: {#css-panel .section .hidden tabindex="0" role="tabpanel" aria-labelledby="css" aria-hidden="true"}
::: {#css-editor}
    h1,
    h2 {
      margin: 0;
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
As mentioned above, `<section>` is a generic sectioning element, and
should only be used if there isn\'t a more specific element to represent
it. As an example, a navigation menu should be wrapped in a
[`<nav>`](nav) element, but a list of search results or a map display
and its controls don\'t have specific elements, and could be put inside
a `<section>`.

Also consider these cases:

-   If the contents of the element represent a standalone, atomic unit
    of content that makes sense syndicated as a standalone piece (e.g. a
    blog post or blog comment, or a newspaper article), the
    [`<article>`](article) element would be a better choice.
-   If the contents represent useful tangential information that works
    alongside the main content, but is not directly part of it (like
    related links, or an author bio), use an [`<aside>`](aside).
-   If the contents represent the main content area of a document, use
    [`<main>`](main).
-   If you are only using the element as a styling wrapper, use a
    [``](div) instead.

To reiterate, each `<section>` should be identified, typically by
including a heading ([h1](heading_elements) - [h6](heading_elements)
element) as a child of the `<section>` element, wherever possible. See
below for examples of where you might see a `<section>` without a
heading.
:::

## Examples

### Simple usage example {#simple_usage_example}

::: section-content
#### Before

::: code-example
[html]{.language-name}

``` {signature="J6KDvFLfQm8eED/CYG4hVDTBWEHgiZiGkHkWU4hbJ8g=" data-language="html"}

  <h2>Heading</h2>
  <p>Bunch of awesome content</p>

```
:::

##### Result

::: {#sect1 .code-example}
::: iframe
:::
:::

#### After

::: code-example
[html]{.language-name}

``` {signature="5b7leNz2AZvXzRIrnfZ11PsNHxxo4Vd3GBLTzD3JgLw=" data-language="html"}
<section>
  <h2>Heading</h2>
  <p>Bunch of awesome content</p>
</section>
```
:::

##### Result {#result_2}

::: {#sect2 .code-example}
::: iframe
:::
:::
:::

### Using a section without a heading {#using_a_section_without_a_heading}

::: section-content
Circumstances where you might see `<section>` used without a heading are
typically found in web application/UI sections rather than in
traditional document structures. In a document, it doesn\'t really make
any sense to have a separate section of content without a heading to
describe its contents. Such headings are useful for all readers, but
particularly useful for users of assistive technologies like screen
readers, and they are also good for SEO.

Consider however a secondary navigation mechanism. If the global
navigation is already wrapped in a `<nav>` element, you could
conceivably wrap a previous/next menu in a `<section>`:

::: code-example
[html]{.language-name}

``` {signature="RaHu3O0bE347gVJz13HmDceSS7OzEYB1A8UfKmik9Ko=" data-language="html"}
<section>
  <a href="#">Previous article</a>
  <a href="#">Next article</a>
</section>
```
:::

Or what about some kind of button bar for controlling your app? This
might not necessarily want a heading, but it is still a distinct section
of the document:

::: code-example
[html]{.language-name}

``` {signature="gryYVEKrpXlsruYIxEPL5CFfWM2gKpqgOWLWiUK1Dt4=" data-language="html"}
<section>
  <button class="reply">Reply</button>
  <button class="reply-all">Reply to all</button>
  <button class="fwd">Forward</button>
  <button class="del">Delete</button>
</section>
```
:::

#### Result {#result_3}

::: {#sect3 .code-example}
::: iframe
:::
:::

Depending on the content, including a heading could also be good for
SEO, so it is an option to consider.
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
<td><a href="../content_categories#flow_content">Flow content</a>, <a
href="../content_categories#sectioning_content">Sectioning content</a>,
<a href="../content_categories#palpable_content">palpable
content</a>.</td>
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
href="../content_categories#flow_content">flow content</a>. Note that a
<code>&lt;section&gt;</code> element must not be a descendant of an <a
href="address"><code>&lt;address&gt;</code></a> element.</td>
</tr>
<tr class="odd">
<th scope="row">Implicit ARIA role</th>
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/region_role"><code>region</code></a>
if the element has an <a
href="https://developer.paciellogroup.com/blog/2017/04/what-is-an-accessible-name/"
target="_blank">accessible name</a>, otherwise <a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/generic_role"><code>generic</code></a></td>
</tr>
<tr class="even">
<th scope="row">Permitted ARIA roles</th>
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/alert_role"><code>alert</code></a>,
<a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/alertdialog_role"><code>alertdialog</code></a>,
<a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/application_role"><code>application</code></a>,
<a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/banner_role"><code>banner</code></a>,
<a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/complementary_role"><code>complementary</code></a>,
<a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/contentinfo_role"><code>contentinfo</code></a>,
<a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/dialog_role"><code>dialog</code></a>,
<a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/document_role"><code>document</code></a>,
<a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/feed_role"><code>feed</code></a>,
<a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/log_role"><code>log</code></a>,
<a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/main_role"><code>main</code></a>,
<a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/marquee_role"><code>marquee</code></a>,
<a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/navigation_role"><code>navigation</code></a>,
<a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/none_role"><code>none</code></a>,
<a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/note_role"><code>note</code></a>,
<a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/presentation_role"><code>presentation</code></a>,
<a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/search_role"><code>search</code></a>,
<a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/status_role"><code>status</code></a>,
<a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/tabpanel_role"><code>tabpanel</code></a></td>
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

## Specifications

::: _table
  ---------------------------------------------------------------------------------------------------------
  Specification
  ---------------------------------------------------------------------------------------------------------
  [HTML Standard\
  [\#
  the-section-element]{.small}](https://html.spec.whatwg.org/multipage/sections.html#the-section-element)

  ---------------------------------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
              Desktop                                                         Mobile                                                                                   
  ----------- --------- ------ --------- ------------------- ------- -------- ----------------- ---------------- --------------------- --------------- --------------- ------------------
              Chrome    Edge   Firefox   Internet Explorer   Opera   Safari   WebView Android   Chrome Android   Firefox for Android   Opera Android   Safari on IOS   Samsung Internet
  `section`   5         12     4         9                   11.1    5        4.4               18               4                     11.1            4.2             1.0
:::

## See also {#see_also}

::: section-content
-   Other section-related elements: [`<body>`](body), [`<nav>`](nav),
    [`<article>`](article), [`<aside>`](aside), [h1](heading_elements),
    [h2](heading_elements), [h3](heading_elements),
    [h4](heading_elements), [h5](heading_elements),
    [h6](heading_elements), [`<hgroup>`](hgroup), [`<header>`](header),
    [`<footer>`](footer), [`<address>`](address)
-   [Using HTML sections and outlines](heading_elements)
-   [ARIA: Region
    role](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/region_role)
-   [Why You Should Choose HTML5 article Over
    section](https://www.smashingmagazine.com/2020/01/html5-article-section/){target="_blank"},
    by Bruce Lawson
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Element/section](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/section){._attribution-link}
:::
