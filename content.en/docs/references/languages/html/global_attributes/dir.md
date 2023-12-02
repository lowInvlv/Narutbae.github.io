

# dir



::: section-content
The `dir` [global attribute](../global_attributes) is an
[enumerated](https://developer.mozilla.org/en-US/docs/Glossary/Enumerated)
attribute that indicates the directionality of the element\'s text.
:::

## Try it {#try_it}

::: section-content
::: iframe
::: {.output-header .border-rounded-top}
#### HTML Demo: dir {#html-demo-dir .output-heading}

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
    <p dir="rtl">This paragraph is in English but incorrectly goes right to left.</p>
    <p dir="ltr">This paragraph is in English and correctly goes left to right.</p>

    <hr />

    <p>هذه الفقرة باللغة العربية ولكن بشكل خاطئ من اليسار إلى اليمين.</p>
    <p dir="auto">هذه الفقرة باللغة العربية ، لذا يجب الانتقال من اليمين إلى اليسار.</p>
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

It can have the following values:

-   `ltr`, which means *left to right* and is to be used for languages
    that are written from the left to the right (like English);
-   `rtl`, which means *right to left* and is to be used for languages
    that are written from the right to the left (like Arabic);
-   `auto`, which lets the user agent decide. It uses a basic algorithm
    as it parses the characters inside the element until it finds a
    character with a strong directionality, then applies that
    directionality to the whole element.

::: {#sect1 .notecard .note}
**Note:** This attribute is mandatory for the [`<bdo>`](../element/bdo)
element where it has a different semantic meaning.

-   This attribute is *not* inherited by the [`<bdi>`](../element/bdi)
    element. If not set, its value is `auto`.
-   This attribute can be overridden by the CSS properties
    [`direction`](https://developer.mozilla.org/en-US/docs/Web/CSS/direction)
    and
    [`unicode-bidi`](https://developer.mozilla.org/en-US/docs/Web/CSS/unicode-bidi),
    if a CSS page is active and the element supports these properties.
-   As the directionality of the text is semantically related to its
    content and not to its presentation, it is recommended that web
    developers use this attribute instead of the related CSS properties
    when possible. That way, the text will display correctly even on a
    browser that doesn\'t support CSS or has the CSS deactivated.
-   The `auto` value should be used for data with an unknown
    directionality, like data coming from user input, eventually stored
    in a database.
:::

::: {#sect2 .notecard .note}
**Note:** Browsers might allow users to change the directionality of
[`<input>`](../element/input) and [`<textarea>`](../element/textarea)s
in order to assist with authoring content. Chrome and Safari provide a
directionality option in the contextual menu of input fields while
Legacy Edge uses the key combinations [Ctrl]{.kbd} + [Left Shift]{.kbd}
and [Ctrl]{.kbd} + [Right Shift]{.kbd}. Firefox uses
[Ctrl]{.kbd}/[Cmd]{.kbd} + [Shift]{.kbd} + [X]{.kbd} but does NOT update
the `dir` attribute value.
:::
:::

## Specifications

::: _table
  ------------------------------------------------------------------------------------------------
  Specification
  ------------------------------------------------------------------------------------------------
  [HTML Standard\
  [\#
  the-dir-attribute]{.small}](https://html.spec.whatwg.org/multipage/dom.html#the-dir-attribute)

  ------------------------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
          Desktop                                                         Mobile                                                                                   
  ------- --------- ------ --------- ------------------- ------- -------- ----------------- ---------------- --------------------- --------------- --------------- ------------------
          Chrome    Edge   Firefox   Internet Explorer   Opera   Safari   WebView Android   Chrome Android   Firefox for Android   Opera Android   Safari on IOS   Samsung Internet
  `dir`   1         79     1         No                  15      ≤4       4.4               18               4                     14              ≤3.2            1.0
:::

## See also {#see_also}

::: section-content
-   All [global attributes](../global_attributes).
-   [`HTMLElement.dir`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/dir)
    that reflects this attribute.
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/dir](https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/dir){._attribution-link}
:::
