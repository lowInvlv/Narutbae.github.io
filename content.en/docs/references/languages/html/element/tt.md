

# \<tt\>: The Teletype Text element



::: section-content
::: {#sect1 .notecard .deprecated}
**Deprecated:** This feature is no longer recommended. Though some
browsers might still support it, it may have already been removed from
the relevant web standards, may be in the process of being dropped, or
may only be kept for compatibility purposes. Avoid using it, and update
existing code if possible; see the [compatibility
table](#browser_compatibility) at the bottom of this page to guide your
decision. Be aware that this feature may cease to work at any time.
:::

The `<tt>` [HTML](../index) element creates inline text which is
presented using the [user
agent\'s](https://developer.mozilla.org/en-US/docs/Glossary/User_agent)
default monospace font face. This element was created for the purpose of
rendering text as it would be displayed on a fixed-width display such as
a teletype, text-only screen, or line printer.

The terms **non-proportional**, **monotype**, and **monospace** are used
interchangeably and have the same general meaning: they describe a
typeface whose characters are all the same number of pixels wide.

This element is obsolete, however. You should use the more semantically
helpful [`<code>`](code), [`<kbd>`](kbd), [`<samp>`](samp), or
[`<var>`](var) elements for inline text that needs to be presented in
monospace type, or the [`<pre>`](pre) tag for content that should be
presented as a separate block.

::: {#sect2 .notecard .note}
**Note:** If none of the semantic elements are appropriate for your use
case (for example, if you need to show some content in a
non-proportional font), you should consider using the [`<span>`](span)
element, styling it as desired using CSS. The
[`font-family`](https://developer.mozilla.org/en-US/docs/Web/CSS/font-family)
property is a good place to start.
:::
:::

## Attributes

::: section-content
This element only includes the [global attributes](../global_attributes)
:::

## Examples

### Basic example {#basic_example}

::: section-content
This example uses `<tt>` to show text entered into, and output by, a
terminal application.

::: code-example
[html]{.language-name}

``` {signature="SkOBCEMA/Pl5YLzCZfhZpLwNeBgY+a6f+9wfcJkafM4=" data-language="html"}
<p>
  Enter the following at the telnet command prompt:
  <code>set localecho</code><br />

  The telnet client should display: <tt>Local Echo is on</tt>
</p>
```
:::

#### Result

::: {#sect3 .code-example}
::: iframe
:::
:::
:::

### Overriding the default font {#overriding_the_default_font}

::: section-content
You can override the browser\'s default font---if the browser permits
you to do so, which it isn\'t required to do---using CSS:

#### CSS

::: code-example
[css]{.language-name}

``` {signature="A4r8jLJpokBOYbHBlvFZi1RqVieAqeAPH8cmKZa/npU=" data-language="css"}
tt {
  font-family: "Lucida Console", "Menlo", "Monaco", "Courier", monospace;
}
```
:::

#### HTML

::: code-example
[html]{.language-name}

``` {signature="SkOBCEMA/Pl5YLzCZfhZpLwNeBgY+a6f+9wfcJkafM4=" data-language="html"}
<p>
  Enter the following at the telnet command prompt:
  <code>set localecho</code><br />

  The telnet client should display: <tt>Local Echo is on</tt>
</p>
```
:::

#### Result {#result_2}

::: {#sect4 .code-example}
::: iframe
:::
:::
:::

## Usage notes {#usage_notes}

::: section-content
The `<tt>` element is, by default, rendered using the browser\'s default
non-proportional font. You can override this using CSS by creating a
rule using the `tt` selector, as seen in the example [Overriding the
default font](#overriding_the_default_font) above.

::: {#sect5 .notecard .note}
**Note:** User-configured changes to the default monospace font setting
may take precedence over your CSS.
:::

Although this element wasn\'t officially deprecated in HTML 4.01, its
use was discouraged in favor of the semantic elements and/or CSS. The
`<tt>` element is obsolete in HTML 5.
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
<th scope="row">Permitted ARIA roles</th>
<td>Any</td>
</tr>
<tr class="even">
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
  -----------------------------------------------------------------------
  Specification
  -----------------------------------------------------------------------
  [HTML Standard\
  [\#
  tt]{.small}](https://html.spec.whatwg.org/multipage/obsolete.html#tt)

  -----------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
  ---------------------------------------------------------------------------------------------------------------------------------------------
         Desktop                                                          Mobile                                                     
  ------ --------- ------ ------------------- ---------- ------- -------- --------- --------- ------------------- --------- -------- ----------
         Chrome    Edge   Firefox             Internet   Opera   Safari   WebView   Chrome    Firefox for Android Opera     Safari   Samsung
                                              Explorer                    Android   Android                       Android   on IOS   Internet

  `tt`   1         12     1                   Yes        15      ≤4       4.4       18        4                   14        ≤3.2     1.0
                                                                                                                                     
                          Before Firefox 4,                                                   Before Firefox 4,                      
                          this element                                                        this element                           
                          implemented the                                                     implemented the                        
                          `HTMLSpanElement`                                                   `HTMLSpanElement`                      
                          interface instead                                                   interface instead                      
                          of the standard                                                     of the standard                        
                          `HTMLElement`                                                       `HTMLElement`                          
                          interface.                                                          interface.                             
  ---------------------------------------------------------------------------------------------------------------------------------------------
:::

## See also {#see_also}

::: section-content
-   The semantic [`<code>`](code), [`<var>`](var), [`<kbd>`](kbd), and
    [`<samp>`](samp) elements
-   The [`<pre>`](pre) element for displaying preformatted text blocks
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Element/tt](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/tt){._attribution-link}
:::
