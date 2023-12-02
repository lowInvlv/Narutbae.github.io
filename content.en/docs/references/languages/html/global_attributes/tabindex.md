

# tabindex



::: section-content
The `tabindex` [global attribute](../global_attributes) allows
developers to make HTML elements focusable, allow or prevent them from
being sequentially focusable (usually with the [Tab]{.kbd} key, hence
the name) and determine their relative ordering for sequential focus
navigation.
:::

## Try it {#try_it}

::: section-content
::: iframe
::: {.output-header .border-rounded-top}
#### HTML Demo: tabindex {#html-demo-tabindex .output-heading}

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
    <p>Click anywhere in this pane, then try tabbing through the elements.</p>

    <label>First in tab order:<input type="text" /></label>

    <div tabindex="0">Tabbable due to tabindex.

    Not tabbable: no tabindex.

    <label>Third in tab order:<input type="text" /></label>
:::
:::

::: {#css-panel .section .hidden tabindex="0" role="tabpanel" aria-labelledby="css" aria-hidden="true"}
::: {#css-editor}
    p {
      font-style: italic;
      font-weight: bold;
    }

    div,
    label {
      display: block;
      letter-spacing: 0.5px;
      margin-bottom: 1rem;
    }

    div:focus {
      font-weight: bold;
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

It accepts an integer as a value, with different results depending on
the integer\'s value:

::: {#sect1 .notecard .note}
**Note:** If an HTML element renders and has `tabindex` attribute with
any valid integer value, the element can be focused with JavaScript (by
calling the
[`focus()`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/focus)
method) or visually by clicking with the mouse. The particular
`tabindex` value controls whether the element is `tabbable` (i.e.
reachable via sequential keyboard navigation, usually with the
[Tab]{.kbd} key).
:::

-   A *negative value* (the exact negative value doesn\'t actually
    matter, usually `tabindex="-1"`) means that the element is not
    reachable via sequential keyboard navigation.

    ::: {#sect2 .notecard .note}
    **Note:** `tabindex="-1"` may be useful for elements that should not
    be navigated to directly using the [Tab]{.kbd} key, but need to have
    keyboard focus set to them. Examples include an off-screen modal
    window that should be focused when it comes into view, or a form
    submission error message that should be immediately focused when an
    errant form is submitted.
    :::
-   `tabindex="0"` means that the element should be focusable in
    sequential keyboard navigation, after any positive `tabindex`
    values. The focus navigation order of these elements is defined by
    their order in the document source.
-   A *positive value* means the element should be focusable in
    sequential keyboard navigation, with its order defined by the value
    of the number. That is, `tabindex="4"` is focused before
    `tabindex="5"` and `tabindex="0"`, but after `tabindex="3"`. If
    multiple elements share the same positive `tabindex` value, their
    order relative to each other follows their position in the document
    source. The maximum value for `tabindex` is 32767.
-   If the `tabindex` attribute is included with no value set, whether
    the element is focusable is determined by the user agent.

    ::: {#sect3 .notecard .warning}
    **Warning:** You are recommended to only use `0` and `-1` as
    `tabindex` values. Avoid using `tabindex` values greater than `0`
    and CSS properties that can change the order of focusable HTML
    elements ([Ordering flex
    items](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_flexible_box_layout/Ordering_flex_items)).
    Doing so makes it difficult for people who rely on using keyboard
    for navigation or assistive technology to navigate and operate page
    content. Instead, write the document with the elements in a logical
    sequence.
    :::

Some focusable HTML elements have a default `tabindex` value of `0` set
under the hood by the [user
agent](https://developer.mozilla.org/en-US/docs/Glossary/User_agent).
These elements are an [`<a>`](../element/a) or
[`<area>`](../element/area) with `href` attribute,
[`<button>`](../element/button), [`<frame>`](../element/frame)
[Deprecated]{.visually-hidden} , [`<iframe>`](../element/iframe),
[`<input>`](../element/input), [`<object>`](../element/object),
[`<select>`](../element/select), [`<textarea>`](../element/textarea),
and SVG
[`<a>`](https://developer.mozilla.org/en-US/docs/Web/SVG/Element/a)
element, or a [`<summary>`](../element/summary) element that provides
summary for a [`<details>`](../element/details) element. Developers
shouldn\'t add the `tabindex` attribute to these elements unless it
changes the default behavior (for example, including a negative value
will remove the element from the focus navigation order).

::: {#sect4 .notecard .warning}
**Warning:** The tabindex attribute must not be used on the
[`<dialog>`](../element/dialog) element.
:::
:::

## Accessibility concerns {#accessibility_concerns}

::: section-content
Avoid using the `tabindex` attribute in conjunction with
non-[interactive content](../content_categories#interactive_content) to
make something intended to be interactive focusable by keyboard input.
An example of this would be using a [``](../element/div) element to
describe a button, instead of the [`<button>`](../element/button)
element.

Interactive components authored using non-interactive elements are not
listed in the [accessibility
tree](https://developer.mozilla.org/en-US/docs/Learn/Accessibility/What_is_accessibility#accessibility_apis).
This prevents assistive technology from being able to navigate to and
manipulate those components. The content should be semantically
described using interactive elements ([`<a>`](../element/a),
[`<button>`](../element/button), [`<details>`](../element/details),
[`<input>`](../element/input), [`<select>`](../element/select),
[`<textarea>`](../element/textarea), etc.) instead. These elements have
built-in roles and states that communicate status to the accessibility
that would otherwise have to be managed by
[ARIA](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA).

-   [Using the tabindex attribute \| The Paciello
    Group](https://www.tpgi.com/using-the-tabindex-attribute/){target="_blank"}
:::

## Specifications

::: _table
  ------------------------------------------------------------------------------------------------
  Specification
  ------------------------------------------------------------------------------------------------
  [HTML Standard\
  [\#
  attr-tabindex]{.small}](https://html.spec.whatwg.org/multipage/interaction.html#attr-tabindex)

  ------------------------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
               Desktop                                                         Mobile                                                                                   
  ------------ --------- ------ --------- ------------------- ------- -------- ----------------- ---------------- --------------------- --------------- --------------- ------------------
               Chrome    Edge   Firefox   Internet Explorer   Opera   Safari   WebView Android   Chrome Android   Firefox for Android   Opera Android   Safari on IOS   Samsung Internet
  `tabindex`   1         12     1.5       Yes                 15      ≤4       4.4               18               4                     14              ≤3.2            1.0
:::

## See also {#see_also}

::: section-content
-   All [global attributes](../global_attributes)
-   [`HTMLElement.tabIndex`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/tabIndex)
    that reflects this attribute
-   Accessibility problems with `tabindex`: see [Don\'t Use Tabindex
    Greater than
    0](https://adrianroselli.com/2014/11/dont-use-tabindex-greater-than-0.html){target="_blank"}
    by Adrian Roselli
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/tabindex](https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/tabindex){._attribution-link}
:::
