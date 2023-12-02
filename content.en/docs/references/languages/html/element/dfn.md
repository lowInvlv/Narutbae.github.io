

# \<dfn\>: The Definition element



::: section-content
The `<dfn>` [HTML](../index) element is used to indicate the term being
defined within the context of a definition phrase or sentence. The
ancestor [`<p>`](p) element, the [`<dt>`](dt)/[`<dd>`](dd) pairing, or
the nearest [`<section>`](section) ancestor of the `<dfn>` element, is
considered to be the definition of the term.
:::

## Try it {#try_it}

::: section-content
::: iframe
::: {.output-header .border-rounded-top}
#### HTML Demo: \<dfn\> {#html-demo-dfn .output-heading}

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
    <p>A <dfn id="def-validator">validator</dfn> is a program that checks for syntax errors in code or documents.</p>
:::
:::

::: {#css-panel .section .hidden tabindex="0" role="tabpanel" aria-labelledby="css" aria-hidden="true"}
::: {#css-editor}
    /* stylelint-disable-next-line block-no-empty */
    dfn {
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
This element\'s attributes include the [global
attributes](../global_attributes).

The [`title`](../global_attributes#title) attribute has special meaning,
as noted below.
:::

## Usage notes {#usage_notes}

::: section-content
There are some not-entirely-obvious aspects to using the `<dfn>`
element. We examine those here.
:::

### Specifying the term being defined {#specifying_the_term_being_defined}

::: section-content
The term being defined is identified following these rules:

1.  If the `<dfn>` element has a [`title`](../global_attributes#title)
    attribute, the value of the `title` attribute is considered to be
    the term being defined. The element must still have text within it,
    but that text may be an abbreviation (perhaps using
    [`<abbr>`](abbr)) or another form of the term.
2.  If the `<dfn>` contains a single child element and does not have any
    text content of its own, and the child element is an
    [`<abbr>`](abbr) element with a `title` attribute itself, then the
    exact value of the `<abbr>` element\'s `title` is the term being
    defined.
3.  Otherwise, the text content of the `<dfn>` element is the term being
    defined. This is shown [in the first example
    below](#basic_identification_of_a_term).

::: {#sect1 .notecard .note}
**Note:** If the `<dfn>` element has a `title` attribute, it *must*
contain the term being defined and no other text.
:::
:::

### Links to `<dfn>` elements {#links_to_dfn_elements}

::: section-content
If you include an [`id`](../global_attributes#id) attribute on the
`<dfn>` element, you can then link to it using [`<a>`](a) elements. Such
links should be uses of the term, with the intent being that the reader
can quickly navigate to the term\'s definition if they\'re not already
aware of it, by clicking on the term\'s link.

This is shown in the example under [Links to
definitions](#links_to_definitions) below.
:::

## Examples

::: section-content
Let\'s take a look at some examples of various usage scenarios.
:::

### Basic identification of a term {#basic_identification_of_a_term}

::: section-content
This example uses a plain `<dfn>` element to identify the location of a
term within the definition.

#### HTML

::: code-example
[html]{.language-name}

``` {signature="K4NxBjt6e2dzQ1k7aPedW121cwVKhGatkmwT5kJ1k5U=" data-language="html"}
<p>
  The <strong>HTML Definition element (<dfn>&lt;dfn&gt;</dfn>)</strong> is used
  to indicate the term being defined within the context of a definition phrase
  or sentence.
</p>
```
:::

Since the `<dfn>` element has no `title`, the text contents of the
`<dfn>` element itself are used as the term being defined.

#### Result

::: {#sect2 .code-example}
::: iframe
:::
:::
:::

### Links to definitions {#links_to_definitions}

::: section-content
To add links to the definitions, you create the link the same way you
always do, with the [`<a>`](a) element.

#### HTML {#html_2}

::: code-example
[html]{.language-name}

``` {signature="jeNTroJjW25Gty0mZNFaezHdnNqxlaNXSuMQGzMU5bk=" data-language="html"}
<p>
  The
  <strong>HTML Definition element (<dfn id="definition-dfn">&lt;dfn&gt;</dfn>)</strong>
  is used to indicate the term being defined within the context of a definition
  phrase or sentence.
</p>

<p>
  Lorem ipsum dolor sit amet, consectetur adipiscing elit. Graece donan, Latine
  voluptatem vocant. Confecta res esset. Duo Reges: constructio interrete.
  Scrupulum, inquam, abeunti;
</p>

<p>
  Because of all of that, we decided to use the
  <code><a href="#definition-dfn">&lt;dfn&gt;</a></code> element for this
  project.
</p>
```
:::

Here we see the definition --- now with an
[`id`](../global_attributes#id) attribute, `"definition-dfn"`, which can
be used as the target of a link. Later on, a link is created using `<a>`
with the [`href`](a#href) attribute set to `"#definition-dfn"` to set up
the link back to the definition.

#### Result {#result_2}

::: {#sect3 .code-example}
::: iframe
:::
:::
:::

### Using abbreviations and definitions together {#using_abbreviations_and_definitions_together}

::: section-content
In some cases, you may wish to use an abbreviation for a term when
defining it. This can be done by using the `<dfn>` and [`<abbr>`](abbr)
elements in tandem, like this:

#### HTML {#html_3}

::: code-example
[html]{.language-name}

``` {signature="6wOpykyE3hb3xiwbCslf2EsqSo6hdG/eJXvTCxdElXw=" data-language="html"}
<p>
  The <dfn><abbr title="Hubble Space Telescope">HST</abbr></dfn> is among the
  most productive scientific instruments ever constructed. It has been in orbit
  for over 20 years, scanning the sky and returning data and photographs of
  unprecedented quality and detail.
</p>

<p>
  Indeed, the <abbr title="Hubble Space Telescope">HST</abbr> has arguably done
  more to advance science than any device ever built.
</p>
```
:::

Note the `<abbr>` element nested inside the `<dfn>`. The former
establishes that the term is an abbreviation (\"HST\") and specifies the
full term (\"Hubble Space Telescope\") in its `title` attribute. The
latter indicates that the abbreviated term represents a term being
defined.

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
href="../content_categories#phrasing_content">phrasing content</a>,
palpable content.</td>
</tr>
<tr class="even">
<th scope="row">Permitted content</th>
<td><a href="../content_categories#phrasing_content">Phrasing
content</a>, but no <a href="dfn"
aria-current="page"><code>&lt;dfn&gt;</code></a> element must be a
descendant.</td>
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
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/term_role"><code>term</code></a></td>
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
  -------------------------------------------------------------------------------------------------------------
  Specification
  -------------------------------------------------------------------------------------------------------------
  [HTML Standard\
  [\#
  the-dfn-element]{.small}](https://html.spec.whatwg.org/multipage/text-level-semantics.html#the-dfn-element)

  -------------------------------------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
          Desktop                                                         Mobile                                                                                   
  ------- --------- ------ --------- ------------------- ------- -------- ----------------- ---------------- --------------------- --------------- --------------- ------------------
          Chrome    Edge   Firefox   Internet Explorer   Opera   Safari   WebView Android   Chrome Android   Firefox for Android   Opera Android   Safari on IOS   Samsung Internet
  `dfn`   15        12     1         Yes                 15      6        4.4               18               4                     14              6               1.0
:::

## See also {#see_also}

::: section-content
-   Elements related to definition lists: [`<dl>`](dl), [`<dt>`](dt),
    [`<dd>`](dd)
-   [`<abbr>`](abbr)
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Element/dfn](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/dfn){._attribution-link}
:::
