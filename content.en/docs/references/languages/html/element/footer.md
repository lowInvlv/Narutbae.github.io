

# \<footer\>



::: section-content
The `<footer>` [HTML](../index) element represents a footer for its
nearest ancestor [sectioning
content](../content_categories#sectioning_content) or [sectioning
root](heading_elements#sectioning_root) element. A `<footer>` typically
contains information about the author of the section, copyright data or
links to related documents.
:::

## Try it {#try_it}

::: section-content
::: iframe
::: {.output-header .border-rounded-top}
#### HTML Demo: \<footer\> {#html-demo-footer .output-heading}

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
    <article>
      <h1>How to be a wizard</h1>
      <ol>
        <li>Grow a long, majestic beard.</li>
        <li>Wear a tall, pointed hat.</li>
        <li>Have I mentioned the beard?</li>
      </ol>
      <footer>
        <p>© 2018 Gandalf</p>
      </footer>
    </article>
:::
:::

::: {#css-panel .section .hidden tabindex="0" role="tabpanel" aria-labelledby="css" aria-hidden="true"}
::: {#css-editor}
    article {
      min-height: 100%;
      display: grid;
      grid-template-rows: auto 1fr auto;
    }

    footer {
      display: flex;
      justify-content: center;
      padding: 5px;
      background-color: #45a1ff;
      color: #fff;
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
<td><a href="../content_categories#flow_content">Flow content</a>,
palpable content.</td>
</tr>
<tr class="even">
<th scope="row">Permitted content</th>
<td><a href="../content_categories#flow_content">Flow content</a>, but
with no <code>&lt;footer&gt;</code> or <a
href="header"><code>&lt;header&gt;</code></a> descendants.</td>
</tr>
<tr class="odd">
<th scope="row">Tag omission</th>
<td>None, both the starting and ending tag are mandatory.</td>
</tr>
<tr class="even">
<th scope="row">Permitted parents</th>
<td>Any element that accepts <a
href="../content_categories#flow_content">flow content</a>. Note that a
<code>&lt;footer&gt;</code> element must not be a descendant of an <a
href="address"><code>&lt;address&gt;</code></a>, <a
href="header"><code>&lt;header&gt;</code></a> or another
<code>&lt;footer&gt;</code> element.</td>
</tr>
<tr class="odd">
<th scope="row">Implicit ARIA role</th>
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/contentinfo_role">contentinfo</a>,
or <a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/generic_role">generic</a>
if a descendant of an <a href="article">article</a>, <a
href="aside">aside</a>, <a href="main">main</a>, <a href="nav">nav</a>
or <a href="section">section</a> element, or an element with
<code>role=</code><a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/article_role"><code>article</code></a>,
<a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/complementary_role">complementary</a>,
<a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/main_role">main</a>,
<a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/navigation_role">navigation</a>
or <a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/region_role">region</a></td>
</tr>
<tr class="even">
<th scope="row">Permitted ARIA roles</th>
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/group_role"><code>group</code></a>,
<a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/presentation_role"><code>presentation</code></a>
or <a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/none_role"><code>none</code></a></td>
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

## Usage notes {#usage_notes}

::: section-content
-   Enclose information about the author in an [`<address>`](address)
    element that can be included into the `<footer>` element.
-   When the nearest ancestor sectioning content or sectioning root
    element is the body element the footer applies to the whole page.
-   The `<footer>` element is not sectioning content and therefore
    doesn\'t introduce a new section in the [outline](heading_elements).
:::

## Examples

::: section-content
::: code-example
[html]{.language-name}

``` {signature="XP1GJTeWpWI4jRvXabOj0QBznJRPl5tq2G0tFdw9HeI=" data-language="html"}
<body>
  <h3>FIFA World Cup top goalscorers</h3>
  <ol>
    <li>Miroslav Klose, 16</li>
    <li>Ronaldo Nazário, 15</li>
    <li>Gerd Müller, 14</li>
  </ol>

  <footer>
    <small>
      Copyright © 2023 Football History Archives. All Rights Reserved.
    </small>
  </footer>
</body>
```
:::

::: code-example
[css]{.language-name}

``` {signature="u1v2fsaNt5NuCyxY6BzrznMfJ79vcEC6rW+QIAkFQPU=" data-language="css"}
footer {
  text-align: center;
  padding: 5px;
  background-color: #abbaba;
  color: #000;
}
```
:::

::: {#sect1 .code-example}
::: iframe
:::
:::
:::

## Accessibility concerns {#accessibility_concerns}

::: section-content
Prior to the release of Safari 13, the `contentinfo` [landmark
role](https://developer.mozilla.org/en-US/docs/Learn/Accessibility/WAI-ARIA_basics#signpostslandmarks)
was not properly exposed by
[VoiceOver](https://help.apple.com/voiceover/info/guide/){target="_blank"}.
If needing to support legacy Safari browsers, add `role="contentinfo"`
to the `footer` element to ensure the landmark will be properly exposed.

-   Related: [WebKit Bugzilla: 146930 -- AX: HTML native elements
    (header, footer, main, aside, nav) should work the same as ARIA
    landmarks, sometimes they
    don\'t](https://webkit.org/b/146930){target="_blank"}
:::

## Specifications

::: _table
  -------------------------------------------------------------------------------------------------------
  Specification
  -------------------------------------------------------------------------------------------------------
  [HTML Standard\
  [\#
  the-footer-element]{.small}](https://html.spec.whatwg.org/multipage/sections.html#the-footer-element)

  -------------------------------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
             Desktop                                                         Mobile                                                                                   
  ---------- --------- ------ --------- ------------------- ------- -------- ----------------- ---------------- --------------------- --------------- --------------- ------------------
             Chrome    Edge   Firefox   Internet Explorer   Opera   Safari   WebView Android   Chrome Android   Firefox for Android   Opera Android   Safari on IOS   Samsung Internet
  `footer`   5         12     4         9                   11.1    5        4.4               18               4                     11.1            4.2             1.0
:::

## See also {#see_also}

::: section-content
-   Other section-related elements: [`<body>`](body), [`<nav>`](nav),
    [`<article>`](article), [`<aside>`](aside), [h1](heading_elements),
    [h2](heading_elements), [h3](heading_elements),
    [h4](heading_elements), [h5](heading_elements),
    [h6](heading_elements), [`<hgroup>`](hgroup), [`<header>`](header),
    [`<section>`](section), [`<address>`](address);
-   [Using HTML sections and outlines](heading_elements)
-   [ARIA: Contentinfo
    role](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/contentinfo_role)
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Element/footer](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/footer){._attribution-link}
:::
