

# enterkeyhint



::: section-content
The `enterkeyhint` [global attribute](../global_attributes) is an
[enumerated](https://developer.mozilla.org/en-US/docs/Glossary/Enumerated)
attribute defining what action label (or icon) to present for the enter
key on virtual keyboards.
:::

## Try it {#try_it}

::: section-content
::: iframe
::: {.output-header .border-rounded-top}
#### HTML Demo: enterkeyhint {#html-demo-enterkeyhint .output-heading}

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
    <input enterkeyhint="go" />

    <p contenteditable enterkeyhint="go">https://example.org</p>
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
:::

## Description

::: section-content
[Form controls](https://developer.mozilla.org/en-US/docs/Learn/Forms)
(such as [`<textarea>`](../element/textarea) or
[`<input>`](../element/input) elements) or elements using
[`contenteditable`](contenteditable) can specify an
[`inputmode`](inputmode) attribute to control what kind of virtual
keyboard will be used. To further improve the user\'s experience, the
enter key can be customized specifically by providing an `enterkeyhint`
attribute indicating how the enter key should be labeled (or which icon
should be shown). The enter key usually represents what the user should
do next; typical actions are: sending text, inserting a new line, or
searching.

If no `enterkeyhint` attribute is provided, the user agent might use
contextual information from the [`inputmode`](inputmode),
[`type`](../element/input#input_types), or
[`pattern`](../element/input#pattern) attributes to display a suitable
enter key label (or icon).
:::

### Values

::: section-content
The `enterkeyhint` attribute is an
[enumerated](https://developer.mozilla.org/en-US/docs/Glossary/Enumerated)
attribute and only accepts the following values:

<figure class="table-container">
<div class="_table">
<table class="no-markdown">
<thead>
<tr class="header">
<th>Value</th>
<th>Description</th>
<th>Example label (depends on user agent and user language)</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><code>enterkeyhint="enter"</code></td>
<td>Typically inserting a new line.</td>
<td><kbd>↵</kbd></td>
</tr>
<tr class="even">
<td><code>enterkeyhint="done"</code></td>
<td>Typically meaning there is nothing more to input and the input
method editor (IME) will be closed.</td>
<td><kbd>Done</kbd></td>
</tr>
<tr class="odd">
<td><code>enterkeyhint="go"</code></td>
<td>Typically meaning to take the user to the target of the text they
typed.</td>
<td><kbd>Open</kbd></td>
</tr>
<tr class="even">
<td><code>enterkeyhint="next"</code></td>
<td>Typically taking the user to the next field that will accept
text.</td>
<td><kbd>Next</kbd></td>
</tr>
<tr class="odd">
<td><code>enterkeyhint="previous"</code></td>
<td>Typically taking the user to the previous field that will accept
text.</td>
<td><kbd>Previous</kbd></td>
</tr>
<tr class="even">
<td><code>enterkeyhint="search"</code></td>
<td>Typically taking the user to the results of searching for the text
they have typed.</td>
<td><kbd>Search</kbd></td>
</tr>
<tr class="odd">
<td><code>enterkeyhint="send"</code></td>
<td>Typically delivering the text to its target.</td>
<td><kbd>Send</kbd></td>
</tr>
</tbody>
</table>

</figure>
:::

## Specifications

::: _table
  --------------------------------------------------------------------------------------------------------
  Specification
  --------------------------------------------------------------------------------------------------------
  [HTML Standard\
  [\#
  attr-enterkeyhint]{.small}](https://html.spec.whatwg.org/multipage/interaction.html#attr-enterkeyhint)

  --------------------------------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
                   Desktop                                                         Mobile                                                                                   
  ---------------- --------- ------ --------- ------------------- ------- -------- ----------------- ---------------- --------------------- --------------- --------------- ------------------
                   Chrome    Edge   Firefox   Internet Explorer   Opera   Safari   WebView Android   Chrome Android   Firefox for Android   Opera Android   Safari on IOS   Samsung Internet
  `enterkeyhint`   77        79     94        No                  66      13.1     77                77               94                    57              13.4            12.0
:::

## See also {#see_also}

::: section-content
-   [`HTMLElement.enterKeyHint`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/enterKeyHint)
    property reflecting this attribute
-   [`inputmode`](inputmode) global attribute
-   [`contenteditable`](contenteditable) global attribute
-   [`type`](../element/input#input_types) and
    [`pattern`](../element/input#pattern) attributes on
    [`<input>`](../element/input) elements
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/enterkeyhint](https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/enterkeyhint){._attribution-link}
:::
