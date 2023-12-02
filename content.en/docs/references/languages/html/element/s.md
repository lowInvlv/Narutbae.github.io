

# \<s\>: The Strikethrough element



::: section-content
The `<s>` [HTML](../index) element renders text with a strikethrough, or
a line through it. Use the `<s>` element to represent things that are no
longer relevant or no longer accurate. However, `<s>` is not appropriate
when indicating document edits; for that, use the [`<del>`](del) and
[`<ins>`](ins) elements, as appropriate.
:::

## Try it {#try_it}

::: section-content
::: iframe
::: {.output-header .border-rounded-top}
#### HTML Demo: \<s\> {#html-demo-s .output-heading}

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
    <p><s>There will be a few tickets available at the box office tonight.</s></p>

    <p>SOLD OUT!</p>
:::
:::

::: {#css-panel .section .hidden tabindex="0" role="tabpanel" aria-labelledby="css" aria-hidden="true"}
::: {#css-editor}
    /* stylelint-disable-next-line block-no-empty */
    s {
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
<tbody>
<tr class="odd">
<th scope="row"><a href="../content_categories">Content
categories</a></th>
<td><a href="../content_categories#phrasing_content">Phrasing
content</a>, <a href="../content_categories#flow_content">flow
content</a>.</td>
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
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/structural_roles#structural_roles_with_html_equivalents"><code>deletion</code></a></td>
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

## Attributes

::: section-content
This element only includes the [global
attributes](../global_attributes).
:::

## Examples

::: section-content
::: code-example
[css]{.language-name}

``` {signature="WpxZxZhQia1LnwY5tEUb7e9d65NVrd8svAw4TMawKMU=" data-language="css"}
.sold-out {
  text-decoration: line-through;
}
```
:::

::: code-example
[html]{.language-name}

``` {signature="n6IwfJsmaEombS6bOmQjxI7kPJLh0ugOWJYr24/9NIk=" data-language="html"}
<s>Today's Special: Salmon</s> SOLD OUT<br />
<span class="sold-out">Today's Special: Salmon</span> SOLD OUT
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

## Accessibility concerns {#accessibility_concerns}

::: section-content
The presence of the `s` element is not announced by most screen reading
technology in its default configuration. It can be made to be announced
by using the CSS
[`content`](https://developer.mozilla.org/en-US/docs/Web/CSS/content)
property, along with the
[`::before`](https://developer.mozilla.org/en-US/docs/Web/CSS/::before)
and
[`::after`](https://developer.mozilla.org/en-US/docs/Web/CSS/::after)
pseudo-elements.

::: code-example
[css]{.language-name}

``` {signature="QHvZ4Z2AJBrl0NhVvYGBcqPmY56YvwoC5NXuIQG2Z3U=" data-language="css"}
s::before,
s::after {
  clip-path: inset(100%);
  clip: rect(1px, 1px, 1px, 1px);
  height: 1px;
  overflow: hidden;
  position: absolute;
  white-space: nowrap;
  width: 1px;
}

s::before {
  content: " [start of stricken text] ";
}

s::after {
  content: " [end of stricken text] ";
}
```
:::

Some people who use screen readers deliberately disable announcing
content that creates extra verbosity. Because of this, it is important
to not abuse this technique and only apply it in situations where not
knowing content has been struck out would adversely affect
understanding.

-   [Short note on making your mark (more accessible) \| The Paciello
    Group](https://www.tpgi.com/short-note-on-making-your-mark-more-accessible/){target="_blank"}
-   [Tweaking Text Level Styles \| Adrian
    Roselli](https://adrianroselli.com/2017/12/tweaking-text-level-styles.html){target="_blank"}
:::

## Specifications

::: _table
  ---------------------------------------------------------------------------------------------------------
  Specification
  ---------------------------------------------------------------------------------------------------------
  [HTML Standard\
  [\#
  the-s-element]{.small}](https://html.spec.whatwg.org/multipage/text-level-semantics.html#the-s-element)

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

  `s`   1         12     1                   Yes        15      ≤4       4.4       18        4         14        ≤3.2     1.0
                                                                                                                          
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
-   The [`<strike>`](strike) element, alter ego of the
    [`<s>`](s){aria-current="page"} element, is obsolete and should not
    be used on websites anymore.
-   The [`<del>`](del) element is to be used instead if the data has
    been *deleted*.
-   The CSS
    [`text-decoration-line`](https://developer.mozilla.org/en-US/docs/Web/CSS/text-decoration-line)
    property is to be used to achieve the former visual aspect of the
    [`<s>`](s){aria-current="page"} element.
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Element/s](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/s){._attribution-link}
:::
