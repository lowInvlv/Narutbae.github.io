

# \<bdi\>: The Bidirectional Isolate element



::: section-content
The `<bdi>` [HTML](../index) element tells the browser\'s bidirectional
algorithm to treat the text it contains in isolation from its
surrounding text. It\'s particularly useful when a website dynamically
inserts some text and doesn\'t know the directionality of the text being
inserted.
:::

## Try it {#try_it}

::: section-content
::: iframe
::: {.output-header .border-rounded-top}
#### HTML Demo: \<bdi\> {#html-demo-bdi .output-heading}

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
    <h1>World wrestling championships</h1>

    <ul>
      <li><bdi class="name">Evil Steven</bdi>: 1st place</li>
      <li><bdi class="name">François fatale</bdi>: 2nd place</li>
      <li><span class="name">سما</span>: 3rd place</li>
      <li><bdi class="name">الرجل القوي إيان</bdi>: 4th place</li>
      <li><span class="name" dir="auto">سما</span>: 5th place</li>
    </ul>
:::
:::

::: {#css-panel .section .hidden tabindex="0" role="tabpanel" aria-labelledby="css" aria-hidden="true"}
::: {#css-editor}
    html {
      font-family: sans-serif;
    }

    /* stylelint-disable-next-line block-no-empty */
    bdi {
    }

    .name {
      color: red;
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

Bidirectional text is text that may contain both sequences of characters
that are arranged left-to-right (LTR) and sequences of characters that
are arranged right-to-left (RTL), such as an Arabic quotation embedded
in an English string. Browsers implement the [Unicode Bidirectional
Algorithm](https://www.w3.org/International/articles/inline-bidi-markup/uba-basics){target="_blank"}
to handle this. In this algorithm, characters are given an implicit
directionality: for example, Latin characters are treated as LTR while
Arabic characters are treated as RTL. Some other characters (such as
spaces and some punctuation) are treated as neutral and are assigned
directionality based on that of their surrounding characters.

Usually, the bidirectional algorithm will do the right thing without the
author having to provide any special markup but, occasionally, the
algorithm needs help. That\'s where `<bdi>` comes in.

The `<bdi>` element is used to wrap a span of text and instructs the
bidirectional algorithm to treat this text in isolation from its
surroundings. This works in two ways:

-   The directionality of text embedded in `<bdi>` *does not influence*
    the directionality of the surrounding text.
-   The directionality of text embedded in `<bdi>` *is not influenced
    by* the directionality of the surrounding text.

For example, consider some text like:

``` {data-language="plain"}
EMBEDDED-TEXT - 1st place
```

If `EMBEDDED-TEXT` is LTR, this works fine. But if `EMBEDDED-TEXT` is
RTL, then `- 1` will be treated as RTL text (because it consists of
neutral and weak characters). The result will be garbled:

``` {data-language="plain"}
1 - EMBEDDED-TEXTst place
```

If you know the directionality of `EMBEDDED-TEXT` in advance, you can
fix this problem by wrapping `EMBEDDED-TEXT` in a [`<span>`](span) with
the [`dir`](../global_attributes#dir) attribute set to the known
directionality. But if you don\'t know the directionality - for example,
because `EMBEDDED-TEXT` is being read from a database or entered by the
user - you should use `<bdi>` to prevent the directionality of
`EMBEDDED-TEXT` from affecting its surroundings.

Though the same visual effect can be achieved using the CSS rule
[`unicode-bidi`](https://developer.mozilla.org/en-US/docs/Web/CSS/unicode-bidi)`: isolate`
on a [`<span>`](span) or another text-formatting element, HTML authors
should not use this approach because it is not semantic and browsers are
allowed to ignore CSS styling.

Embedding the characters in `<span dir="auto">` has the same effect as
using `<bdi>`, but its semantics are less clear.
:::

## Attributes

::: section-content
Like all other HTML elements, this element supports the [global
attributes](../global_attributes), except that the
[`dir`](../global_attributes#dir) attribute behaves differently than
normal: it defaults to `auto`, meaning its value is never inherited from
the parent element. This means that unless you specify a value of either
`rtl` or `ltr` for `dir`, the [user
agent](https://developer.mozilla.org/en-US/docs/Glossary/User_agent)
will determine the correct directionality to use based on the contents
of the `<bdi>`.
:::

## Examples

### No bdi with only LTR {#no_bdi_with_only_ltr}

::: section-content
This example lists the winners of a competition using [`<span>`](span)
elements only. When the names only contain LTR text the results look
fine:

::: code-example
[html]{.language-name}

``` {signature="73iNkMK9qFXp3QRjhWvpi4PWkSUN/c2RugYr7PwJyA0=" data-language="html"}
<ul>
  <li><span class="name">Henrietta Boffin</span> - 1st place</li>
  <li><span class="name">Jerry Cruncher</span> - 2nd place</li>
</ul>
```
:::

::: {#sect1 .code-example}
::: iframe
:::
:::
:::

### No bdi with RTL text {#no_bdi_with_rtl_text}

::: section-content
This example lists the winners of a competition using [`<span>`](span)
elements only, and one of the winners has a name consisting of RTL text.
In this case the \"`- 1`\", which consists of characters with neutral or
weak directionality, will adopt the directionality of the RTL text, and
the result will be garbled:

::: code-example
[html]{.language-name}

``` {signature="tvs5apW5E+dZ2zNiqG18Ie0kgyB71TdJq9HY6i3pBMk=" data-language="html"}
<ul>
  <li><span class="name">اَلأَعْشَى</span> - 1st place</li>
  <li><span class="name">Jerry Cruncher</span> - 2nd place</li>
</ul>
```
:::

::: {#sect2 .code-example}
::: iframe
:::
:::
:::

### Using bdi with LTR and RTL text {#using_bdi_with_ltr_and_rtl_text}

::: section-content
This example lists the winners of a competition using `<bdi>` elements.
These elements instruct the browser to treat the name in isolation from
its embedding context, so the example output is properly ordered:

::: code-example
[html]{.language-name}

``` {signature="trr15C0NOFwImByQQucSa4FUCesc++rCthXkEKU6rt0=" data-language="html"}
<ul>
  <li><bdi class="name">اَلأَعْشَى</bdi> - 1st place</li>
  <li><bdi class="name">Jerry Cruncher</bdi> - 2nd place</li>
</ul>
```
:::

::: {#sect3 .code-example}
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
<td><a href="../content_categories#phrasing_content">Phrasing
content</a>.</td>
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
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/generic_role"><code>generic</code></a></td>
</tr>
<tr class="even">
<th scope="row">Permitted ARIA roles</th>
<td>Any</td>
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

## Specifications

::: _table
  -------------------------------------------------------------------------------------------------------------
  Specification
  -------------------------------------------------------------------------------------------------------------
  [HTML Standard\
  [\#
  the-bdi-element]{.small}](https://html.spec.whatwg.org/multipage/text-level-semantics.html#the-bdi-element)

  -------------------------------------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
          Desktop                                                         Mobile                                                                                   
  ------- --------- ------ --------- ------------------- ------- -------- ----------------- ---------------- --------------------- --------------- --------------- ------------------
          Chrome    Edge   Firefox   Internet Explorer   Opera   Safari   WebView Android   Chrome Android   Firefox for Android   Opera Android   Safari on IOS   Samsung Internet
  `bdi`   16        79     10        No                  15      6        ≤37               18               10                    14              6               1.0
:::

## See also {#see_also}

::: section-content
-   [Inline markup and bidirectional text in
    HTML](https://www.w3.org/International/articles/inline-bidi-markup/){target="_blank"}
-   [Unicode Bidirectional Algorithm
    basics](https://www.w3.org/International/articles/inline-bidi-markup/uba-basics){target="_blank"}
-   [Localization](https://developer.mozilla.org/en-US/docs/Glossary/Localization)
-   Related HTML element: [`<bdo>`](bdo)
-   Related CSS properties:
    [`direction`](https://developer.mozilla.org/en-US/docs/Web/CSS/direction),
    [`unicode-bidi`](https://developer.mozilla.org/en-US/docs/Web/CSS/unicode-bidi)
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Element/bdi](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/bdi){._attribution-link}
:::
