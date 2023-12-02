

# itemid



::: section-content
The `itemid` [global attribute](../global_attributes) provides microdata
in the form of a unique, global identifier of an item.

An `itemid` attribute can only be specified for an element that has both
[`itemscope`](itemscope) and [`itemtype`](itemtype) attributes. Also,
`itemid` can only be specified on elements that possess an `itemscope`
attribute whose corresponding `itemtype` refers to or defines a
vocabulary that supports global identifiers.

The exact meaning of an `itemtype`\'s global identifier is provided by
the definition of that identifier within the specified vocabulary. The
vocabulary defines whether several items with the same global identifier
can coexist and, if so, how items with the same identifier are handled.

::: {#sect1 .notecard .note}
**Note:** The
[WHATWG](https://developer.mozilla.org/en-US/docs/Glossary/WHATWG)
definition specifies that an `itemid` must be a
[URL](https://developer.mozilla.org/en-US/docs/Glossary/URL). However,
the following example correctly illustrates that a
[URN](https://developer.mozilla.org/en-US/docs/Glossary/URN) may also be
used. This inconsistency may reflect the incomplete nature of the
Microdata specification.
:::
:::

## Examples

### Representing structured data for a book {#representing_structured_data_for_a_book}

::: section-content
This example uses microdata attributes to represent the following
structured data:

<figure class="table-container">
<div class="_table">
<table class="standard-table">
<tbody>
<tr class="odd">
<td rowspan="4">itemscope</td>
<td>itemtype: itemid</td>
<td colspan="2">https://schema.org/Book: urn:isbn:0-374-22848-5</td>
</tr>
<tr class="even">
<td>itemprop</td>
<td>title</td>
<td>Owls of the Eastern Ice</td>
</tr>
<tr class="odd">
<td>itemprop</td>
<td>author</td>
<td>Jonathan C Slaght</td>
</tr>
<tr class="even">
<td>itemprop</td>
<td>datePublished</td>
<td>2020-08-04</td>
</tr>
</tbody>
</table>

</figure>

#### HTML

::: code-example
[html]{.language-name}

``` {signature="f12VTKQeCXMR126kL8ngzeBgfzbt2oDvxayU86J8AAI=" data-language="html"}
<dl
  itemscope
  itemtype="https://schema.org/Book"
  itemid="urn:isbn:0-374-22848-5<">
  <dt>Title</dt>
  <dd itemprop="title">Owls of the Eastern Ice</dd>
  <dt>Author</dt>
  <dd itemprop="author">Jonathan C Slaght</dd>
  <dt>Publication date</dt>
  <dd>
    <time itemprop="datePublished" datetime="2020-08-04">August 4 2020</time>
  </dd>
</dl>
```
:::

#### Result

::: {#sect2 .code-example}
::: iframe
:::
:::
:::

## Specifications

::: _table
  ------------------------------------------------------------------------------------------
  Specification
  ------------------------------------------------------------------------------------------
  [HTML Standard\
  [\#
  attr-itemid]{.small}](https://html.spec.whatwg.org/multipage/microdata.html#attr-itemid)

  ------------------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
             Desktop                                                         Mobile                                                                                   
  ---------- --------- ------ --------- ------------------- ------- -------- ----------------- ---------------- --------------------- --------------- --------------- ------------------
             Chrome    Edge   Firefox   Internet Explorer   Opera   Safari   WebView Android   Chrome Android   Firefox for Android   Opera Android   Safari on IOS   Samsung Internet
  `itemid`   Yes       12     Yes       Yes                 Yes     Yes      Yes               Yes              Yes                   Yes             Yes             Yes
:::

## See also {#see_also}

::: section-content
-   All [global attributes](../global_attributes).
-   Other microdata related global attributes:
    -   [`itemprop`](itemprop)
    -   [`itemref`](itemref)
    -   [`itemscope`](itemscope)
    -   [`itemtype`](itemtype)
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/itemid](https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/itemid){._attribution-link}
:::
