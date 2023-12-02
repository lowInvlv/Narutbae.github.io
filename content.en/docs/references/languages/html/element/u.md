

# \<u\>: The Unarticulated Annotation (Underline) element



::: section-content
The `<u>` [HTML](../index) element represents a span of inline text
which should be rendered in a way that indicates that it has a
non-textual annotation. This is rendered by default as a simple solid
underline, but may be altered using CSS.

::: {#sect1 .notecard .warning}
**Warning:** This element used to be called the \"Underline\" element in
older versions of HTML, and is still sometimes misused in this way. To
underline text, you should instead apply a style that includes the CSS
[`text-decoration`](https://developer.mozilla.org/en-US/docs/Web/CSS/text-decoration)
property set to `underline`.
:::
:::

## Try it {#try_it}

::: section-content
::: iframe
::: {.output-header .border-rounded-top}
#### HTML Demo: \<u\> {#html-demo-u .output-heading}

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
    <p>You could use this element to highlight <u>speling</u> mistakes, so the writer can <u>corect</u> them.</p>
:::
:::

::: {#css-panel .section .hidden tabindex="0" role="tabpanel" aria-labelledby="css" aria-hidden="true"}
::: {#css-editor}
    p {
      margin: 0;
    }

    u {
      text-decoration: #f00 wavy underline;
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

See the [Usage notes](#usage_notes) section for further details on when
it\'s appropriate to use `<u>` and when it isn\'t.
:::

## Attributes

::: section-content
This element only includes the [global
attributes](../global_attributes).
:::

## Usage notes {#usage_notes}

::: section-content
Along with other pure styling elements, the original HTML Underline
(`<u>`) element was deprecated in HTML 4; however, `<u>` was restored in
HTML 5 with a new, semantic, meaning: to mark text as having some form
of non-textual annotation applied.

::: {#sect2 .notecard .note}
**Note:** Avoid using the `<u>` element with its default styling (of
underlined text) in such a way as to be confused with a hyperlink, which
is also underlined by default.
:::
:::

### Use cases {#use_cases}

::: section-content
Valid use cases for the `<u>` element include annotating spelling
errors, applying a [proper name
mark](https://en.wikipedia.org/wiki/Proper_name_mark){target="_blank"}
to denote proper names in Chinese text, and other forms of annotation.

You should *not* use `<u>` to underline text for presentation purposes,
or to denote titles of books.
:::

### Other elements to consider using {#other_elements_to_consider_using}

::: section-content
In most cases, you should use an element other than `<u>`, such as:

-   [`<em>`](em) to denote stress emphasis
-   [`<b>`](b) to draw attention to text
-   [`<mark>`](mark) to mark key words or phrases
-   [`<strong>`](strong) to indicate that text has strong importance
-   [`<cite>`](cite) to mark the titles of books or other publications
-   [`<i>`](i) to denote technical terms, transliterations, thoughts, or
    names of vessels in Western texts

To provide textual annotations (as opposed to the non-textual
annotations created with `<u>`), use the [`<ruby>`](ruby) element.

To apply an underlined appearance without any semantic meaning, use the
[`text-decoration`](https://developer.mozilla.org/en-US/docs/Web/CSS/text-decoration)
property\'s value `underline`.
:::

## Examples

### Indicating a spelling error {#indicating_a_spelling_error}

::: section-content
This example uses the `<u>` element and some CSS to display a paragraph
which includes a misspelled error, with the error indicated in the red
wavy underline style which is fairly commonly used for this purpose.

#### HTML

::: code-example
[html]{.language-name}

``` {signature="JYfqiR5W3qppbN5ulAJs3FVGHbMT9jxksTSiMceyVEE=" data-language="html"}
<p>This paragraph includes a <u class="spelling">wrnogly</u> spelled word.</p>
```
:::

In the HTML, we see the use of `<u>` with a class, `spelling`, which is
used to indicate the misspelling of the word \"wrongly\".

#### CSS

::: code-example
[css]{.language-name}

``` {signature="dKcteSUJM1HU1FcZqhqAJkYjKSuMX+gr9Jt3bHTSWHI=" data-language="css"}
u.spelling {
  text-decoration: red wavy underline;
}
```
:::

This CSS indicates that when the `<u>` element is styled with the class
`spelling`, it should have a red wavy underline underneath its text.
This is a common styling for spelling errors. Another common style can
be presented using `red dashed underline`.

#### Result

The result should be familiar to anyone who has used any of the more
popular word processors available today.

::: {#sect3 .code-example}
::: iframe
:::
:::
:::

### Avoiding \<u\> {#avoiding_u}

::: section-content
Most of the time, you actually don\'t want to use `<u>`. Here are some
examples that show what you should do instead in several cases.

#### Non-semantic underlines {#non-semantic_underlines}

To underline text without implying any semantic meaning, use a
[`<span>`](span) element with the
[`text-decoration`](https://developer.mozilla.org/en-US/docs/Web/CSS/text-decoration)
property set to `"underline"`, as shown below.

##### HTML {#html_2}

::: code-example
[html]{.language-name}

``` {signature="9XcB15mQ8LktEFzDTS/pHleaGVi1POMKlUzF95qnK38=" data-language="html"}
<span class="underline">Today's Special</span>
<br />
Chicken Noodle Soup With Carrots
```
:::

##### CSS {#css_2}

::: code-example
[css]{.language-name}

``` {signature="lhjHvumCvagO0Wocf88gqstu9IJJa8ICORUDDKkqpbs=" data-language="css"}
.underline {
  text-decoration: underline;
}
```
:::

##### Result {#result_2}

::: {#sect4 .code-example}
::: iframe
:::
:::

#### Presenting a book title {#presenting_a_book_title}

Book titles should be presented using the [`<cite>`](cite) element
instead of `<u>` or even `<i>`.

##### Using the cite element {#using_the_cite_element}

::: code-example
[html]{.language-name}

``` {signature="IvAbWaSpyzx2PfuOIlRUZE586Uu0qCCEghIgmYP9un4=" data-language="html"}
<p>The class read <cite>Moby Dick</cite> in the first term.</p>
```
:::

::: {#sect5 .code-example}
::: iframe
:::
:::

##### Styling the cite element {#styling_the_cite_element}

The default styling for the `<cite>` element renders the text in
italics. You can override that using CSS:

::: code-example
[html]{.language-name}

``` {signature="IvAbWaSpyzx2PfuOIlRUZE586Uu0qCCEghIgmYP9un4=" data-language="html"}
<p>The class read <cite>Moby Dick</cite> in the first term.</p>
```
:::

::: code-example
[css]{.language-name}

``` {signature="KOazMaZHLmsqODOwqfdrIpKB0RsMGpSDYiXqA8AAy3Q=" data-language="css"}
cite {
  font-style: normal;
  text-decoration: underline;
}
```
:::

::: {#sect6 .code-example}
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
href="../content_categories#phrasing_content">phrasing content</a>,
palpable content.</td>
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
href="../content_categories#phrasing_content">phrasing content</a>.</td>
</tr>
<tr class="odd">
<th scope="row">Implicit ARIA role</th>
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/generic_role"><code>generic</code></a></td>
</tr>
<tr class="even">
<th scope="row">Permitted ARIA roles</th>
<td>Any</td>
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
  the-u-element]{.small}](https://html.spec.whatwg.org/multipage/text-level-semantics.html#the-u-element)

  ---------------------------------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
  ----------------------------------------------------------------------------------------------------------------------------------
        Desktop                                                          Mobile                                           
  ----- --------- ------ ------------------- ---------- ------- -------- --------- --------- --------- --------- -------- ----------
        Chrome    Edge   Firefox             Internet   Opera   Safari   WebView   Chrome    Firefox   Opera     Safari   Samsung
                                             Explorer                    Android   Android   for       Android   on IOS   Internet
                                                                                             Android                      

  `u`   1         12     1                   Yes        15      ≤4       4.4       18        4         14        ≤3.2     1.0
                                                                                                                          
                         Before Firefox 4,                                                                                
                         this element                                                                                     
                         implemented the                                                                                  
                         `HTMLSpanElement`                                                                                
                         interface instead                                                                                
                         of the standard                                                                                  
                         `HTMLElement`                                                                                    
                         interface.                                                                                       
  ----------------------------------------------------------------------------------------------------------------------------------
:::

## See also {#see_also}

::: section-content
-   The [`<span>`](span), [`<i>`](i), [`<em>`](em), [`<b>`](b), and
    [`<cite>`](cite) elements should usually be used instead.
-   The CSS
    [`text-decoration`](https://developer.mozilla.org/en-US/docs/Web/CSS/text-decoration)
    property should be used for non-semantic underlining.
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Element/u](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/u){._attribution-link}
:::
