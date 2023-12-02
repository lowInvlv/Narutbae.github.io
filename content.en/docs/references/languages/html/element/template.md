

# \<template\>: The Content Template element



::: section-content
The `<template>` [HTML](../index) element is a mechanism for holding
[HTML](https://developer.mozilla.org/en-US/docs/Glossary/HTML) that is
not to be rendered immediately when a page is loaded but may be
instantiated subsequently during runtime using JavaScript.

Think of a template as a content fragment that is being stored for
subsequent use in the document. While the parser does process the
contents of the `<template>` element while loading the page, it does so
only to ensure that those contents are valid; the element\'s contents
are not rendered, however.
:::

## Attributes

::: section-content
The only standard attributes that the `<template>` element supports are
the [global attributes](../global_attributes).

In Chromium-based browsers, the `<template>` element also supports a
non-standard [`shadowrootmode`
attribute](https://github.com/mfreed7/declarative-shadow-dom/blob/master/README.md#syntax){target="_blank"},
as part of an experimental [\"Declarative Shadow
DOM\"](https://developer.chrome.com/articles/declarative-shadow-dom/){target="_blank"}
proposal. In supporting browsers, a `<template>` element with the
`shadowrootmode` attribute is detected by the HTML parser and
immediately applied as the shadow root of its parent element.
`shadowrootmode` can take a value of `open` or `closed`; these are
equivalent to the `open` and `closed` values of the
[`Element.attachShadow()`](https://developer.mozilla.org/en-US/docs/Web/API/Element/attachShadow)
`mode` option.

Also, the corresponding
[`HTMLTemplateElement`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLTemplateElement)
interface includes a standard
[`content`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLTemplateElement/content)
property (without an equivalent content/markup attribute). This
`content` property is read-only and holds a
[`DocumentFragment`](https://developer.mozilla.org/en-US/docs/Web/API/DocumentFragment)
that contains the DOM subtree represented by the template. Be careful
when using the `content` property because the returned
`DocumentFragment` can exhibit unexpected behavior. For more details,
see the [Avoiding DocumentFragment
pitfalls](#avoiding_documentfragment_pitfalls) section below.
:::

## Examples

::: section-content
First we start with the HTML portion of the example.

::: code-example
[html]{.language-name}

``` {signature="I8s7uGl9d3MCpGhD4iu/aLbSxzvqaTgHK7jKRNxZOIE=" data-language="html"}
<table id="producttable">
  <thead>
    <tr>
      <td>UPC_Code</td>
      <td>Product_Name</td>
    </tr>
  </thead>
  <tbody>
    <!-- existing data could optionally be included here -->
  </tbody>
</table>

<template id="productrow">
  <tr>
    <td class="record"></td>
    <td></td>
  </tr>
</template>
```
:::

First, we have a table into which we will later insert content using
JavaScript code. Then comes the template, which describes the structure
of an HTML fragment representing a single table row.

Now that the table has been created and the template defined, we use
JavaScript to insert rows into the table, with each row being
constructed using the template as its basis.

::: code-example
[js]{.language-name}

``` {signature="fcTyqG2hfSPp31p+5ZaE2RIpOwoBDb569EosXX5oQh0=" data-language="js"}
// Test to see if the browser supports the HTML template element by checking
// for the presence of the template element's content attribute.
if ("content" in document.createElement("template")) {
  // Instantiate the table with the existing HTML tbody
  // and the row with the template
  const tbody = document.querySelector("tbody");
  const template = document.querySelector("#productrow");

  // Clone the new row and insert it into the table
  const clone = template.content.cloneNode(true);
  let td = clone.querySelectorAll("td");
  td[0].textContent = "1235646565";
  td[1].textContent = "Stuff";

  tbody.appendChild(clone);

  // Clone the new row and insert it into the table
  const clone2 = template.content.cloneNode(true);
  td = clone2.querySelectorAll("td");
  td[0].textContent = "0384928528";
  td[1].textContent = "Acme Kidney Beans 2";

  tbody.appendChild(clone2);
} else {
  // Find another way to add the rows to the table because
  // the HTML template element is not supported.
}
```
:::

The result is the original HTML table, with two new rows appended to it
via JavaScript:

::: {#sect1 .code-example}
::: iframe
:::
:::
:::

## Avoiding DocumentFragment pitfalls {#avoiding_documentfragment_pitfalls}

::: section-content
When a
[`DocumentFragment`](https://developer.mozilla.org/en-US/docs/Web/API/DocumentFragment)
value is passed,
[`Node.appendChild`](https://developer.mozilla.org/en-US/docs/Web/API/Node/appendChild)
and similar methods move only the *child nodes* of that value into the
target node. Therefore, it is usually preferable to attach event
handlers to the children of a `DocumentFragment`, rather than to the
`DocumentFragment` itself.

Consider the following HTML and JavaScript:
:::

### HTML

::: section-content
::: code-example
[html]{.language-name}

``` {signature="uJr6GnUPUCUNWoTzSM8RJE9yZVY76XSniXQyhjBxK5g=" data-language="html"}
<div id="container">

<template id="template">
  Click me
</template>
```
:::
:::

### JavaScript

::: section-content
::: code-example
[js]{.language-name}

``` {signature="C1NNEZsMKRq3qmZWfEeX0g/WzogXFxvvdfrh4TR57Ng=" data-language="js"}
const container = document.getElementById("container");
const template = document.getElementById("template");

function clickHandler(event) {
  event.target.append(" — Clicked this div");
}

const firstClone = template.content.cloneNode(true);
firstClone.addEventListener("click", clickHandler);
container.appendChild(firstClone);

const secondClone = template.content.cloneNode(true);
secondClone.children[0].addEventListener("click", clickHandler);
container.appendChild(secondClone);
```
:::
:::

### Result

::: section-content
Since `firstClone` is a `DocumentFragment`, only its children are added
to `container` when `appendChild` is called; the event handlers of
`firstClone` are not copied. In contrast, because an event handler is
added to the first *child node* of `secondClone`, the event handler is
copied when `appendChild` is called, and clicking on it works as one
would expect.

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
<td><a href="../content_categories#metadata_content">Metadata
content</a>, <a href="../content_categories#flow_content">flow
content</a>, <a href="../content_categories#phrasing_content">phrasing
content</a>, <a
href="../content_categories#script-supporting_elements">script-supporting
element</a></td>
</tr>
<tr class="even">
<th scope="row">Permitted content</th>
<td>No restrictions</td>
</tr>
<tr class="odd">
<th scope="row">Tag omission</th>
<td>None, both the starting and ending tag are mandatory.</td>
</tr>
<tr class="even">
<th scope="row">Permitted parents</th>
<td>Any element that accepts <a
href="../content_categories#metadata_content">metadata content</a>, <a
href="../content_categories#phrasing_content">phrasing content</a>, or
<a
href="../content_categories#script-supporting_elements">script-supporting
elements</a>. Also allowed as a child of a <a
href="colgroup"><code>&lt;colgroup&gt;</code></a> element that does
<em>not</em> have a <a href="colgroup#span"><code>span</code></a>
attribute.</td>
</tr>
<tr class="odd">
<th scope="row">Implicit ARIA role</th>
<td><a href="https://www.w3.org/TR/html-aria/#dfn-no-corresponding-role"
target="_blank">No corresponding role</a></td>
</tr>
<tr class="even">
<th scope="row">Permitted ARIA roles</th>
<td>No <code>role</code> permitted</td>
</tr>
<tr class="odd">
<th scope="row">DOM interface</th>
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLTemplateElement"><code>HTMLTemplateElement</code></a></td>
</tr>
</tbody>
</table>

</figure>
:::

## Specifications

::: _table
  ------------------------------------------------------------------------------------------------------------
  Specification
  ------------------------------------------------------------------------------------------------------------
  [HTML Standard\
  [\#
  the-template-element]{.small}](https://html.spec.whatwg.org/multipage/scripting.html#the-template-element)

  ------------------------------------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
                     Desktop                                                                     Mobile                                                                                   
  ------------------ ------------ ------------ --------- ------------------- ---------- -------- ----------------- ---------------- --------------------- --------------- --------------- ------------------
                     Chrome       Edge         Firefox   Internet Explorer   Opera      Safari   WebView Android   Chrome Android   Firefox for Android   Opera Android   Safari on IOS   Samsung Internet
  `template`         26           13           22        No                  15         8        Yes               26               22                    14              8               1.5
  `shadowrootmode`   11190--111   11190--111   No        No                  9776--97   16.4     11190--111        11190--111       No                    64              16.4            22.015.0--22.0
:::

## See also {#see_also}

::: section-content
-   Web components: [`<slot>`](slot) (and historical: `<shadow>`)
-   [Using templates and
    slots](https://developer.mozilla.org/en-US/docs/Web/API/Web_components/Using_templates_and_slots)
-   [CSS
    scoping](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_scoping)
    module
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Element/template](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/template){._attribution-link}
:::
