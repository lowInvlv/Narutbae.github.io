

# data-\*



::: section-content
The `data-*` [global attributes](../global_attributes) form a class of
attributes called **custom data attributes**, that allow proprietary
information to be exchanged between the [HTML](../index) and its
[DOM](https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model)
representation by scripts.
:::

## Try it {#try_it}

::: section-content
::: iframe
::: {.output-header .border-rounded-top}
#### HTML Demo: data-\* {#html-demo-data- .output-heading}

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
    <h1>Secret agents</h1>

    <ul>
      <li data-id="10784">Jason Walters, 003: Found dead in "A View to a Kill".</li>
      <li data-id="97865">Alex Trevelyan, 006: Agent turned terrorist leader; James' nemesis in "Goldeneye".</li>
      <li data-id="45732">James Bond, 007: The main man; shaken but not stirred.</li>
    </ul>
:::
:::

::: {#css-panel .section .hidden tabindex="0" role="tabpanel" aria-labelledby="css" aria-hidden="true"}
::: {#css-editor}
    h1 {
      margin: 0;
    }

    ul {
      margin: 10px 0 0;
    }

    li {
      position: relative;
      width: 200px;
      padding-bottom: 10px;
    }

    li:after {
      content: 'Data ID: ' attr(data-id);
      position: absolute;
      top: -22px;
      left: 10px;
      background: black;
      color: white;
      padding: 2px;
      border: 1px solid #eee;
      opacity: 0;
      transition: 0.5s opacity;
    }

    li:hover:after {
      opacity: 1;
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

All such custom data are available via the
[`HTMLElement`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement)
interface of the element the attribute is set on. The
[`HTMLElement.dataset`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/dataset)
property gives access to them. The `*` may be replaced by any name
following [the production rule of XML
names](https://www.w3.org/TR/REC-xml/#NT-Name){target="_blank"} which
includes the following recommendations:

-   The name should not start with `xml` (case-insensitive), as it\'s
    reserved for future XML specifications.
-   The name should not contain any colon characters (`:`), as XML
    assigns meaning to such names.
-   The name should not contain any capital letters, as XML is all
    lowercase.

These are recommendations. If these naming recommendations are not
followed, no errors will occur. The attributes will still be matched
using CSS [attribute
selectors](https://developer.mozilla.org/en-US/docs/Web/CSS/Attribute_selectors),
with the attribute being case insensitive and any attribute value being
case-sensitive. Attributes not conforming to these three recommendations
will also still be recognized by the JavaScript
[`HTMLElement.dataset`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/dataset)
property and user-agents will include the attribute in the
[`DOMStringMap`](https://developer.mozilla.org/en-US/docs/Web/API/DOMStringMap)
containing all the custom data attributes for an
[`HTMLElement`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement).

If you plan to use
[`HTMLElement.dataset`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/dataset),
the portion of the attribute name following the `data-` can only include
characters allowed in JavaScript property names (and hyphens, which will
be removed). The `dataset` version of the attribute name removes the
\"data-\" prefix and converts the rest of the name from
[kebab-case](https://developer.mozilla.org/en-US/docs/Glossary/Kebab_case)
to camelCase. For example, `element.getAttribute("data-test")` is
equivalent to `element.dataset.test` and `data-test-abc` will be
accessible as `HTMLElement.dataset.testAbc` (or by
`HTMLElement.dataset["testAbc"]`). Avoid non-alphabetic characters
following a hyphen, such as `data-test-1` or `data--test`, as they will
not be recognized by
[`HTMLElement.dataset`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/dataset).
:::

### Usage

::: section-content
By adding `data-*` attributes, even ordinary HTML elements can become
rather complex and powerful program-objects. For example, a space-ship
\"[sprite](https://en.wikipedia.org/wiki/Sprite_(computer_graphics)){target="_blank"}*\"*
in a game could be a simple [`<img>`](../element/img) element with a
[`class`](class) attribute and several `data-*` attributes:

::: code-example
[html]{.language-name}

``` {signature="a1qPQkSymHZrc1ikVb3riZH1wdTVj2cS0/1v256K3Bg=" data-language="html"}
<img
  class="spaceship cruiserX3"
  src="shipX3.png"
  data-ship-id="324"
  data-weapons="laserI laserII"
  data-shields="72%"
  data-x="414354"
  data-y="85160"
  data-z="31940"
  onclick="spaceships[this.dataset.shipId].blasted()" />
```
:::

For a more in-depth tutorial about using HTML data attributes, see
[Using data
attributes](https://developer.mozilla.org/en-US/docs/Learn/HTML/Howto/Use_data_attributes).
:::

## Specifications

::: _table
  -------------------------------------------------------------------------------------
  Specification
  -------------------------------------------------------------------------------------
  [HTML Standard\
  [\#
  attr-data-\*]{.small}](https://html.spec.whatwg.org/multipage/dom.html#attr-data-*)

  -------------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
             Desktop                                                         Mobile                                                                                   
  ---------- --------- ------ --------- ------------------- ------- -------- ----------------- ---------------- --------------------- --------------- --------------- ------------------
             Chrome    Edge   Firefox   Internet Explorer   Opera   Safari   WebView Android   Chrome Android   Firefox for Android   Opera Android   Safari on IOS   Samsung Internet
  `data-*`   7         12     6         Yes                 15      5.1      4.4               18               6                     14              5               1.0
:::

## See also {#see_also}

::: section-content
-   All [global attributes](../global_attributes).
-   The
    [`HTMLElement.dataset`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/dataset)
    property that allows to access and modify these values.
-   [Using data
    attributes](https://developer.mozilla.org/en-US/docs/Learn/HTML/Howto/Use_data_attributes)
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/data-\*](https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/data-*){._attribution-link}
:::
