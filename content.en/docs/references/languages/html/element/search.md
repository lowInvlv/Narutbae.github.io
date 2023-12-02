

# \<search\>: The generic search element



::: section-content
The `<search>` [HTML](../index) element is a container representing the
parts of the document or application with form controls or other content
related to performing a search or filtering operation. The `<search>`
element semantically identifies the purpose of the element\'s contents
as having search or filtering capabilities. The search or filtering
functionality can be for the website or application, the current web
page or document, or the entire Internet or subsection thereof.
:::

## Attributes

::: section-content
This element only includes the [global
attributes](../global_attributes).
:::

## Usage notes {#usage_notes}

::: section-content
The `<search>` element is not for presenting search results. Rather,
search or filtered results should be presented as part of the main
content of that web page. That said, suggestions and links that are part
of \"quick search\" functionality within the search or filtering
functionality are appropriately nested within the contents of the
`<search>` element as they are search features.
:::

## Accessibility

::: section-content
The `<search>` element defines a
[`search`](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/search_role)
landmark. This removes the need for adding `role=search` to a
[`<form>`](form) element.
:::

## Examples

### Header search form {#header_search_form}

::: section-content
This example demonstrates the use of `<search>` as the container for a
search within a website header to perform a simple site-wide search. The
`<search>` is a semantic container for the [`<form>`](form) that submits
the user-entered search query to a server.

#### HTML

::: code-example
[html]{.language-name}

``` {signature="NFWNkiEba3UjxsSVNFkVmI/c3rs4URpSOADLZOLZEQc=" data-language="html"}
<header>
  <h1>Movie website</h1>
  <search>
    <form action="./search/">
      <label for="movie">Find a Movie</label>
      <input type="search" id="movie" name="q" />
      <button type="submit">Search</button>
    </form>
  </search>
</header>
```
:::

#### Result

::: {#sect1 .code-example}
::: iframe
:::
:::
:::

### Web app search {#web_app_search}

::: section-content
This example demonstrates potential DOM content when dynamically
including JavaScript search functionality in a web application. When
search functionality is implemented entirely with JavaScript, if no form
is submitted, neither a [`<form>`](form) element nor a submit
[`<button>`](button) is required. For semantics, the `<search>` element
is included to contain the search and filtering capabilities.

#### HTML {#html_2}

::: code-example
[html]{.language-name}

``` {signature="Ge7fxrSKVSmGBd7NvisxguVLE/ye/NEk1tSiiPlRa50=" data-language="html"}
<search>
  <label>
    Find and filter your query
    <input type="search" id="query" />
  </label>
  <label>
    <input type="checkbox" id="exact-only" />
    Exact matches only
  </label>

  <section>
    <h3>Results:</h3>
    <ul id="results">
      <!-- search result content -->
    </ul>
    <output id="no-results">
      <!-- no results content -->
    </output>
  </section>
</search>
```
:::

#### Result {#result_2}

::: {#sect2 .code-example}
::: iframe
:::
:::

::: {#sect3 .notecard .note}
**Note:** Remember that some users don\'t have JavaScript, and none of
your users have JavaScript running until the JavaScript is successfully
downloaded, parsed, and executed, ensure your users can access the
content of your site with JavaScript disabled.
:::
:::

### Multiple searches {#multiple_searches}

::: section-content
This example demonstrates a page with two search features. The first is
a global site search located on the header. The second is a search and
filter based on the page context, in our example a car search.

#### HTML {#html_3}

::: code-example
[html]{.language-name}

``` {signature="3Km2JjJHwHj8LKdbgOsp3GRsJO+4rxresokjcPsba/A=" data-language="html"}
<body>
  <header>
    <h1>Car rental agency</h1>
    <search title="Website">...</search>
  </header>
  <main>
    <h2>Cars available for rent</h2>
    <search title="Cars">
      <h3>Filter results</h3>
      ...
    </search>
    <article>
      <!-- search result content -->
    </article>
  </main>
</body>
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
<td><a href="../content_categories#flow_content">Flow content</a>, <a
href="../content_categories#palpable_content">palpable content</a>.</td>
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
<th scope="row">Implicit ARIA role</th>
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/search_role"><code>search</code></a></td>
</tr>
<tr class="odd">
<th scope="row">Permitted ARIA roles</th>
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/form_role"><code>form</code></a>,
<a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/group_role"><code>group</code></a>,
<a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/none_role"><code>none</code></a>,
<a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/presentation_role"><code>presentation</code></a>,
<a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/region_role"><code>region</code></a>,
<a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/search_role"><code>search</code></a></td>
</tr>
<tr class="even">
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
  ---------------------------------------------------------------------------------------------------------------
  Specification
  ---------------------------------------------------------------------------------------------------------------
  [HTML Standard\
  [\#
  the-search-element]{.small}](https://html.spec.whatwg.org/multipage/grouping-content.html#the-search-element)

  ---------------------------------------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
             Desktop                                                         Mobile                                                                                   
  ---------- --------- ------ --------- ------------------- ------- -------- ----------------- ---------------- --------------------- --------------- --------------- ------------------
             Chrome    Edge   Firefox   Internet Explorer   Opera   Safari   WebView Android   Chrome Android   Firefox for Android   Opera Android   Safari on IOS   Samsung Internet
  `search`   118       118    118       No                  104     17       118               118              118                   No              17              No
:::

## See also {#see_also}

::: section-content
-   Other search-related elements: [`<header>`](header),
    [`<footer>`](footer), [`<aside>`](aside), [`<nav>`](nav),
    [`<form>`](form)
-   [ARIA: Search
    role](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/search_role)
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Element/search](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/search){._attribution-link}
:::
