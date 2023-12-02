

# \<dl\>: The Description List element



::: section-content
The `<dl>` [HTML](../index) element represents a description list. The
element encloses a list of groups of terms (specified using the
[`<dt>`](dt) element) and descriptions (provided by [`<dd>`](dd)
elements). Common uses for this element are to implement a glossary or
to display metadata (a list of key-value pairs).
:::

## Try it {#try_it}

::: section-content
::: iframe
::: {.output-header .border-rounded-top}
#### HTML Demo: \<dl\> {#html-demo-dl .output-heading}

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
    <p>Cryptids of Cornwall:</p>

    <dl>
      <dt>Beast of Bodmin</dt>
      <dd>A large feline inhabiting Bodmin Moor.</dd>

      <dt>Morgawr</dt>
      <dd>A sea serpent.</dd>

      <dt>Owlman</dt>
      <dd>A giant owl-like creature.</dd>
    </dl>
:::
:::

::: {#css-panel .section .hidden tabindex="0" role="tabpanel" aria-labelledby="css" aria-hidden="true"}
::: {#css-editor}
    p,
    dt {
      font-weight: bold;
    }

    dl,
    dd {
      font-size: 0.9rem;
    }

    dd {
      margin-bottom: 1em;
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
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<th scope="row"><a href="../content_categories">Content
categories</a></th>
<td><a href="../content_categories#flow_content">Flow content</a>, and
if the <code>&lt;dl&gt;</code> element's children include one name-value
group, palpable content.</td>
</tr>
<tr class="even">
<th scope="row">Permitted content</th>
<td><p>Either: Zero or more groups each consisting of one or more <a
href="dt"><code>&lt;dt&gt;</code></a> elements followed by one or more
<a href="dd"><code>&lt;dd&gt;</code></a> elements, optionally intermixed
with <a href="script"><code>&lt;script&gt;</code></a> and <a
href="template"><code>&lt;template&gt;</code></a> elements.<br />
Or: (in <a
href="https://developer.mozilla.org/en-US/docs/Glossary/WHATWG">WHATWG</a>
HTML, <a
href="https://developer.mozilla.org/en-US/docs/Glossary/W3C">W3C</a>
HTML 5.2 and later) One or more <a
href="div"><code>&lt;div&gt;</code></a> elements, optionally intermixed
with <a href="script"><code>&lt;script&gt;</code></a> and <a
href="template"><code>&lt;template&gt;</code></a> elements.</p></td>
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
<td><a href="https://www.w3.org/TR/html-aria/#dfn-no-corresponding-role"
target="_blank">No corresponding role</a></td>
</tr>
<tr class="even">
<th scope="row">Permitted ARIA roles</th>
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/group_role"><code>group</code></a>,
<a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/list_role"><code>list</code></a>,
<a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/none_role"><code>none</code></a>,
<a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/presentation_role"><code>presentation</code></a></td>
</tr>
<tr class="odd">
<th scope="row">DOM interface</th>
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLDListElement"><code>HTMLDListElement</code></a></td>
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

## Examples

### Single term and description {#single_term_and_description}

::: section-content
::: code-example
[html]{.language-name}

``` {signature="M2KB6BAn11nEoejo3yfJckht/P+TUmFXQBI5qSDOJ30=" data-language="html"}
<dl>
  <dt>Firefox</dt>
  <dd>
    A free, open source, cross-platform, graphical web browser developed by the
    Mozilla Corporation and hundreds of volunteers.
  </dd>

  <!-- Other terms and descriptions -->
</dl>
```
:::

#### Result

::: {#sect1 .code-example}
::: iframe
:::
:::
:::

### Multiple terms, single description {#multiple_terms_single_description}

::: section-content
::: code-example
[html]{.language-name}

``` {signature="r70kadJajGwLcDcHd4FV8dfWdIwl2ddLtbWMVHd1L4M=" data-language="html"}
<dl>
  <dt>Firefox</dt>
  <dt>Mozilla Firefox</dt>
  <dt>Fx</dt>
  <dd>
    A free, open source, cross-platform, graphical web browser developed by the
    Mozilla Corporation and hundreds of volunteers.
  </dd>

  <!-- Other terms and descriptions -->
</dl>
```
:::

#### Result {#result_2}

::: {#sect2 .code-example}
::: iframe
:::
:::
:::

### Single term, multiple descriptions {#single_term_multiple_descriptions}

::: section-content
::: code-example
[html]{.language-name}

``` {signature="2wkvGqjOgJk7dQZOFONstJAg6gD1mzw5/PkNeNkbSPA=" data-language="html"}
<dl>
  <dt>Firefox</dt>
  <dd>
    A free, open source, cross-platform, graphical web browser developed by the
    Mozilla Corporation and hundreds of volunteers.
  </dd>
  <dd>
    The Red Panda also known as the Lesser Panda, Wah, Bear Cat or Firefox, is a
    mostly herbivorous mammal, slightly larger than a domestic cat (60 cm long).
  </dd>

  <!-- Other terms and descriptions -->
</dl>
```
:::

#### Result {#result_3}

::: {#sect3 .code-example}
::: iframe
:::
:::
:::

### Multiple terms and descriptions {#multiple_terms_and_descriptions}

::: section-content
It is also possible to define multiple terms with multiple corresponding
descriptions, by combining the examples above.
:::

### Metadata

::: section-content
Description lists are useful for displaying metadata as a list of
key-value pairs.

::: code-example
[html]{.language-name}

``` {signature="ggC1gFkDvO6JFAhoN3EqxIwXHU9xb2iS+jCZJURc0aI=" data-language="html"}
<dl>
  <dt>Name</dt>
  <dd>Godzilla</dd>
  <dt>Born</dt>
  <dd>1952</dd>
  <dt>Birthplace</dt>
  <dd>Japan</dd>
  <dt>Color</dt>
  <dd>Green</dd>
</dl>
```
:::

#### Result {#result_4}

::: {#sect4 .code-example}
::: iframe
:::
:::

Tip: It can be handy to define a key-value separator in the CSS, such
as:

::: code-example
[css]{.language-name}

``` {signature="+1HiRyGoTWLoL9dc9hWcGgNcU1bY9VCCK8Vw6JPkpBY=" data-language="css"}
dt::after {
  content: ": ";
}
```
:::
:::

### Wrapping name-value groups in `div` elements {#wrapping_name-value_groups_in_div_elements}

::: section-content
[WHATWG](https://developer.mozilla.org/en-US/docs/Glossary/WHATWG) HTML
allows wrapping each name-value group in a
[`<dl>`](dl){aria-current="page"} element in a [``](div) element.
This can be useful when using [microdata](../microdata), or when [global
attributes](../global_attributes) apply to a whole group, or for styling
purposes.

::: code-example
[html]{.language-name}

``` {signature="QCqvOoQtxNieexVFq+A7+T0VrsJ3whs6tVqRt06AeIQ=" data-language="html"}
<dl>
  
    <dt>Name</dt>
    <dd>Godzilla</dd>
  
  
    <dt>Born</dt>
    <dd>1952</dd>
  
  
    <dt>Birthplace</dt>
    <dd>Japan</dd>
  
  
    <dt>Color</dt>
    <dd>Green</dd>
  
</dl>
```
:::

#### Result {#result_5}

::: {#sect5 .code-example}
::: iframe
:::
:::
:::

## Notes

::: section-content
Do not use this element (nor [`<ul>`](ul) elements) to merely create
indentation on a page. Although it works, this is a bad practice and
obscures the meaning of description lists.

To change the indentation of a description term, use the
[CSS](https://developer.mozilla.org/en-US/docs/Web/CSS)
[`margin`](https://developer.mozilla.org/en-US/docs/Web/CSS/margin)
property.
:::

## Accessibility concerns {#accessibility_concerns}

::: section-content
Each screen reader exposes `<dl>` content differently, including total
count, terms/definitions context, and navigation methods. These
differences are not necessarily bugs. As of iOS 14, VoiceOver will
announce that `<dl>` content is a list when navigating with the virtual
cursor (not via the read-all command). VoiceOver does not support list
navigation commands with `<dl>`. Be careful applying ARIA `term` and
`definition` roles to `<dl>` constructs as VoiceOver (macOS and iOS)
will adjust how they are announced.

-   [VoiceOver on iOS 14 Supports Description
    Lists](https://adrianroselli.com/2020/09/voiceover-on-ios-14-supports-description-lists.html){target="_blank"}
-   [Brief Note on Description List
    Support](https://adrianroselli.com/2022/12/brief-note-on-description-list-support.html){target="_blank"}
:::

## Specifications

::: _table
  -------------------------------------------------------------------------------------------------------
  Specification
  -------------------------------------------------------------------------------------------------------
  [HTML Standard\
  [\#
  the-dl-element]{.small}](https://html.spec.whatwg.org/multipage/grouping-content.html#the-dl-element)

  -------------------------------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
         Desktop                                                         Mobile                                                                                   
  ------ --------- ------ --------- ------------------- ------- -------- ----------------- ---------------- --------------------- --------------- --------------- ------------------
         Chrome    Edge   Firefox   Internet Explorer   Opera   Safari   WebView Android   Chrome Android   Firefox for Android   Opera Android   Safari on IOS   Samsung Internet
  `dl`   1         12     1         Yes                 15      ≤4       4.4               18               4                     14              ≤3.2            1.0
:::

## See also {#see_also}

::: section-content
-   [`<dt>`](dt)
-   [`<dd>`](dd)
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Element/dl](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/dl){._attribution-link}
:::
