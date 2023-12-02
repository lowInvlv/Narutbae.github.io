

# \<br\>: The Line Break element



::: section-content
The `<br>` [HTML](../index) element produces a line break in text
(carriage-return). It is useful for writing a poem or an address, where
the division of lines is significant.
:::

## Try it {#try_it}

::: section-content
::: iframe
::: {.output-header .border-rounded-top}
#### HTML Demo: \<br\> {#html-demo-br .output-heading}

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
    <p>
      O’er all the hilltops<br />
      Is quiet now,<br />
      In all the treetops<br />
      Hearest thou<br />
      Hardly a breath;<br />
      The birds are asleep in the trees:<br />
      Wait, soon like these<br />
      Thou too shalt rest.
    </p>
:::
:::

::: {#css-panel .section .hidden tabindex="0" role="tabpanel" aria-labelledby="css" aria-hidden="true"}
::: {#css-editor}
    p {
      font-size: 1rem;
      font-family: sans-serif;
      margin: 20px;
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

As you can see from the above example, a `<br>` element is included at
each point where we want the text to break. The text after the `<br>`
begins again at the start of the next line of the text block.

::: {#sect1 .notecard .note}
**Note:** Do not use `<br>` to create margins between paragraphs; wrap
them in [`<p>`](p) elements and use the
[CSS](https://developer.mozilla.org/en-US/docs/Web/CSS)
[`margin`](https://developer.mozilla.org/en-US/docs/Web/CSS/margin)
property to control their size.
:::
:::

## Attributes

::: section-content
This element\'s attributes include the [global
attributes](../global_attributes).
:::

### Deprecated attributes {#deprecated_attributes}

::: section-content

[`clear`](#clear) [Deprecated]{.visually-hidden}

:   Indicates where to begin the next line after the break.
:::

## Styling with CSS {#styling_with_css}

::: section-content
The `<br>` element has a single, well-defined purpose --- to create a
line break in a block of text. As such, it has no dimensions or visual
output of its own, and there is very little you can do to style it.

You can set a
[`margin`](https://developer.mozilla.org/en-US/docs/Web/CSS/margin) on
`<br>` elements themselves to increase the spacing between the lines of
text in the block, but this is a bad practice --- you should use the
[`line-height`](https://developer.mozilla.org/en-US/docs/Web/CSS/line-height)
property that was designed for that purpose.
:::

## Examples

### Simple br {#simple_br}

::: section-content
In the following example we use `<br>` elements to create line breaks
between the different lines of a postal address:

::: code-example
[html]{.language-name}

``` {signature="1OurpK+QdBD1DLJH1DTGuzsqsxsxAaITfhCr2n3azkA=" data-language="html"}
Mozilla<br />
331 E. Evelyn Avenue<br />
Mountain View, CA<br />
94041<br />
USA<br />
```
:::

#### Result

::: {#sect2 .code-example}
::: iframe
:::
:::
:::

## Accessibility concerns {#accessibility_concerns}

::: section-content
Creating separate paragraphs of text using `<br>` is not only bad
practice, it is problematic for people who navigate with the aid of
screen reading technology. Screen readers may announce the presence of
the element, but not any content contained within `<br>`s. This can be a
confusing and frustrating experience for the person using the screen
reader.

Use `<p>` elements, and use CSS properties like
[`margin`](https://developer.mozilla.org/en-US/docs/Web/CSS/margin) to
control their spacing.
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
href="../content_categories#phrasing_content">phrasing content</a>.</td>
</tr>
<tr class="even">
<th scope="row">Permitted content</th>
<td>None; it is a <a
href="https://developer.mozilla.org/en-US/docs/Glossary/Void_element">void
element</a>.</td>
</tr>
<tr class="odd">
<th scope="row">Tag omission</th>
<td>Must have a start tag, and must not have an end tag. In XHTML
documents, write this element as <code>&lt;br /&gt;</code>.</td>
</tr>
<tr class="even">
<th scope="row">Permitted parents</th>
<td>Any element that accepts <a
href="../content_categories#phrasing_content">phrasing content</a>.</td>
</tr>
<tr class="odd">
<th scope="row">Implicit ARIA role</th>
<td><a href="https://www.w3.org/TR/html-aria/#dfn-no-corresponding-role"
target="_blank">No corresponding role</a></td>
</tr>
<tr class="even">
<th scope="row">Permitted ARIA roles</th>
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/none_role"><code>none</code></a>,
<a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/presentation_role"><code>presentation</code></a></td>
</tr>
<tr class="odd">
<th scope="row">DOM interface</th>
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLBRElement"><code>HTMLBRElement</code></a></td>
</tr>
</tbody>
</table>

</figure>
:::

## Specifications

::: _table
  -----------------------------------------------------------------------------------------------------------
  Specification
  -----------------------------------------------------------------------------------------------------------
  [HTML Standard\
  [\#
  the-br-element]{.small}](https://html.spec.whatwg.org/multipage/text-level-semantics.html#the-br-element)

  -----------------------------------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
            Desktop                                                         Mobile                                                                                   
  --------- --------- ------ --------- ------------------- ------- -------- ----------------- ---------------- --------------------- --------------- --------------- ------------------
            Chrome    Edge   Firefox   Internet Explorer   Opera   Safari   WebView Android   Chrome Android   Firefox for Android   Opera Android   Safari on IOS   Samsung Internet
  `br`      1         12     1         Yes                 15      ≤4       4.4               18               4                     14              ≤3.2            1.0
  `clear`   1         12     1         Yes                 15      ≤4       4.4               18               4                     14              ≤3.2            1.0
:::

## See also {#see_also}

::: section-content
-   [`<address>`](address) element
-   [`<p>`](p) element
-   [`<wbr>`](wbr) element
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Element/br](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/br){._attribution-link}
:::
