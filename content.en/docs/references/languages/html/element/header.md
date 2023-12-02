

# \<header\>



::: section-content
The `<header>` [HTML](../index) element represents introductory content,
typically a group of introductory or navigational aids. It may contain
some heading elements but also a logo, a search form, an author name,
and other elements.
:::

## Try it {#try_it}

::: section-content
::: iframe
::: {.output-header .border-rounded-top}
#### HTML Demo: \<header\> {#html-demo-header .output-heading}

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
    <header>
      <a class="logo" href="#">Cute Puppies Express!</a>
    </header>

    <article>
      <header>
        <h1>Beagles</h1>
        <time>08.12.2014</time>
      </header>
      <p>I love beagles <em>so</em> much! Like, really, a lot. They’re adorable and their ears are so, so snuggly soft!</p>
    </article>
:::
:::

::: {#css-panel .section .hidden tabindex="0" role="tabpanel" aria-labelledby="css" aria-hidden="true"}
::: {#css-editor}
    .logo {
      background: left / cover url('/media/examples/puppy-header-logo.jpg');
      display: flex;
      height: 120px;
      align-items: center;
      justify-content: center;
      font:
        bold calc(1em + 2 * (100vw - 120px) / 100) 'Dancing Script',
        fantasy;
      color: #ff0083;
      text-shadow: #000 2px 2px 0.2rem;
    }

    header > h1 {
      margin-bottom: 0;
    }

    header > time {
      font: italic 0.7rem sans-serif;
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

## Usage notes {#usage_notes}

::: section-content
The `<header>` element has an identical meaning to the site-wide
[`banner`](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/banner_role)
landmark role, unless nested within sectioning content. Then, the
`<header>` element is not a landmark.

The `<header>` element can define a global site header, described as a
`banner` in the accessibility tree. It usually includes a logo, company
name, search feature, and possibly the global navigation or a slogan. It
is generally located at the top of the page.

Otherwise, it is a `section` in the accessibility tree, and usually
contains the surrounding section\'s heading (an `h1` -- `h6` element)
and optional subheading, but this is **not** required.
:::

### Historical Usage {#historical_usage}

::: section-content
The `<header>` element originally existed at the very beginning of HTML
for headings. It is seen in [the very first
website](http://info.cern.ch/){target="_blank"}. At some point, headings
became [`<h1>` through `<h6>`](heading_elements), allowing `<header>` to
be free to fill a different role.
:::

## Attributes

::: section-content
This element only includes the [global
attributes](../global_attributes).
:::

## Examples

### Page Header {#page_header}

::: section-content
::: code-example
[html]{.language-name}

``` {signature="L7G//UQoT92KxgsueTIW6FV6GliHEvXaRlvwzGdZISw=" data-language="html"}
<header>
  <h1>Main Page Title</h1>
  <img src="mdn-logo-sm.png" alt="MDN logo" />
</header>
```
:::

#### Result

::: {#sect1 .code-example}
::: iframe
:::
:::
:::

### Article Header {#article_header}

::: section-content
::: code-example
[html]{.language-name}

``` {signature="8qwCAfsFt1eZe7t6xqKtQ2bLcTo97qCPxkqbd0pjmU4=" data-language="html"}
<article>
  <header>
    <h2>The Planet Earth</h2>
    <p>
      Posted on Wednesday, <time datetime="2017-10-04">4 October 2017</time> by
      Jane Smith
    </p>
  </header>
  <p>
    We live on a planet that's blue and green, with so many things still unseen.
  </p>
  <p><a href="https://example.com/the-planet-earth/">Continue reading…</a></p>
</article>
```
:::

#### Result {#result_2}

::: {#sect2 .code-example}
::: iframe
:::
:::
:::

## Accessibility

::: section-content
The `<header>` element defines a
[`banner`](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/banner_role)
landmark when its context is the [`<body>`](body) element. The HTML
header element is not considered a banner landmark when it is descendant
of an [`<article>`](article), [`<aside>`](aside), [`<main>`](main),
[`<nav>`](nav), or [`<section>`](section) element.
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
href="../content_categories#palpable_content">palpable content</a>.</td>
</tr>
<tr class="even">
<th scope="row">Permitted content</th>
<td><a href="../content_categories#flow_content">Flow content</a>, but
with no <code>&lt;header&gt;</code> or <a
href="footer"><code>&lt;footer&gt;</code></a> descendant.</td>
</tr>
<tr class="odd">
<th scope="row">Tag omission</th>
<td>None, both the starting and ending tag are mandatory.</td>
</tr>
<tr class="even">
<th scope="row">Permitted parents</th>
<td>Any element that accepts <a
href="../content_categories#flow_content">flow content</a>. Note that a
<code>&lt;header&gt;</code> element must not be a descendant of an <a
href="address"><code>&lt;address&gt;</code></a>, <a
href="footer"><code>&lt;footer&gt;</code></a> or another <a
href="header" aria-current="page"><code>&lt;header&gt;</code></a>
element.</td>
</tr>
<tr class="odd">
<th scope="row">Implicit ARIA role</th>
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/banner_role">banner</a>,
or <a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/generic_role">generic</a>
if a descendant of an <a href="article"><code>article</code></a>, <a
href="aside"><code>aside</code></a>, <a
href="main"><code>main</code></a>, <a href="nav"><code>nav</code></a> or
<a href="section"><code>section</code></a> element, or an element with
<code>role=</code><a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/article_role"><code>article</code></a>,
<a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/complementary_role"><code>complementary</code></a>,
<a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/main_role"><code>main</code></a>,
<a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/navigation_role"><code>navigation</code></a>
or <a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/region_role"><code>region</code></a></td>
</tr>
<tr class="even">
<th scope="row">Permitted ARIA roles</th>
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/group_role"><code>group</code></a>,
<a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/presentation_role"><code>presentation</code></a>
or <a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/none_role"><code>none</code></a></td>
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
  -------------------------------------------------------------------------------------------------------
  Specification
  -------------------------------------------------------------------------------------------------------
  [HTML Standard\
  [\#
  the-header-element]{.small}](https://html.spec.whatwg.org/multipage/sections.html#the-header-element)

  -------------------------------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
             Desktop                                                         Mobile                                                                                   
  ---------- --------- ------ --------- ------------------- ------- -------- ----------------- ---------------- --------------------- --------------- --------------- ------------------
             Chrome    Edge   Firefox   Internet Explorer   Opera   Safari   WebView Android   Chrome Android   Firefox for Android   Opera Android   Safari on IOS   Samsung Internet
  `header`   5         12     4         9                   11.1    5        4.4               18               4                     11.1            4.2             1.0
:::

## See also {#see_also}

::: section-content
-   Other section-related elements: [`<body>`](body), [`<nav>`](nav),
    [`<article>`](article), [`<aside>`](aside), [h1](heading_elements),
    [h2](heading_elements), [h3](heading_elements),
    [h4](heading_elements), [h5](heading_elements),
    [h6](heading_elements), [`<footer>`](footer),
    [`<section>`](section), [`<address>`](address).
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Element/header](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/header){._attribution-link}
:::
