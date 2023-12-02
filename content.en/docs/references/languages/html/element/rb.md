

# \<rb\>: The Ruby Base element



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

The `<rb>` [HTML](../index) element is used to delimit the base text
component of a [`<ruby>`](ruby) annotation, i.e. the text that is being
annotated. One `<rb>` element should wrap each separate atomic segment
of the base text.
:::

## Attributes

::: section-content
This element only includes the [global
attributes](../global_attributes).
:::

## Usage notes {#usage_notes}

::: section-content
-   Ruby annotations are for showing pronunciation of East Asian
    characters, like using Japanese furigana or Taiwanese bopomofo
    characters. The `<rb>` element is used to separate out each segment
    of the ruby base text.
-   Even though `<rb>` is not a [void
    element](https://developer.mozilla.org/en-US/docs/Glossary/Void_element),
    it is common to just include the opening tag of each element in the
    source code, so that the ruby markup is less complex and easier to
    read. The browser can then fill in the full element in the rendered
    version.
-   You need to include one [`<rt>`](rt) element for each base
    segment/`<rb>` element that you want to annotate.
:::

## Examples

### Using rb {#using_rb}

::: section-content
In this example, we provide an annotation for the original character
equivalent of \"Kanji\":

::: code-example
[html]{.language-name}

``` {signature="6okhRiocfiWkPkX6HnFhYov0ZspFaOZmHPeNVDVt8kM=" data-language="html"}
<ruby>
  <rb>漢</rb><rb>字 </rb><rp>(</rp><rt>kan</rt><rt>ji</rt><rp>)</rp>
</ruby>
```
:::

Note how we\'ve included two `<rb>` elements, to delimit the two
separate parts of the ruby base text. The annotation on the other hand
is delimited by two [`<rt>`](rt) elements.

#### Result

::: {#sect2 .code-example}
::: iframe
:::
:::
:::

### Separate annotations {#separate_annotations}

::: section-content
Note that we could also write this example with the two base text parts
annotated completely separately. In this case we don\'t need to include
`<rb>` elements:

::: code-example
[html]{.language-name}

``` {signature="Y+5q/G3EBi/ofswS5LfyI/FrJgypPFnlRQxpSurHYlA=" data-language="html"}
<ruby>
  漢 <rp>(</rp><rt>Kan</rt><rp>)</rp> 字 <rp>(</rp><rt>ji</rt><rp>)</rp>
</ruby>
```
:::

#### Result {#result_2}

::: {#sect3 .code-example}
::: iframe
:::
:::

See the article about the [`<ruby>`](ruby) element for further examples.
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
<td>None.</td>
</tr>
<tr class="even">
<th scope="row">Permitted content</th>
<td>As a child of a <a href="ruby"><code>&lt;ruby&gt;</code></a>
element.</td>
</tr>
<tr class="odd">
<th scope="row">Tag omission</th>
<td>The end tag can be omitted if the element is immediately followed by
an <a href="rt"><code>&lt;rt&gt;</code></a>, <a
href="rtc"><code>&lt;rtc&gt;</code></a>, or <a
href="rp"><code>&lt;rp&gt;</code></a> element or another
<code>&lt;rb&gt;</code> element, or if there is no more content in the
parent element.</td>
</tr>
<tr class="even">
<th scope="row">Permitted parents</th>
<td>A <a href="ruby"><code>&lt;ruby&gt;</code></a> element.</td>
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
  rb]{.small}](https://html.spec.whatwg.org/multipage/obsolete.html#rb)

  -----------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
  -------------------------------------------------------------------------------------------------------------------------------------------------
         Desktop                                                              Mobile                                                    
  ------ ----------- ----------- --------- ---------- ----------- ----------- ----------- ----------- --------- ----------- ----------- -----------
         Chrome      Edge        Firefox   Internet   Opera       Safari      WebView     Chrome      Firefox   Opera       Safari on   Samsung
                                           Explorer                           Android     Android     for       Android     IOS         Internet
                                                                                                      Android                           

  `rb`   5           79          38        5          15          5           4.4         18          38        14          4.2         1.0
                                                                                                                                        
         Blink has   Blink has                        Blink has   Safari has  Blink has   Blink has             Blink has   Safari has  Blink has
         support for support for                      support for support for support for support for           support for support for support for
         parsing the parsing the                      parsing the parsing the parsing the parsing the           parsing the parsing the parsing the
         `rb`        `rb`                             `rb`        `rb`        `rb`        `rb`                  `rb`        `rb`        `rb`
         element,    element,                         element,    element,    element,    element,              element,    element,    element,
         but not for but not for                      but not for but not for but not for but not for           but not for but not for but not for
         rendering   rendering                        rendering   rendering   rendering   rendering             rendering   rendering   rendering
         `rb`        `rb`                             `rb`        `rb`        `rb`        `rb`                  `rb`        `rb`        `rb`
         content as  content as                       content as  content as  content as  content as            content as  content as  content as
         expected.   expected.                        expected.   expected.   expected.   expected.             expected.   expected.   expected.
  -------------------------------------------------------------------------------------------------------------------------------------------------
:::

## See also {#see_also}

::: section-content
-   [`<ruby>`](ruby)
-   [`<rt>`](rt)
-   [`<rp>`](rp)
-   [`<rtc>`](rtc)
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Element/rb](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/rb){._attribution-link}
:::
