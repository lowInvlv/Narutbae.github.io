

# style



::: section-content
The `style` [global attribute](../global_attributes) contains
[CSS](https://developer.mozilla.org/en-US/docs/Web/CSS) styling
declarations to be applied to the element. Note that it is recommended
for styles to be defined in a separate file or files. This attribute and
the [`<style>`](../element/style) element have mainly the purpose of
allowing for quick styling, for example for testing purposes.
:::

## Try it {#try_it}

::: section-content
::: iframe
::: {.output-header .border-rounded-top}
#### HTML Demo: style {#html-demo-style .output-heading}

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
    <div style="background: #ffe7e8; border: 2px solid #e66465">
      <p style="margin: 15px; line-height: 1.5; text-align: center">
        Well, I am the slime from your video<br />
        Oozin' along on your livin' room floor.
      </p>
    
:::
:::

::: {#css-panel .section .hidden tabindex="0" role="tabpanel" aria-labelledby="css" aria-hidden="true"}
::: {#css-editor}
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

::: {#sect1 .notecard .note}
**Note:** This attribute must not be used to convey semantic
information. Even if all styling is removed, a page should remain
semantically correct. Typically it shouldn\'t be used to hide irrelevant
information; this should be done using the [`hidden`](hidden) attribute.
:::
:::

## Specifications

::: _table
  ----------------------------------------------------------------------------------------------------
  Specification
  ----------------------------------------------------------------------------------------------------
  [HTML Standard\
  [\#
  the-style-attribute]{.small}](https://html.spec.whatwg.org/multipage/dom.html#the-style-attribute)

  ----------------------------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
            Desktop                                                         Mobile                                                                                   
  --------- --------- ------ --------- ------------------- ------- -------- ----------------- ---------------- --------------------- --------------- --------------- ------------------
            Chrome    Edge   Firefox   Internet Explorer   Opera   Safari   WebView Android   Chrome Android   Firefox for Android   Opera Android   Safari on IOS   Samsung Internet
  `style`   1         12     1         Yes                 15      1        4.4               18               4                     14              1               1.0
:::

## See also {#see_also}

::: section-content
All [global attributes](../global_attributes).
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/style](https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/style){._attribution-link}
:::
