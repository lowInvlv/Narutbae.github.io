

# \<title\>: The Document Title element



::: section-content
The `<title>` [HTML](../index) element defines the document\'s title
that is shown in a
[browser](https://developer.mozilla.org/en-US/docs/Glossary/Browser)\'s
title bar or a page\'s tab. It only contains text; tags within the
element are ignored.

::: code-example
[html]{.language-name}

``` {signature="edRg81zzSeEMPE8aOW5jVNIFmQrub1mPG/jF2XRIgJc=" data-language="html"}
<title>Grandma's Heavy Metal Festival Journal</title>
```
:::

<figure class="table-container">
<div class="_table">
<table class="properties">
<tbody>
<tr class="odd">
<th scope="row"><a href="../content_categories">Content
categories</a></th>
<td><a href="../content_categories#metadata_content">Metadata
content</a>.</td>
</tr>
<tr class="even">
<th scope="row">Permitted content</th>
<td>Text that is not inter-element <a
href="https://developer.mozilla.org/en-US/docs/Glossary/Whitespace">whitespace</a>.</td>
</tr>
<tr class="odd">
<th scope="row">Tag omission</th>
<td>Both opening and closing tags are required. Note that leaving off
<code>&lt;/title&gt;</code> should cause the browser to ignore the rest
of the page.</td>
</tr>
<tr class="even">
<th scope="row">Permitted parents</th>
<td>A <a href="head"><code>&lt;head&gt;</code></a> element that contains
no other <a href="title"
aria-current="page"><code>&lt;title&gt;</code></a> element.</td>
</tr>
<tr class="odd">
<th scope="row">Implicit ARIA role</th>
<td><a href="https://www.w3.org/TR/html-aria/#dfn-no-corresponding-role"
target="_blank">No corresponding role</a></td>
</tr>
<tr class="even">
<th scope="row">Permitted ARIA roles</th>
<td>No <code>role</code> permitted.</td>
</tr>
<tr class="odd">
<th scope="row">DOM interface</th>
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLTitleElement"><code>HTMLTitleElement</code></a></td>
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
The `<title>` element is always used within a page\'s [`<head>`](head)
block.
:::

### Page titles and SEO {#page_titles_and_seo}

::: section-content
The contents of a page title can have significant implications for
search engine optimization
([SEO](https://developer.mozilla.org/en-US/docs/Glossary/SEO)). In
general, a longer, descriptive title performs better than short or
generic titles. The content of the title is one of the components used
by search engine algorithms to decide the order in which to list pages
in search results. Also, the title is the initial \"hook\" by which you
grab the attention of readers glancing at the search results page.

A few guidelines and tips for composing good titles:

-   Avoid one- or two-word titles. Use a descriptive phrase, or a
    term-definition pairing for glossary or reference-style pages.
-   Search engines typically display about the first 55--60 characters
    of a page title. Text beyond that may be lost, so try not to have
    titles longer than that. If you must use a longer title, make sure
    the important parts come earlier and that nothing critical is in the
    part of the title that is likely to be dropped.
-   Don\'t use \"keyword blobs.\" If your title is just a list of words,
    algorithms often reduce your page\'s position in the search results.
-   Try to make sure your titles are as unique as possible within your
    own site. Duplicate---or near-duplicate---titles can contribute to
    inaccurate search results.
:::

## Examples

::: section-content
::: code-example
[html]{.language-name}

``` {signature="XI/Y/25/eRguLF4UTRF+Tk0Z3niGh6Fl5659F6//J2s=" data-language="html"}
<title>Awesome interesting stuff</title>
```
:::

This example establishes a page whose title (as displayed at the top of
the window or in the window\'s tab) as \"Awesome interesting stuff\".
:::

## Accessibility concerns {#accessibility_concerns}

::: section-content
It is important to provide an accurate and concise title to describe the
page\'s purpose.

A common navigation technique for users of assistive technology is to
read the page title and infer the content the page contains. This is
because navigating into a page to determine its content can be a
time-consuming and potentially confusing process. Titles should be
unique to every page of a website, ideally surfacing the primary purpose
of the page first, followed by the name of the website. Following this
pattern will help ensure that the primary purpose of the page is
announced by a screen reader first. This provides a far better
experience than having to listen to the name of a website before the
unique page title, for every page a user navigates to in the same
website.
:::

### Examples {#examples_2}

::: section-content
::: code-example
[html]{.language-name}

``` {signature="Tg7WXTeW2+DNcrDL1awdgLAOR5H0h//QSIH0tfBOZpU=" data-language="html"}
<title>Menu - Blue House Chinese Food - FoodYum: Online takeout today!</title>
```
:::

If a form submission contains errors and the submission re-renders the
current page, the title can be used to help make users aware of any
errors with their submission. For instance, update the page `title`
value to reflect significant page state changes (such as form validation
problems).

::: code-example
[html]{.language-name}

``` {signature="4ojY91Z2/aT2aLQDSY1Azjnxii2Ey8JaJykUF74pDpA=" data-language="html"}
<title>
  2 errors - Your order - Sea Food Store - Food: Online takeout today!
</title>
```
:::

::: {#sect1 .notecard .note}
**Note:** Presently, dynamically updating a page\'s title will not be
automatically announced by screen readers. If you are going to update
the page title to reflect significant changes to a page\'s state, then
the use of [ARIA Live
Regions](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/ARIA_Live_Regions)
may be necessary, as well.
:::

-   [MDN Understanding WCAG, Guideline 2.4
    explanations](https://developer.mozilla.org/en-US/docs/Web/Accessibility/Understanding_WCAG/Operable#guideline_2.4_%E2%80%94_navigable_provide_ways_to_help_users_navigate_find_content_and_determine_where_they_are)
-   [Understanding Success Criterion 2.4.2 \| W3C Understanding WCAG
    2.1](https://www.w3.org/WAI/WCAG21/Understanding/page-titled.html){target="_blank"}
:::

## Specifications

::: _table
  ------------------------------------------------------------------------------------------------------
  Specification
  ------------------------------------------------------------------------------------------------------
  [HTML Standard\
  [\#
  the-title-element]{.small}](https://html.spec.whatwg.org/multipage/semantics.html#the-title-element)

  ------------------------------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
            Desktop                                                         Mobile                                                                                   
  --------- --------- ------ --------- ------------------- ------- -------- ----------------- ---------------- --------------------- --------------- --------------- ------------------
            Chrome    Edge   Firefox   Internet Explorer   Opera   Safari   WebView Android   Chrome Android   Firefox for Android   Opera Android   Safari on IOS   Samsung Internet
  `title`   1         12     1         1                   15      1        4.4               18               4                     14              1               1.0
:::

## See also {#see_also}

::: section-content
-   SVG
    [`<title>`](https://developer.mozilla.org/en-US/docs/Web/SVG/Element/title)
    element
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Element/title](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/title){._attribution-link}
:::
