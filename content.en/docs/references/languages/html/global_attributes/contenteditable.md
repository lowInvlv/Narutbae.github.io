

# contenteditable



::: section-content
The `contenteditable` [global attribute](../global_attributes) is an
enumerated attribute indicating if the element should be editable by the
user. If so, the browser modifies its widget to allow editing.
:::

## Try it {#try_it}

::: section-content
::: iframe
::: {.output-header .border-rounded-top}
#### HTML Demo: contenteditable {#html-demo-contenteditable .output-heading}

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
    <blockquote contenteditable="true">
      <p>Edit this content to add your own quote</p>
    </blockquote>

    <cite contenteditable="true">-- Write your own name here</cite>
:::
:::

::: {#css-panel .section .hidden tabindex="0" role="tabpanel" aria-labelledby="css" aria-hidden="true"}
::: {#css-editor}
    blockquote {
      background: #eee;
      border-radius: 5px;
      margin: 16px 0;
    }

    blockquote p {
      padding: 15px;
    }

    cite {
      margin: 16px 32px;
      font-weight: bold;
    }

    blockquote p::before {
      content: '\201C';
    }

    blockquote p::after {
      content: '\201D';
    }

    [contenteditable='true'] {
      caret-color: red;
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

The attribute must take one of the following values:

-   `true` or an *empty string*, which indicates that the element is
    editable.
-   `false`, which indicates that the element is not editable.
-   `plaintext-only`, which indicates that the element\'s raw text is
    editable, but rich text formatting is disabled.

If the attribute is given without a value, like
`<label contenteditable>Example Label</label>`, its value is treated as
an empty string.

If this attribute is missing or its value is invalid, its value is
*inherited* from its parent element: so the element is editable if its
parent is editable.

Note that although its allowed values include `true` and `false`, this
attribute is an
*[enumerated](https://developer.mozilla.org/en-US/docs/Glossary/Enumerated)*
one and not a *Boolean* one.

You can set the color used to draw the text insertion
[caret](https://developer.mozilla.org/en-US/docs/Glossary/Caret) with
the CSS
[`caret-color`](https://developer.mozilla.org/en-US/docs/Web/CSS/caret-color)
property.

Elements that are made editable, and therefore interactive, by using the
`contenteditable` attribute can be focused. They participate in
sequential keyboard navigation. However, elements with the
`contenteditable` attribute nested within other `contenteditable`
elements are not added to the tabbing sequence by default. You can add
the nested `contenteditable` elements to the keyboard navigation
sequence by specifying the `tabindex` value
([`tabindex="0"`](tabindex)).
:::

## Specifications

::: _table
  --------------------------------------------------------------------------------------------------------------
  Specification
  --------------------------------------------------------------------------------------------------------------
  [HTML Standard\
  [\#
  attr-contenteditable]{.small}](https://html.spec.whatwg.org/multipage/interaction.html#attr-contenteditable)

  --------------------------------------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
                      Desktop                                                         Mobile                                                                                   
  ------------------- --------- ------ --------- ------------------- ------- -------- ----------------- ---------------- --------------------- --------------- --------------- ------------------
                      Chrome    Edge   Firefox   Internet Explorer   Opera   Safari   WebView Android   Chrome Android   Firefox for Android   Opera Android   Safari on IOS   Samsung Internet
  `contenteditable`   1         12     3         5.5                 9       ≤4       4.4               18               4                     14              ≤3.2            1.0
  `plaintext-only`    51        ≤79    No        No                  38      Yes      51                51               No                    41              Yes             5.0
:::

## See also {#see_also}

::: section-content
-   All [global attributes](../global_attributes)
-   [`HTMLElement.contentEditable`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/contentEditable)
    and
    [`HTMLElement.isContentEditable`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/isContentEditable)
-   The CSS
    [`caret-color`](https://developer.mozilla.org/en-US/docs/Web/CSS/caret-color)
    property
-   [HTMLElement `input`
    event](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/input_event)
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/contenteditable](https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/contenteditable){._attribution-link}
:::
