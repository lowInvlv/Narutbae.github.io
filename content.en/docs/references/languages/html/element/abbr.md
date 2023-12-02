

# \<abbr\>: The Abbreviation element



::: section-content
The `<abbr>` [HTML](../index) element represents an abbreviation or
acronym.

When including an abbreviation or acronym, provide a full expansion of
the term in plain text on first use, along with the `<abbr>` to mark up
the abbreviation. This informs the user what the abbreviation or acronym
means.

The optional [`title`](../global_attributes#title) attribute can provide
an expansion for the abbreviation or acronym when a full expansion is
not present. This provides a hint to user agents on how to
announce/display the content while informing all users what the
abbreviation means. If present, `title` must contain this full
description and nothing else.
:::

## Try it {#try_it}

::: section-content
::: iframe
::: {.output-header .border-rounded-top}
#### HTML Demo: \<abbr\> {#html-demo-abbr .output-heading}

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
    <p>
      You can use <abbr>CSS</abbr> (Cascading Style Sheets) to style your <abbr>HTML</abbr> (HyperText Markup Language).
      Using style sheets, you can keep your <abbr>CSS</abbr> presentation layer and <abbr>HTML</abbr> content layer
      separate. This is called "separation of concerns."
    </p>
:::
:::

::: {#css-panel .section .hidden tabindex="0" role="tabpanel" aria-labelledby="css" aria-hidden="true"}
::: {#css-editor}
    abbr {
      font-style: italic;
      color: chocolate;
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
This element only supports the [global
attributes](../global_attributes). The
[`title`](../global_attributes#title) attribute has a specific semantic
meaning when used with the `<abbr>` element; it *must* contain a full
human-readable description or expansion of the abbreviation. This text
is often presented by browsers as a tooltip when the mouse cursor is
hovered over the element.

Each `<abbr>` element you use is independent of all others; providing a
`title` for one does not automatically attach the same expansion text to
others with the same content text.
:::

## Usage notes {#usage_notes}

### Typical use cases {#typical_use_cases}

::: section-content
It\'s certainly not required that all abbreviations be marked up using
`<abbr>`. There are, though, a few cases where it\'s helpful to do so:

-   When an abbreviation is used and you want to provide an expansion or
    definition outside the flow of the document\'s content, use `<abbr>`
    with an appropriate [`title`](../global_attributes#title).
-   To define an abbreviation which may be unfamiliar to the reader,
    present the term using `<abbr>` and inline text providing the
    definition. Include a `title` attribute only when the inline
    expansion or definition is not available.
-   When an abbreviation\'s presence in the text needs to be
    semantically noted, the `<abbr>` element is useful. This can be
    used, in turn, for styling or scripting purposes.
-   You can use `<abbr>` in concert with [`<dfn>`](dfn) to establish
    definitions for terms which are abbreviations or acronyms. See the
    example [Defining an abbreviation](#defining_an_abbreviation) below.
:::

### Grammar considerations {#grammar_considerations}

::: section-content
In languages with [grammatical
number](https://en.wikipedia.org/wiki/Grammatical_number){target="_blank"}
(that is, languages where the number of items affects the grammar of a
sentence), use the same grammatical number in your `title` attribute as
inside your `<abbr>` element. This is especially important in languages
with more than two numbers, such as Arabic, but is also relevant in
English.
:::

## Default styling {#default_styling}

::: section-content
The purpose of this element is purely for the convenience of the author
and all browsers display it inline
([`display`](https://developer.mozilla.org/en-US/docs/Web/CSS/display)`: inline`)
by default, though its default styling varies from one browser to
another:

Some browsers add a dotted underline to the content of the element.
Others add a dotted underline while converting the contents to small
caps. Others may not style it differently than a [`<span>`](span)
element. To control this styling, use
[`text-decoration`](https://developer.mozilla.org/en-US/docs/Web/CSS/text-decoration)
and
[`font-variant`](https://developer.mozilla.org/en-US/docs/Web/CSS/font-variant).
:::

## Examples

### Marking up an abbreviation semantically {#marking_up_an_abbreviation_semantically}

::: section-content
To mark up an abbreviation without providing an expansion or
description, use `<abbr>` without any attributes, as seen in this
example.

#### HTML

::: code-example
[html]{.language-name}

``` {signature="BuRjbvvFo9xCc1rYmeTHk8owTBH+XTb20JibP3th01U=" data-language="html"}
<p>Using <abbr>HTML</abbr> is fun and easy!</p>
```
:::

#### Result

::: {#sect1 .code-example}
::: iframe
:::
:::
:::

### Styling abbreviations {#styling_abbreviations}

::: section-content
You can use CSS to set a custom style to be used for abbreviations, as
seen in this simple example.

#### HTML {#html_2}

::: code-example
[html]{.language-name}

``` {signature="fOL8fradlYXqM3/G0fmRsKhB98FehxQRao36MN2nuF0=" data-language="html"}
<p>Using <abbr>CSS</abbr>, you can style your abbreviations!</p>
```
:::

#### CSS

::: code-example
[css]{.language-name}

``` {signature="+OjG0mJBckdkkJYLL4gazovCHMkytzzVCr9aZk7YLyc=" data-language="css"}
abbr {
  font-variant: all-small-caps;
}
```
:::

#### Result {#result_2}

::: {#sect2 .code-example}
::: iframe
:::
:::
:::

### Providing an expansion {#providing_an_expansion}

::: section-content
Adding a [`title`](../global_attributes#title) attribute lets you
provide an expansion or definition for the abbreviation or acronym.

#### HTML {#html_3}

::: code-example
[html]{.language-name}

``` {signature="YCByAVLqtCO50Ol1lLCo9PG3Jg5KVWP2bLsd1G7f7b0=" data-language="html"}
<p>Ashok's joke made me <abbr title="Laugh Out Loud">LOL</abbr> big time.</p>
```
:::

#### Result {#result_3}

::: {#sect3 .code-example}
::: iframe
:::
:::
:::

### Defining an abbreviation {#defining_an_abbreviation}

::: section-content
You can use `<abbr>` in tandem with [`<dfn>`](dfn) to more formally
define an abbreviation, as shown here.

#### HTML {#html_4}

::: code-example
[html]{.language-name}

``` {signature="whhZ8zMjla7A/XZ3kYMZDhYTy87eZ2lcNAJHMYelWiQ=" data-language="html"}
<p>
  <dfn id="html"><abbr title="HyperText Markup Language">HTML</abbr> </dfn> is a
  markup language used to create the semantics and structure of a web page.
</p>

<p>
  A <dfn id="spec">Specification</dfn> (<abbr>spec</abbr>) is a document that
  outlines in detail how a technology or API is intended to function and how it
  is accessed.
</p>
```
:::

#### Result {#result_4}

::: {#sect4 .code-example}
::: iframe
:::
:::
:::

### Accessibility concerns {#accessibility_concerns}

::: section-content
Spelling out the acronym or abbreviation in full the first time it is
used on a page is beneficial for helping people understand it,
especially if the content is technical or industry jargon.

Only include a `title` if expanding the abbreviation or acronym in the
text is not possible. Having a difference between the announced word or
phrase and what is displayed on the screen, especially if it\'s
technical jargon the reader may not be familiar with, can be jarring.

#### HTML {#html_5}

::: code-example
[html]{.language-name}

``` {signature="OrwO8NkLLWVv8DcE3Y2at7troO6W6bp8nGEeb0hhG28=" data-language="html"}
<p>
  JavaScript Object Notation (<abbr>JSON</abbr>) is a lightweight
  data-interchange format.
</p>
```
:::

#### Result {#result_5}

::: {#sect5 .code-example}
::: iframe
:::
:::

This is especially helpful for people who are unfamiliar with the
terminology or concepts discussed in the content, people who are new to
the language, and people with cognitive concerns.
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
href="../content_categories#phrasing_content">phrasing content</a>,
palpable content</td>
</tr>
<tr class="even">
<th scope="row">Permitted content</th>
<td><a href="../content_categories#phrasing_content">Phrasing
content</a></td>
</tr>
<tr class="odd">
<th scope="row">Tag omission</th>
<td>None, both the starting and ending tag are mandatory.</td>
</tr>
<tr class="even">
<th scope="row">Permitted parents</th>
<td>Any element that accepts <a
href="../content_categories#phrasing_content">phrasing content</a></td>
</tr>
<tr class="odd">
<th scope="row">Implicit ARIA role</th>
<td><a href="https://www.w3.org/TR/html-aria/#dfn-no-corresponding-role"
target="_blank">No corresponding role</a></td>
</tr>
<tr class="even">
<th scope="row">Permitted ARIA roles</th>
<td>Any</td>
</tr>
<tr class="odd">
<th scope="row">DOM Interface</th>
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
  the-abbr-element]{.small}](https://html.spec.whatwg.org/multipage/text-level-semantics.html#the-abbr-element)

  ---------------------------------------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
  -------------------------------------------------------------------------------------------------------------------------------------
           Desktop                                                          Mobile                                           
  -------- --------- ------ ------------------- ---------- ------- -------- --------- --------- --------- --------- -------- ----------
           Chrome    Edge   Firefox             Internet   Opera   Safari   WebView   Chrome    Firefox   Opera     Safari   Samsung
                                                Explorer                    Android   Android   for       Android   on IOS   Internet
                                                                                                Android                      

  `abbr`   2         12     1                   7          15      4        4.4       18        4         14        3.2      1.0
                                                                                                                             
                            Before Firefox 4,                                                                                
                            this element                                                                                     
                            implemented the                                                                                  
                            `HTMLSpanElement`                                                                                
                            interface instead                                                                                
                            of the standard                                                                                  
                            `HTMLElement`                                                                                    
                            interface.                                                                                       
  -------------------------------------------------------------------------------------------------------------------------------------
:::

## See also {#see_also}

::: section-content
-   [Using the `<abbr>`
    element](https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/Advanced_text_formatting#abbreviations)
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Element/abbr](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/abbr){._attribution-link}
:::
