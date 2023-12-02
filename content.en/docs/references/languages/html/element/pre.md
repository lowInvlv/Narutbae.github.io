

# \<pre\>: The Preformatted Text element



::: section-content
The `<pre>` [HTML](../index) element represents preformatted text which
is to be presented exactly as written in the HTML file. The text is
typically rendered using a non-proportional, or
[monospaced](https://en.wikipedia.org/wiki/Monospaced_font){target="_blank"},
font. Whitespace inside this element is displayed as written.
:::

## Try it {#try_it}

::: section-content
::: iframe
::: {.output-header .border-rounded-top}
#### HTML Demo: \<pre\> {#html-demo-pre .output-heading}

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
    <pre>
      L          TE
        A       A
          C    V
           R A
           DOU
           LOU
          REUSE
          QUE TU
          PORTES
        ET QUI T'
        ORNE O CI
         VILISÉ
        OTE-  TU VEUX
         LA    BIEN
        SI      RESPI
                RER       - Apollinaire
    </pre>
:::
:::

::: {#css-panel .section .hidden tabindex="0" role="tabpanel" aria-labelledby="css" aria-hidden="true"}
::: {#css-editor}
    pre {
      font-size: 0.7rem;
      margin: 0;
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

If you have to display reserved characters such as `<`, `>`, `&`, and
`"` within the `<pre>` tag, the characters must be escaped using their
respective [HTML
entity](https://developer.mozilla.org/en-US/docs/Glossary/Entity).
:::

## Attributes

::: section-content
This element only includes the [global
attributes](../global_attributes).

[`cols`](#cols) [Non-standard]{.visually-hidden} [Deprecated]{.visually-hidden}

:   Contains the *preferred* count of characters that a line should
    have. It was a non-standard synonym of [`width`](#width). To achieve
    such an effect, use CSS
    [`width`](https://developer.mozilla.org/en-US/docs/Web/CSS/width)
    instead.

[`width`](#width) [Deprecated]{.visually-hidden} [Non-standard]{.visually-hidden}

:   Contains the *preferred* count of characters that a line should
    have. Though technically still implemented, this attribute has no
    visual effect; to achieve such an effect, use CSS
    [`width`](https://developer.mozilla.org/en-US/docs/Web/CSS/width)
    instead.

[`wrap`](#wrap) [Non-standard]{.visually-hidden} [Deprecated]{.visually-hidden}

:   Is a *hint* indicating how the overflow must happen. In modern
    browser this hint is ignored and no visual effect results in its
    present; to achieve such an effect, use CSS
    [`white-space`](https://developer.mozilla.org/en-US/docs/Web/CSS/white-space)
    instead.
:::

## Accessibility concerns {#accessibility_concerns}

::: section-content
It is important to provide an alternate description for any images or
diagrams created using preformatted text. The alternate description
should clearly and concisely describe the image or diagram\'s content.

People experiencing low vision conditions and browsing with the aid of
assistive technology such as a screen reader may not understand what the
preformatted text characters are representing when they are read out in
sequence.

A combination of the [`<figure>`](figure) and
[`<figcaption>`](figcaption) elements, supplemented by the
[ARIA](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA)
`role` and
[`aria-label`](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Attributes/aria-label)
attributes on the `pre` element allow the preformatted
[ASCII](https://developer.mozilla.org/en-US/docs/Glossary/ASCII) art to
be announced as an image with alternative text, and the `figcaption`
serving as the image\'s caption.
:::

### Example

::: section-content
::: code-example
[html]{.language-name}

``` {signature="B5YQB9OgIEPWVPXxsTuXL2miUqASlopw2LLCKbutcpc=" data-language="html"}
<figure>
  <pre role="img" aria-label="ASCII COW">
      ___________________________
  &lt; I'm an expert in my field. &gt;
      ---------------------------
          \   ^__^
           \  (oo)\_______
              (__)\       )\/\
                  ||----w |
                  ||     ||
  </pre>
  <figcaption id="cow-caption">
    A cow saying, "I'm an expert in my field." The cow is illustrated using
    preformatted text characters.
  </figcaption>
</figure>
```
:::

-   [MDN Understanding WCAG, Guideline 1.1
    explanations](https://developer.mozilla.org/en-US/docs/Web/Accessibility/Understanding_WCAG/Perceivable#guideline_1.1_%E2%80%94_providing_text_alternatives_for_non-text_content)
-   [H86: Providing text alternatives for ASCII art, emoticons, and
    leetspeak \| W3C Techniques for WCAG
    2.0](https://www.w3.org/TR/WCAG20-TECHS/H86.html){target="_blank"}
:::

## Examples

### Basic example {#basic_example}

::: section-content
#### HTML

::: code-example
[html]{.language-name}

``` {signature="iIQd1jZopQJdpu+WHzSH6n5jyMjDI5+WBXiveyKwjEk=" data-language="html"}
<p>Using CSS to change the font color is easy.</p>
<pre>
body {
  color: red;
}
</pre>
```
:::

#### Result

::: {#sect1 .code-example}
::: iframe
:::
:::
:::

### Escaping reserved characters {#escaping_reserved_characters}

::: section-content
#### HTML {#html_2}

::: code-example
[html]{.language-name}

``` {signature="6tKQNA302zYigID+/jL3rLMNftHbaURc1QMq1nXNeOc=" data-language="html"}
<pre>
let i = 5;

if (i &lt; 10 &amp;&amp; i &gt; 0)
  return &quot;Single Digit Number&quot;
</pre>
```
:::

#### Result {#result_2}

::: {#sect2 .code-example}
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
<td><a href="../content_categories#flow_content">Flow content</a>,
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
href="../content_categories#flow_content">flow content</a>.</td>
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
href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLPreElement"><code>HTMLPreElement</code></a></td>
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
  the-pre-element]{.small}](https://html.spec.whatwg.org/multipage/grouping-content.html#the-pre-element)

  ---------------------------------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
  ---------------------------------------------------------------------------------------------------------------------------------------------------------------------
            Desktop                                                                       Mobile                                                           
  --------- ------------ ------------ ------------ ------------ ------------ ------------ ------------ ------------ ------------ ------------ ------------ ------------
            Chrome       Edge         Firefox      Internet     Opera        Safari       WebView      Chrome       Firefox for  Opera        Safari on    Samsung
                                                   Explorer                               Android      Android      Android      Android      IOS          Internet

  `pre`     1            12           1            Yes          15           ≤4           4.4          18           4            14           ≤3.2         1.0

  `cols`    No           No           1--29        No           No           No           No           No           4--29        No           No           No

  `width`   1            12           1            Yes          15           3            4.4          18           4            14           2            1.0
                                                                                                                                                           
            Specifying   Specifying   Since        Specifying   Specifying   Specifying   Specifying   Specifying   Since        Specifying   Specifying   Specifying
            the `width`  the `width`  Firefox 29,  the `width`  the `width`  the `width`  the `width`  the `width`  Firefox 29,  the `width`  the `width`  the `width`
            attribute    attribute    specifying   attribute    attribute    attribute    attribute    attribute    specifying   attribute    attribute    attribute
            has no       has no       the `width`  has no       has no       has no       has no       has no       the `width`  has no       has no       has no
            layout       layout       attribute    layout       layout       layout       layout       layout       attribute    layout       layout       layout
            effect.      effect.      has no       effect.      effect.      effect.      effect.      effect.      has no       effect.      effect.      effect.
                                      layout                                                                        layout                                 
                                      effect.                                                                       effect.                                

  `wrap`    16           79           1            No           15           6            4.4          18           4            14           6            1.0
  ---------------------------------------------------------------------------------------------------------------------------------------------------------------------
:::

## See also {#see_also}

::: section-content
-   CSS:
    [`white-space`](https://developer.mozilla.org/en-US/docs/Web/CSS/white-space),
    [`word-break`](https://developer.mozilla.org/en-US/docs/Web/CSS/word-break)
-   [HTML
    Entity](https://developer.mozilla.org/en-US/docs/Glossary/Entity)
-   Related element: [`<code>`](code)
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Element/pre](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/pre){._attribution-link}
:::
