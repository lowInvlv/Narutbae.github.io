

# \<address\>: The Contact Address element



::: section-content
The `<address>` [HTML](../index) element indicates that the enclosed
HTML provides contact information for a person or people, or for an
organization.
:::

## Try it {#try_it}

::: section-content
::: iframe
::: {.output-header .border-rounded-top}
#### HTML Demo: \<address\> {#html-demo-address .output-heading}

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
    <p>Contact the author of this page:</p>

    <address>
      <a href="mailto:jim@rock.com">jim@rock.com</a><br />
      <a href="tel:+13115552368">(311) 555-2368</a>
    </address>
:::
:::

::: {#css-panel .section .hidden tabindex="0" role="tabpanel" aria-labelledby="css" aria-hidden="true"}
::: {#css-editor}
    a[href^='mailto']::before {
      content: '📧 ';
    }

    a[href^='tel']::before {
      content: '📞 ';
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

The contact information provided by an `<address>` element\'s contents
can take whatever form is appropriate for the context, and may include
any type of contact information that is needed, such as a physical
address, URL, email address, phone number, social media handle,
geographic coordinates, and so forth. The `<address>` element should
include the name of the person, people, or organization to which the
contact information refers.

`<address>` can be used in a variety of contexts, such as providing a
business\'s contact information in the page header, or indicating the
author of an article by including an `<address>` element within the
[`<article>`](article).
:::

## Attributes

::: section-content
This element only includes the [global
attributes](../global_attributes).
:::

## Usage notes {#usage_notes}

::: section-content
-   The `<address>` element can only be used to represent the contact
    information for its nearest [`<article>`](article) or
    [`<body>`](body) element ancestor.
-   This element should not contain more information than the contact
    information, like a publication date (which belongs in a
    [`<time>`](time) element).
-   Typically an `<address>` element can be placed inside the
    [`<footer>`](footer) element of the current section, if any.
:::

## Examples

::: section-content
This example demonstrates the use of `<address>` to demarcate the
contact information for an article\'s author.

::: code-example
[html]{.language-name}

``` {signature="HSgCVynSQQpCbBCnvdL264YbPY4qB5vhI7Yiu8NtBSw=" data-language="html"}
<address>
  You can contact author at
  <a href="http://www.somedomain.com/contact">www.somedomain.com</a>.<br />
  If you see any bugs, please
  <a href="mailto:webmaster@somedomain.com">contact webmaster</a>.<br />
  You may also want to visit us:<br />
  Mozilla Foundation<br />
  331 E Evelyn Ave<br />
  Mountain View, CA 94041<br />
  USA
</address>
```
:::
:::

### Result

::: section-content
::: {#sect1 .code-example}
::: iframe
:::
:::

Although it renders text with the same default styling as the [`<i>`](i)
or [`<em>`](em) elements, it is more appropriate to use `<address>` when
dealing with contact information, as it conveys additional semantic
information.
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
<td><a href="../content_categories#flow_content">Flow content</a>,
palpable content.</td>
</tr>
<tr class="even">
<th scope="row">Permitted content</th>
<td><a href="../content_categories#flow_content">Flow content</a>, but
with no nested <code>&lt;address&gt;</code> element, no heading content
(<a href="hgroup"><code>&lt;hgroup&gt;</code></a>, <a
href="heading_elements">h1</a>, <a href="heading_elements">h2</a>, <a
href="heading_elements">h3</a>, <a href="heading_elements">h4</a>, <a
href="heading_elements">h5</a>, <a href="heading_elements">h6</a>), no
sectioning content (<a href="article"><code>&lt;article&gt;</code></a>,
<a href="aside"><code>&lt;aside&gt;</code></a>, <a
href="section"><code>&lt;section&gt;</code></a>, <a
href="nav"><code>&lt;nav&gt;</code></a>), and no <a
href="header"><code>&lt;header&gt;</code></a> or <a
href="footer"><code>&lt;footer&gt;</code></a> element.</td>
</tr>
<tr class="odd">
<th scope="row">Tag omission</th>
<td>None, both the starting and ending tag are mandatory.</td>
</tr>
<tr class="even">
<th scope="row">Permitted parents</th>
<td>Any element that accepts <a
href="../content_categories#flow_content">flow content</a>, but always
excluding <code>&lt;address&gt;</code> elements (according to the
logical principle of symmetry, if <code>&lt;address&gt;</code> tag, as a
parent, can not have nested <code>&lt;address&gt;</code> element, then
the same <code>&lt;address&gt;</code> content can not have
<code>&lt;address&gt;</code> tag as its parent).</td>
</tr>
<tr class="odd">
<th scope="row">Implicit ARIA role</th>
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/group_role"><code>group</code></a></td>
</tr>
<tr class="even">
<th scope="row">Permitted ARIA roles</th>
<td>Any</td>
</tr>
<tr class="odd">
<th scope="row">DOM interface</th>
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement"><code>HTMLElement</code></a>
Prior to Gecko 2.0 (Firefox 4), Gecko implemented this element using the
<a
href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLSpanElement"><code>HTMLSpanElement</code></a>
interface</td>
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
  the-address-element]{.small}](https://html.spec.whatwg.org/multipage/sections.html#the-address-element)

  ---------------------------------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
              Desktop                                                         Mobile                                                                                   
  ----------- --------- ------ --------- ------------------- ------- -------- ----------------- ---------------- --------------------- --------------- --------------- ------------------
              Chrome    Edge   Firefox   Internet Explorer   Opera   Safari   WebView Android   Chrome Android   Firefox for Android   Opera Android   Safari on IOS   Samsung Internet
  `address`   1         12     1         Yes                 15      1        4.4               18               4                     14              1               1.0
:::

## See also {#see_also}

::: section-content
-   Others section-related elements: [`<body>`](body), [`<nav>`](nav),
    [`<article>`](article), [`<aside>`](aside), [h1](heading_elements),
    [h2](heading_elements), [h3](heading_elements),
    [h4](heading_elements), [h5](heading_elements),
    [h6](heading_elements), [`<hgroup>`](hgroup), [`<footer>`](footer),
    [`<section>`](section), [`<header>`](header);
-   [Sections and outlines of an HTML document](heading_elements).
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Element/address](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/address){._attribution-link}
:::
