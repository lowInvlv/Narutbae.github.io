

# \<h1\>--\<h6\>: The HTML Section Heading elements



::: section-content
The `<h1>` to `<h6>` [HTML](../index) elements represent six levels of
section headings. `<h1>` is the highest section level and `<h6>` is the
lowest. By default, all heading elements create a
[block-level](https://developer.mozilla.org/en-US/docs/Glossary/Block-level_content)
box in the layout, starting on a new line and taking up the full width
available in their containing block.
:::

## Try it {#try_it}

::: section-content
::: iframe
::: {.output-header .border-rounded-top}
#### HTML Demo: \<h1-h6\> {#html-demo-h1-h6 .output-heading}

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
    <h1>Beetles</h1>
    <h2>External morphology</h2>
    <h3>Head</h3>
    <h4>Mouthparts</h4>
    <h3>Thorax</h3>
    <h4>Prothorax</h4>
    <h4>Pterothorax</h4>
:::
:::

::: {#css-panel .section .hidden tabindex="0" role="tabpanel" aria-labelledby="css" aria-hidden="true"}
::: {#css-editor}
    h1,
    h2,
    h3,
    h4 {
      margin: 0.1rem 0;
    }

    h1 {
      font-size: 2rem;
    }

    h2 {
      font-size: 1.5rem;
      padding-left: 20px;
    }

    h3 {
      font-size: 1.2rem;
      padding-left: 40px;
    }

    h4 {
      font-size: 1rem;
      font-style: italic;
      padding-left: 60px;
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
<td><a href="../content_categories#flow_content">Flow content</a>,
heading content, palpable content.</td>
</tr>
<tr class="even">
<th scope="row">Permitted content</th>
<td><a href="../content_categories#phrasing_content">Phrasing
content</a>.</td>
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
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/heading_role">heading</a></td>
</tr>
<tr class="even">
<th scope="row">Permitted ARIA roles</th>
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/tab_role"><code>tab</code></a>,
<a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/presentation_role"><code>presentation</code></a>
or <a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/none_role"><code>none</code></a></td>
</tr>
<tr class="odd">
<th scope="row">DOM interface</th>
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLHeadingElement"><code>HTMLHeadingElement</code></a></td>
</tr>
</tbody>
</table>

</figure>
:::

## Attributes

::: section-content
These elements only include the [global
attributes](../global_attributes).
:::

## Usage notes {#usage_notes}

::: section-content
-   Heading information can be used by user agents to construct a table
    of contents for a document automatically.
-   Do not use heading elements to resize text. Instead, use the
    [CSS](https://developer.mozilla.org/en-US/docs/Glossary/CSS)
    [`font-size`](https://developer.mozilla.org/en-US/docs/Web/CSS/font-size)
    property.
-   Do not skip heading levels: always start from `<h1>`, followed by
    `<h2>` and so on.
:::

### Avoid using multiple `<h1>` elements on one page {#avoid_using_multiple_h1_elements_on_one_page}

::: section-content
While using multiple `<h1>` elements on one page is allowed by the HTML
standard (as long as they are not [nested](#nesting)), this is not
considered a best practice. A page should generally have a single `<h1>`
element that describes the content of the page (similar to the
document\'s [`<title> element`](title)).

::: {#sect1 .notecard .note}
**Note:** Nesting multiple `<h1>` elements in nested [sectioning
elements](../element#content_sectioning) was allowed in older versions
of the HTML standard. However, this was never considered a best practice
and is now non-conforming. Read more in [There Is No Document Outline
Algorithm](https://adrianroselli.com/2016/08/there-is-no-document-outline-algorithm.html){target="_blank"}.
:::

Prefer using only one `<h1>` per page and [nest headings](#nesting)
without skipping levels.
:::

## Examples

### All headings {#all_headings}

::: section-content
The following code shows all the heading levels, in use.

::: code-example
[html]{.language-name}

``` {signature="9bKrXasxxQvsi8ieaZehRoRpvBdzCV2RzPxKK3WFBbg=" data-language="html"}
<h1>Heading level 1</h1>
<h2>Heading level 2</h2>
<h3>Heading level 3</h3>
<h4>Heading level 4</h4>
<h5>Heading level 5</h5>
<h6>Heading level 6</h6>
```
:::

::: {#sect2 .code-example}
::: iframe
:::
:::
:::

### Example page {#example_page}

::: section-content
The following code shows a few headings with some content under them.

::: code-example
[html]{.language-name}

``` {signature="/q/ebtQxmwHf0i0DJSBy/YOxhgozik1/K9oKgUa8csM=" data-language="html"}
<h1>Heading elements</h1>
<h2>Summary</h2>
<p>Some text here…</p>

<h2>Examples</h2>
<h3>Example 1</h3>
<p>Some text here…</p>

<h3>Example 2</h3>
<p>Some text here…</p>

<h2>See also</h2>
<p>Some text here…</p>
```
:::

::: {#sect3 .code-example}
::: iframe
:::
:::
:::

## Accessibility concerns {#accessibility_concerns}

### Navigation

::: section-content
A common navigation technique for users of screen reading software is to
quickly jump from heading to heading in order to determine the content
of the page. Because of this, it is important to not skip one or more
heading levels. Doing so may create confusion, as the person navigating
this way may be left wondering where the missing heading is.

**Don\'t do this:**

::: code-example
[html]{.language-name}

``` {signature="1xgyFjhXWCddMjfwMXZ9TLfCbTHjfBtWLxFuOuHWmrc=" data-language="html"}
<h1>Heading level 1</h1>
<h3>Heading level 3</h3>
<h4>Heading level 4</h4>
```
:::

**Prefer this:**

::: code-example
[html]{.language-name}

``` {signature="vkLI2f26Lj58rZ9ffPjxGfuSGyYKcAC+D+0LzrdqMyQ=" data-language="html"}
<h1>Heading level 1</h1>
<h2>Heading level 2</h2>
<h3>Heading level 3</h3>
```
:::

#### Nesting

Headings may be nested as subsections to reflect the organization of the
content of the page. Most screen readers can also generate an ordered
list of all the headings on a page, which can help a person quickly
determine the hierarchy of the content:

1.  `h1` Beetles
    1.  `h2` Etymology
    2.  `h2` Distribution and Diversity
    3.  `h2` Evolution
        1.  `h3` Late Paleozoic
        2.  `h3` Jurassic
        3.  `h3` Cretaceous
        4.  `h3` Cenozoic
    4.  `h2` External Morphology
        1.  `h3` Head
            1.  `h4` Mouthparts
        2.  `h3` Thorax
            1.  `h4` Prothorax
            2.  `h4` Pterothorax
        3.  `h3` Legs
        4.  `h3` Wings
        5.  `h3` Abdomen

When headings are nested, heading levels may be \"skipped\" when closing
a subsection.

-   [Headings • Page Structure • WAI Web Accessibility
    Tutorials](https://www.w3.org/WAI/tutorials/page-structure/headings/){target="_blank"}
-   [MDN Understanding WCAG, Guideline 1.3
    explanations](https://developer.mozilla.org/en-US/docs/Web/Accessibility/Understanding_WCAG/Perceivable#guideline_1.3_%E2%80%94_create_content_that_can_be_presented_in_different_ways)
-   [Understanding Success Criterion 1.3.1 \| W3C Understanding WCAG
    2.0](https://www.w3.org/TR/UNDERSTANDING-WCAG20/content-structure-separation-programmatic.html){target="_blank"}
-   [MDN Understanding WCAG, Guideline 2.4
    explanations](https://developer.mozilla.org/en-US/docs/Web/Accessibility/Understanding_WCAG/Operable#guideline_2.4_%E2%80%94_navigable_provide_ways_to_help_users_navigate_find_content_and_determine_where_they_are)
-   [Understanding Success Criterion 2.4.1 \| W3C Understanding WCAG
    2.0](https://www.w3.org/TR/UNDERSTANDING-WCAG20/navigation-mechanisms-skip.html){target="_blank"}
-   [Understanding Success Criterion 2.4.6 \| W3C Understanding WCAG
    2.0](https://www.w3.org/TR/UNDERSTANDING-WCAG20/navigation-mechanisms-descriptive.html){target="_blank"}
-   [Understanding Success Criterion 2.4.10 \| W3C Understanding WCAG
    2.0](https://www.w3.org/TR/UNDERSTANDING-WCAG20/navigation-mechanisms-headings.html){target="_blank"}
:::

### Labeling section content {#labeling_section_content}

::: section-content
Another common navigation technique for users of screen reading software
is to generate a list of [sectioning
content](../element#content_sectioning) and use it to determine the
page\'s layout.

Sectioning content can be labeled using a combination of the
[`aria-labelledby`](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Attributes/aria-labelledby)
and [`id`](../global_attributes#id) attributes, with the label concisely
describing the purpose of the section. This technique is useful for
situations where there is more than one sectioning element on the same
page.

#### Sectioning content examples {#sectioning_content_examples}

::: code-example
[html]{.language-name}

``` {signature="h5MhSqZruH8k0uFBY91EUCvMBA2rnP7o9m1biyT+JxM=" data-language="html"}
<header>
  <nav aria-labelledby="primary-navigation">
    <h2 id="primary-navigation">Primary navigation</h2>
    <!-- navigation items -->
  </nav>
</header>

<!-- page content -->

<footer>
  <nav aria-labelledby="footer-navigation">
    <h2 id="footer-navigation">Footer navigation</h2>
    <!-- navigation items -->
  </nav>
</footer>
```
:::

::: {#sect4 .code-example}
::: iframe
:::
:::

In this example, screen reading technology would announce that there are
two [`<nav>`](nav) sections, one called \"Primary navigation\" and one
called \"Footer navigation\". If labels were not provided, the person
using screen reading software may have to investigate each `nav`
element\'s contents to determine their purpose.

-   [Using the aria-labelledby
    attribute](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Attributes/aria-labelledby)
-   [Labeling Regions • Page Structure • W3C WAI Web Accessibility
    Tutorials](https://www.w3.org/WAI/tutorials/page-structure/labels/#using-aria-labelledby){target="_blank"}
:::

## Specifications

::: _table
  -------------------------------------------------------------------------------------------------------------------------------------------------
  Specification
  -------------------------------------------------------------------------------------------------------------------------------------------------
  [HTML Standard\
  [\#
  the-h1,-h2,-h3,-h4,-h5,-and-h6-elements]{.small}](https://html.spec.whatwg.org/multipage/sections.html#the-h1,-h2,-h3,-h4,-h5,-and-h6-elements)

  -------------------------------------------------------------------------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
                       Desktop                                                         Mobile                                                                                   
  -------------------- --------- ------ --------- ------------------- ------- -------- ----------------- ---------------- --------------------- --------------- --------------- ------------------
                       Chrome    Edge   Firefox   Internet Explorer   Opera   Safari   WebView Android   Chrome Android   Firefox for Android   Opera Android   Safari on IOS   Samsung Internet
  `Heading_Elements`   1         12     1         Yes                 15      ≤4       4.4               18               4                     14              ≤3.2            1.0
:::

## See also {#see_also}

::: section-content
-   [`<p>`](p)
-   [``](div)
-   [`<section>`](section)
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Element/Heading_Elements](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/Heading_Elements){._attribution-link}
:::
