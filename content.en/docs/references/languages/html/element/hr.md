

# \<hr\>: The Thematic Break (Horizontal Rule) element



::: section-content
The `<hr>` [HTML](../index) element represents a thematic break between
paragraph-level elements: for example, a change of scene in a story, or
a shift of topic within a section.
:::

## Try it {#try_it}

::: section-content
::: iframe
::: {.output-header .border-rounded-top}
#### HTML Demo: \<hr\> {#html-demo-hr .output-heading}

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
    <p>§1: The first rule of Fight Club is: You do not talk about Fight Club.</p>

    <hr />

    <p>§2: The second rule of Fight Club is: Always bring cupcakes.</p>
:::
:::

::: {#css-panel .section .hidden tabindex="0" role="tabpanel" aria-labelledby="css" aria-hidden="true"}
::: {#css-editor}
    hr {
      border: none;
      border-top: 3px double #333;
      color: #333;
      overflow: visible;
      text-align: center;
      height: 5px;
    }

    hr:after {
      background: #fff;
      content: '§';
      padding: 0 4px;
      position: relative;
      top: -13px;
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

Historically, this has been presented as a horizontal rule or line.
While it may still be displayed as a horizontal rule in visual browsers,
this element is now defined in semantic terms, rather than
presentational terms, so if you wish to draw a horizontal line, you
should do so using appropriate CSS.
:::

## Attributes

::: section-content
This element\'s attributes include the [global
attributes](../global_attributes).

[`align`](#align) [Deprecated]{.visually-hidden} [Non-standard]{.visually-hidden}

:   Sets the alignment of the rule on the page. If no value is
    specified, the default value is `left`.

[`color`](#color) [Deprecated]{.visually-hidden} [Non-standard]{.visually-hidden}

:   Sets the color of the rule through color name or hexadecimal value.

[`noshade`](#noshade) [Deprecated]{.visually-hidden} [Non-standard]{.visually-hidden}

:   Sets the rule to have no shading.

[`size`](#size) [Deprecated]{.visually-hidden} [Non-standard]{.visually-hidden}

:   Sets the height, in pixels, of the rule.

[`width`](#width) [Deprecated]{.visually-hidden} [Non-standard]{.visually-hidden}

:   Sets the length of the rule on the page through a pixel or
    percentage value.
:::

## Example

### HTML

::: section-content
::: code-example
[html]{.language-name}

``` {signature="QpIg03uP5cuR12WLHhTEftwyT8UeZqdaX/D1T/JfcCY=" data-language="html"}
<p>
  This is the first paragraph of text. This is the first paragraph of text. This
  is the first paragraph of text. This is the first paragraph of text.
</p>

<hr />

<p>
  This is the second paragraph of text. This is the second paragraph of text.
  This is the second paragraph of text. This is the second paragraph of text.
</p>
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

## Technical summary {#technical_summary}

::: section-content
<figure class="table-container">
<div class="_table">
<table class="properties">
<tbody>
<tr class="odd">
<th scope="row"><a href="../content_categories">Content
categories</a></th>
<td><a href="../content_categories#flow_content">Flow content</a>.</td>
</tr>
<tr class="even">
<th scope="row">Permitted content</th>
<td>None; it is a <a
href="https://developer.mozilla.org/en-US/docs/Glossary/Void_element">void
element</a>.</td>
</tr>
<tr class="odd">
<th scope="row">Tag omission</th>
<td>It must have start tag, but must not have an end tag.</td>
</tr>
<tr class="even">
<th scope="row">Permitted parents</th>
<td>Any element that accepts <a
href="../content_categories#flow_content">flow content</a>.</td>
</tr>
<tr class="odd">
<th scope="row">Implicit ARIA role</th>
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/separator_role"><code>separator</code></a></td>
</tr>
<tr class="even">
<th scope="row">Permitted ARIA roles</th>
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/presentation_role"><code>presentation</code></a>
or <a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/none_role"><code>none</code></a></td>
</tr>
<tr class="odd">
<th scope="row">DOM interface</th>
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLHRElement"><code>HTMLHRElement</code></a></td>
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
  the-hr-element]{.small}](https://html.spec.whatwg.org/multipage/grouping-content.html#the-hr-element)

  -------------------------------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
              Desktop                                                         Mobile                                                                                   
  ----------- --------- ------ --------- ------------------- ------- -------- ----------------- ---------------- --------------------- --------------- --------------- ------------------
              Chrome    Edge   Firefox   Internet Explorer   Opera   Safari   WebView Android   Chrome Android   Firefox for Android   Opera Android   Safari on IOS   Samsung Internet
  `hr`        1         12     1         5.5                 ≤12.1   3        4.4               18               4                     ≤12.1           1               1.0
  `align`     1         12     1         ≤6                  ≤12.1   ≤4       4.4               18               4                     ≤12.1           ≤3.2            1.0
  `color`     33        12     1         ≤6                  20      10.1     4.4.3             33               4                     20              10.3            2.0
  `noshade`   1         12     1         ≤6                  ≤12.1   ≤4       4.4               18               4                     ≤12.1           ≤3.2            1.0
  `size`      1         12     1         ≤6                  ≤12.1   ≤4       4.4               18               4                     ≤12.1           ≤3.2            1.0
  `width`     1         12     1         ≤6                  ≤12.1   ≤4       4.4               18               4                     ≤12.1           ≤3.2            1.0
:::

## See also {#see_also}

::: section-content
-   [`<p>`](p)
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Element/hr](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/hr){._attribution-link}
:::
