

# \<b\>: The Bring Attention To element



::: section-content
The `<b>` [HTML](../index) element is used to draw the reader\'s
attention to the element\'s contents, which are not otherwise granted
special importance. This was formerly known as the Boldface element, and
most browsers still draw the text in boldface. However, you should not
use `<b>` for styling text or granting importance. If you wish to create
boldface text, you should use the CSS
[`font-weight`](https://developer.mozilla.org/en-US/docs/Web/CSS/font-weight)
property. If you wish to indicate an element is of special importance,
you should use the [`<strong>`](strong) element.
:::

## Try it {#try_it}

::: section-content
::: iframe
::: {.output-header .border-rounded-top}
#### HTML Demo: \<b\> {#html-demo-b .output-heading}

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
      The two most popular science courses offered by the school are <b class="term">chemistry</b> (the study of chemicals
      and the composition of substances) and <b class="term">physics</b> (the study of the nature and properties of matter
      and energy).
    </p>
:::
:::

::: {#css-panel .section .hidden tabindex="0" role="tabpanel" aria-labelledby="css" aria-hidden="true"}
::: {#css-editor}
    /* stylelint-disable-next-line block-no-empty */
    b {
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
This element only includes the [global
attributes](../global_attributes).
:::

## Usage notes {#usage_notes}

::: section-content
-   Use the `<b>` for cases like keywords in a summary, product names in
    a review, or other spans of text whose typical presentation would be
    boldfaced (but not including any special importance).
-   Do not confuse the `<b>` element with the [`<strong>`](strong),
    [`<em>`](em), or [`<mark>`](mark) elements. The [`<strong>`](strong)
    element represents text of certain *importance*, [`<em>`](em) puts
    some emphasis on the text and the [`<mark>`](mark) element
    represents text of certain *relevance*. The `<b>` element doesn\'t
    convey such special semantic information; use it only when no others
    fit.
-   Similarly, do not mark titles and headings using the `<b>` element.
    For this purpose, use the [h1](heading_elements) to
    [h6](heading_elements) tags. Further, stylesheets can change the
    default style of these elements, with the result that they are not
    *necessarily* displayed in bold.
-   It is a good practice to use the
    [`class`](../global_attributes#class) attribute on the `<b>` element
    in order to convey additional semantic information as needed (for
    example `<b class="lead">` for the first sentence in a paragraph).
    This makes it easier to manage multiple use cases of `<b>` if your
    stylistic needs change, without the need to change all of its uses
    in the HTML.
-   Historically, the `<b>` element was meant to make text boldface.
    Styling information has been deprecated since HTML4, so the meaning
    of the `<b>` element has been changed.
-   If there is no semantic purpose to using the `<b>` element, you
    should use the CSS
    [`font-weight`](https://developer.mozilla.org/en-US/docs/Web/CSS/font-weight)
    property with the value `"bold"` instead in order to make text bold.
:::

## Examples

::: section-content
::: code-example
[html]{.language-name}

``` {signature="yCJGzgyS/vr9uydADE4SK+H5aQvykvC6oY0I4y2uKko=" data-language="html"}
<p>
  This article describes several <b class="keywords">text-level</b> elements. It
  explains their usage in an <b class="keywords">HTML</b> document.
</p>
Keywords are displayed with the default style of the
<b>element, likely in bold.</b>
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
  the-b-element]{.small}](https://html.spec.whatwg.org/multipage/text-level-semantics.html#the-b-element)

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

  `b`   1         12     1                   Yes        15      1        4.4       18        4         14        1        1.0
                                                                                                                          
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
-   Other elements conveying text-level semantics: [`<a>`](a),
    [`<em>`](em), [`<strong>`](strong), [`<small>`](small),
    [`<cite>`](cite), [`<q>`](q), [`<dfn>`](dfn), [`<abbr>`](abbr),
    [`<time>`](time), [`<code>`](code), [`<var>`](var),
    [`<samp>`](samp), [`<kbd>`](kbd), [`<sub>`](sub), [`<sup>`](sup),
    [`<i>`](i), [`<mark>`](mark), [`<ruby>`](ruby), [`<rp>`](rp),
    [`<rt>`](rt), [`<bdo>`](bdo), [`<span>`](span), [`<br>`](br),
    [`<wbr>`](wbr).
-   [Using \<b\> and \<i\> elements
    (W3C)](https://www.w3.org/International/questions/qa-b-and-i-tags){target="_blank"}
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Element/b](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/b){._attribution-link}
:::
