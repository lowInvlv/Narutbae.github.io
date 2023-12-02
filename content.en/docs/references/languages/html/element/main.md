

# \<main\>



::: section-content
The `<main>` [HTML](../index) element represents the dominant content of
the [`<body>`](body) of a document. The main content area consists of
content that is directly related to or expands upon the central topic of
a document, or the central functionality of an application.
:::

## Try it {#try_it}

::: section-content
::: iframe
::: {.output-header .border-rounded-top}
#### HTML Demo: \<main\> {#html-demo-main .output-heading}

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
    <header>Gecko facts</header>

    <main>
      <p>
        Geckos are a group of usually small, usually nocturnal lizards. They are found on every continent except Australia.
      </p>

      <p>Many species of gecko have adhesive toe pads which enable them to climb walls and even windows.</p>
    </main>
:::
:::

::: {#css-panel .section .hidden tabindex="0" role="tabpanel" aria-labelledby="css" aria-hidden="true"}
::: {#css-editor}
    header {
      font:
        bold calc(0.025 * (100vw)) Arial,
        sans-serif;
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

A document mustn\'t have more than one `<main>` element that doesn\'t
have the [`hidden`](../global_attributes#hidden) attribute specified.

<figure class="table-container">
<div class="_table">
<table class="properties">
<tbody>
<tr class="odd">
<th scope="row"><a href="../content_categories">Content
categories</a></th>
<td><a href="../content_categories#flow_content">Flow content</a>,
palpable content.</td>
</tr>
<tr class="even">
<th scope="row">Permitted content</th>
<td><a href="../content_categories#flow_content">Flow content</a>.</td>
</tr>
<tr class="odd">
<th scope="row">Tag omission</th>
<td>None; both the starting and ending tags are mandatory.</td>
</tr>
<tr class="even">
<th scope="row">Permitted parents</th>
<td>Where <a href="../content_categories#flow_content">flow content</a>
is expected, but only if it is a <a
href="https://html.spec.whatwg.org/multipage/grouping-content.html#hierarchically-correct-main-element"
target="_blank">hierarchically correct <code>main</code>
element</a>.</td>
</tr>
<tr class="odd">
<th scope="row">Implicit ARIA role</th>
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/main_role"><code>main</code></a></td>
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
The content of a `<main>` element should be unique to the document.
Content that is repeated across a set of documents or document sections
such as sidebars, navigation links, copyright information, site logos,
and search forms shouldn\'t be included unless the search form is the
main function of the page.

`<main>` doesn\'t contribute to the document\'s outline; that is, unlike
elements such as [`<body>`](body), headings such as
[h2](heading_elements), and such, `<main>` doesn\'t affect the
[DOM\'s](https://developer.mozilla.org/en-US/docs/Glossary/DOM) concept
of the structure of the page. It\'s strictly informative.
:::

## Examples

::: section-content
::: code-example
[html]{.language-name}

``` {signature="tyfb3BYxWBtdvVUJ+iaJ7d3DOTT4AcsjzuhhiNZbuFA=" data-language="html"}
<!-- other content -->

<main>
  <h1>Apples</h1>
  <p>The apple is the pomaceous fruit of the apple tree.</p>

  <article>
    <h2>Red Delicious</h2>
    <p>
      These bright red apples are the most common found in many supermarkets.
    </p>
    <p>…</p>
    <p>…</p>
  </article>

  <article>
    <h2>Granny Smith</h2>
    <p>These juicy, green apples make a great filling for apple pies.</p>
    <p>…</p>
    <p>…</p>
  </article>
</main>

<!-- other content -->
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

## Accessibility concerns {#accessibility_concerns}

### Landmark

::: section-content
The `<main>` element behaves like a [`main`
landmark](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/main_role)
role.
[Landmarks](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/ARIA_Techniques#landmark_roles)
can be used by assistive technology to quickly identify and navigate to
large sections of the document. Prefer using the `<main>` element over
declaring `role="main"`, unless there are [legacy browser support
concerns](#browser_compatibility).
:::

### Skip navigation {#skip_navigation}

::: section-content
Skip navigation, also known as \"skipnav\", is a technique that allows
an assistive technology user to quickly bypass large sections of
repeated content (main navigation, info banners, etc.). This lets the
user access the main content of the page faster.

Adding an [`id`](../global_attributes#id) attribute to the `<main>`
element lets it be a target of a skip navigation link.

::: code-example
[html]{.language-name}

``` {signature="aBaSk9dQ7yDgTfk+fBabUFcjDX4FCxV/mO+DRQSOZNg=" data-language="html"}
<body>
  <a href="#main-content">Skip to main content</a>

  <!-- navigation and header content -->

  <main id="main-content">
    <!-- main page content -->
  </main>
</body>
```
:::

-   [WebAIM: \"Skip Navigation\"
    Links](https://webaim.org/techniques/skipnav/){target="_blank"}
:::

### Reader mode {#reader_mode}

::: section-content
Browser reader mode functionality looks for the presence of the `<main>`
element, as well as [heading](heading_elements) and [content sectioning
elements](../element#content_sectioning) when converting content into a
specialized reader view.

-   [Building websites for Safari Reader Mode and other reading
    apps.](https://medium.com/@mandy.michael/building-websites-for-safari-reader-mode-and-other-reading-apps-1562913c86c9){target="_blank"}
:::

## Specifications

::: _table
  -----------------------------------------------------------------------------------------------------------
  Specification
  -----------------------------------------------------------------------------------------------------------
  [HTML Standard\
  [\#
  the-main-element]{.small}](https://html.spec.whatwg.org/multipage/grouping-content.html#the-main-element)

  -----------------------------------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
           Desktop                                                         Mobile                                                                                   
  -------- --------- ------ --------- ------------------- ------- -------- ----------------- ---------------- --------------------- --------------- --------------- ------------------
           Chrome    Edge   Firefox   Internet Explorer   Opera   Safari   WebView Android   Chrome Android   Firefox for Android   Opera Android   Safari on IOS   Samsung Internet
  `main`   26        12     21        No                  16      7        4.4               26               21                    14              7               1.5
:::

## See also {#see_also}

::: section-content
-   Basic structural elements: [`<html>`](html), [`<head>`](head),
    [`<body>`](body)
-   Section-related elements: [`<article>`](article),
    [`<aside>`](aside), [`<footer>`](footer), [`<header>`](header), or
    [`<nav>`](nav)
-   [ARIA: Main
    role](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/main_role)
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Element/main](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/main){._attribution-link}
:::
