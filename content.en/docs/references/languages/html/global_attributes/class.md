

# class



::: section-content
The `class` [global attribute](../global_attributes) is a
space-separated list of the case-sensitive classes of the element.
Classes allow CSS and JavaScript to select and access specific elements
via the [class
selectors](https://developer.mozilla.org/en-US/docs/Web/CSS/Class_selectors)
or functions like the DOM method
[`document.getElementsByClassName`](https://developer.mozilla.org/en-US/docs/Web/API/Document/getElementsByClassName).
:::

## Try it {#try_it}

::: section-content
::: iframe
::: {.output-header .border-rounded-top}
#### HTML Demo: class {#html-demo-class .output-heading}

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
    <p>Narrator: This is the beginning of the play.</p>

    <p class="note editorial">Above point sounds a bit obvious. Remove/rewrite?</p>

    <p>Narrator: I must warn you now folks that this beginning is very exciting.</p>

    <p class="note">[Lights go up and wind blows; Caspian enters stage right]</p>
:::
:::

::: {#css-panel .section .hidden tabindex="0" role="tabpanel" aria-labelledby="css" aria-hidden="true"}
::: {#css-editor}
    .note {
      font-style: italic;
      font-weight: bold;
    }

    .editorial {
      background: rgb(255, 0, 0, 0.25);
      padding: 10px;
    }

    .editorial:before {
      content: 'Editor: ';
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

Though the specification doesn\'t put requirements on the name of
classes, web developers are encouraged to use names that describe the
semantic purpose of the element, rather than the presentation of the
element. For example, *attribute* to describe an attribute rather than
*italics*, although an element of this class may be presented by
*italics*. Semantic names remain logical even if the presentation of the
page changes.
:::

## Specifications

::: _table
  --------------------------------------------------------------------------------------------------------------------
  Specification
  --------------------------------------------------------------------------------------------------------------------
  [HTML Standard\
  [\#
  global-attributes:classes-2]{.small}](https://html.spec.whatwg.org/multipage/dom.html#global-attributes:classes-2)

  --------------------------------------------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
            Desktop                                                         Mobile                                                                                   
  --------- --------- ------ --------- ------------------- ------- -------- ----------------- ---------------- --------------------- --------------- --------------- ------------------
            Chrome    Edge   Firefox   Internet Explorer   Opera   Safari   WebView Android   Chrome Android   Firefox for Android   Opera Android   Safari on IOS   Samsung Internet
  `class`   1         12     1         Yes                 15      ≤4       4.4               18               4                     14              ≤3.2            1.0
:::

## See also {#see_also}

::: section-content
-   All [global attributes](../global_attributes).
-   [`element.className`](https://developer.mozilla.org/en-US/docs/Web/API/Element/className)
-   [`element.classList`](https://developer.mozilla.org/en-US/docs/Web/API/Element/classList)
-   [Introduction to
    CSS](https://developer.mozilla.org/en-US/docs/Learn/CSS)
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/class](https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/class){._attribution-link}
:::
