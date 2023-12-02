

# \<article\>: The Article Contents element



::: section-content
The `<article>` [HTML](../index) element represents a self-contained
composition in a document, page, application, or site, which is intended
to be independently distributable or reusable (e.g., in syndication).
Examples include: a forum post, a magazine or newspaper article, or a
blog entry, a product card, a user-submitted comment, an interactive
widget or gadget, or any other independent item of content.
:::

## Try it {#try_it}

::: section-content
::: iframe
::: {.output-header .border-rounded-top}
#### HTML Demo: \<article\> {#html-demo-article .output-heading}

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
    <article class="forecast">
      <h1>Weather forecast for Seattle</h1>
      <article class="day-forecast">
        <h2>03 March 2018</h2>
        <p>Rain.</p>
      </article>
      <article class="day-forecast">
        <h2>04 March 2018</h2>
        <p>Periods of rain.</p>
      </article>
      <article class="day-forecast">
        <h2>05 March 2018</h2>
        <p>Heavy rain.</p>
      </article>
    </article>
:::
:::

::: {#css-panel .section .hidden tabindex="0" role="tabpanel" aria-labelledby="css" aria-hidden="true"}
::: {#css-editor}
    .forecast {
      margin: 0;
      padding: 0.3rem;
      background-color: #eee;
    }

    .forecast > h1,
    .day-forecast {
      margin: 0.5rem;
      padding: 0.3rem;
      font-size: 1.2rem;
    }

    .day-forecast {
      background: right/contain content-box border-box no-repeat
        url('/media/examples/rain.svg') white;
    }

    .day-forecast > h2,
    .day-forecast > p {
      margin: 0.2rem;
      font-size: 1rem;
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

A given document can have multiple articles in it; for example, on a
blog that shows the text of each article one after another as the reader
scrolls, each post would be contained in an `<article>` element,
possibly with one or more `<section>`s within.

<figure class="table-container">
<div class="_table">
<table class="properties">
<tbody>
<tr class="odd">
<th scope="row"><a href="../content_categories">Content
categories</a></th>
<td><a href="../content_categories#flow_content">Flow content</a>, <a
href="../content_categories#sectioning_content">sectioning content</a>,
<a href="../content_categories#palpable_content">palpable
content</a></td>
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
href="../content_categories#flow_content">flow content</a>. Note that an
<code>&lt;article&gt;</code> element must not be a descendant of an <a
href="address"><code>&lt;address&gt;</code></a> element.</td>
</tr>
<tr class="odd">
<th scope="row">Implicit ARIA role</th>
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/article_role"><code>article</code></a></td>
</tr>
<tr class="even">
<th scope="row">Permitted ARIA roles</th>
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/application_role"><code>application</code></a>,
<a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/document_role"><code>document</code></a>,
<a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/feed_role"><code>feed</code></a>,
<a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/main_role"><code>main</code></a>,
<a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/none_role"><code>none</code></a>,
<a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/presentation_role"><code>presentation</code></a>,
<a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/region_role"><code>region</code></a></td>
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
-   Each `<article>` should be identified, typically by including a
    heading ([`<h1>` - `<h6>`](heading_elements) element) as a child of
    the `<article>` element.
-   When an `<article>` element is nested, the inner element represents
    an article related to the outer element. For example, the comments
    of a blog post can be `<article>` elements nested in the `<article>`
    representing the blog post.
-   Author information of an `<article>` element can be provided through
    the [`<address>`](address) element, but it doesn\'t apply to nested
    `<article>` elements.
-   The publication date and time of an `<article>` element can be
    described using the [`datetime`](time#datetime) attribute of a
    [`<time>`](time) element.
:::

## Examples

::: section-content
::: code-example
[html]{.language-name}

``` {signature="vNOmQ8f+S5cgrfrDUuO1OpmTWH1C8HA5WSh/JnlFC4E=" data-language="html"}
<article class="film_review">
  <h2>Jurassic Park</h2>
  <section class="main_review">
    <h3>Review</h3>
    <p>Dinos were great!</p>
  </section>
  <section class="user_reviews">
    <h3>User reviews</h3>
    <article class="user_review">
      <h4>Too scary!</h4>
      <p>Way too scary for me.</p>
      <footer>
        <p>
          Posted on
          <time datetime="2015-05-16 19:00">May 16</time>
          by Lisa.
        </p>
      </footer>
    </article>
    <article class="user_review">
      <h4>Love the dinos!</h4>
      <p>I agree, dinos are my favorite.</p>
      <footer>
        <p>
          Posted on
          <time datetime="2015-05-17 19:00">May 17</time>
          by Tom.
        </p>
      </footer>
    </article>
  </section>
  <footer>
    <p>
      Posted on
      <time datetime="2015-05-15 19:00">May 15</time>
      by Staff.
    </p>
  </footer>
</article>
```
:::
:::

## Result

::: section-content
::: {#sect1 .code-example}
::: iframe
:::
:::
:::

## Specifications

::: _table
  ---------------------------------------------------------------------------------------------------------
  Specification
  ---------------------------------------------------------------------------------------------------------
  [HTML Standard\
  [\#
  the-article-element]{.small}](https://html.spec.whatwg.org/multipage/sections.html#the-article-element)

  ---------------------------------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
              Desktop                                                         Mobile                                                                                   
  ----------- --------- ------ --------- ------------------- ------- -------- ----------------- ---------------- --------------------- --------------- --------------- ------------------
              Chrome    Edge   Firefox   Internet Explorer   Opera   Safari   WebView Android   Chrome Android   Firefox for Android   Opera Android   Safari on IOS   Samsung Internet
  `article`   5         12     4         9                   11.1    5        4.4               18               4                     11.1            4.2             1.0
:::

## See also {#see_also}

::: section-content
-   Other section-related elements: [`<body>`](body), [`<nav>`](nav),
    [`<section>`](section), [`<aside>`](aside), [h1](heading_elements),
    [h2](heading_elements), [h3](heading_elements),
    [h4](heading_elements), [h5](heading_elements),
    [h6](heading_elements), [`<hgroup>`](hgroup), [`<header>`](header),
    [`<footer>`](footer), [`<address>`](address)
-   [Using HTML sections and outlines](heading_elements)
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Element/article](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/article){._attribution-link}
:::
