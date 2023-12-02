

# \<map\>: The Image Map element



::: section-content
The `<map>` [HTML](../index) element is used with [`<area>`](area)
elements to define an image map (a clickable link area).
:::

## Try it {#try_it}

::: section-content
::: iframe
::: {.output-header .border-rounded-top}
#### HTML Demo: \<map\> {#html-demo-map .output-heading}

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
    <map name="infographic">
      <area
        shape="poly"
        coords="130,147,200,107,254,219,130,228"
        href="https://developer.mozilla.org/docs/Web/HTML"
        target="_blank"
        alt="HTML" />
      <area
        shape="poly"
        coords="130,147,130,228,6,219,59,107"
        href="https://developer.mozilla.org/docs/Web/CSS"
        target="_blank"
        alt="CSS" />
      <area
        shape="poly"
        coords="130,147,200,107,130,4,59,107"
        href="https://developer.mozilla.org/docs/Web/JavaScript"
        target="_blank"
        alt="JavaScript" />
    </map>
    <img usemap="#infographic" src="/media/examples/mdn-info2.png" alt="MDN infographic" />
:::
:::

::: {#css-panel .section .hidden tabindex="0" role="tabpanel" aria-labelledby="css" aria-hidden="true"}
::: {#css-editor}
    img {
      display: block;
      margin: 0 auto;
      width: 260px;
      height: 232px;
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
This element includes the [global attributes](../global_attributes).

[`name`](#name)

:   The `name` attribute gives the map a name so that it can be
    referenced. The attribute must be present and must have a non-empty
    value with no space characters. The value of the `name` attribute
    must not be equal to the value of the `name` attribute of another
    `<map>` element in the same document. If the
    [`id`](../global_attributes#id) attribute is also specified, both
    attributes must have the same value.
:::

## Examples

### Image map with two areas {#image_map_with_two_areas}

::: section-content
Click the left-hand parrot for JavaScript, or the right-hand parrot for
CSS.

#### HTML

::: code-example
[html]{.language-name}

``` {signature="LEh5/t8XIY1dh+1Z5cZFYcYdrDJL438BprxMI1C1vGw=" data-language="html"}
<!-- Photo by Juliana e Mariana Amorim on Unsplash -->
<map name="primary">
  <area
    shape="circle"
    coords="75,75,75"
    href="https://developer.mozilla.org/docs/Web/JavaScript"
    target="_blank"
    alt="JavaScript" />
  <area
    shape="circle"
    coords="275,75,75"
    href="https://developer.mozilla.org/docs/Web/CSS"
    target="_blank"
    alt="CSS" />
</map>
<img
  usemap="#primary"
  src="parrots.jpg"
  alt="350 x 150 picture of two parrots" />
```
:::

#### Result

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
<td>Any <a
href="../content_categories#transparent_content_model">transparent</a>
element.</td>
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
href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLMapElement"><code>HTMLMapElement</code></a></td>
</tr>
</tbody>
</table>

</figure>
:::

## Specifications

::: _table
  ---------------------------------------------------------------------------------------------------
  Specification
  ---------------------------------------------------------------------------------------------------
  [HTML Standard\
  [\#
  the-map-element]{.small}](https://html.spec.whatwg.org/multipage/image-maps.html#the-map-element)

  ---------------------------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
  --------------------------------------------------------------------------------------------------------------------------------------
           Desktop                                                           Mobile                                           
  -------- --------- ------ -------------------- ---------- ------- -------- --------- --------- --------- --------- -------- ----------
           Chrome    Edge   Firefox              Internet   Opera   Safari   WebView   Chrome    Firefox   Opera     Safari   Samsung
                                                 Explorer                    Android   Android   for       Android   on IOS   Internet
                                                                                                 Android                      

  `map`    1         12     1                    Yes        15      1        4.4       18        4         14        1        1.0
                                                                                                                              
                            \[\"Before Firefox                                                                                
                            5, in Quirks Mode,                                                                                
                            empty maps were no                                                                                
                            longer skipped over                                                                               
                            in favor of                                                                                       
                            non-empty ones when                                                                               
                            matching.\",                                                                                      
                            \"Before Firefox 17,                                                                              
                            the default styling                                                                               
                            of the `<map>` HTML                                                                               
                            element was                                                                                       
                            `display: block;`.                                                                                
                            This is now                                                                                       
                            `display: inline;`                                                                                
                            and matches the                                                                                   
                            behavior of the                                                                                   
                            other browsers. It                                                                                
                            was already the case                                                                              
                            in Quirks Mode.\"\]                                                                               

  `name`   1         12     1                    Yes        15      1        4.4       18        4         14        1        1.0
  --------------------------------------------------------------------------------------------------------------------------------------
:::

## See also {#see_also}

::: section-content
-   [`<a>`](a)
-   [`<area>`](area)
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Element/map](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/map){._attribution-link}
:::
