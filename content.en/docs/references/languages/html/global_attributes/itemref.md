

# itemref



::: section-content
Properties that are not descendants of an element with the
[`itemscope`](itemscope) attribute can be associated with an item using
the [global attribute](../global_attributes) `itemref`.

`itemref` provides a list of element IDs (not `itemid`s) elsewhere in
the document, with additional properties

The `itemref` attribute can only be specified on elements that have an
`itemscope` attribute specified.

::: {#sect1 .notecard .note}
**Note:** The `itemref` attribute is not part of the microdata data
model. It is merely a syntactic construct to aid authors in adding
annotations to pages where the data to be annotated does not follow a
convenient tree structure. For example, it allows authors to mark up
data in a table so that each column defines a separate item while
keeping the properties in the cells.
:::
:::

## Examples

### Representing structured data for a band {#representing_structured_data_for_a_band}

::: section-content
This example uses microdata attributes to represent the following
structured data (in [JSON-LD](https://json-ld.org/){target="_blank"}
format):

::: code-example
[json]{.language-name}

``` {signature="5jNQMtf3O3MRZQx7fZ9yYG5u9+qWyZHWHMU1biaoWz0=" data-language="json"}
{
  "@id": "amanda",
  "name": "Amanda",
  "band": {
    "@id": "b",
    "name": "Jazz Band",
    "size": 12
  }
}
```
:::

#### HTML

::: code-example
[html]{.language-name}

``` {signature="EBplAOAbZOTJ5Lh3KSWI2ONHEuuszvP29DjQ2DF8giI=" data-language="html"}
<div itemscope id="amanda" itemref="a b">
<p id="a">Name: <span itemprop="name">Amanda</span></p>
<div id="b" itemprop="band" itemscope itemref="c">
<div id="c">
  <p>Band: <span itemprop="name">Jazz Band</span></p>
  <p>Size: <span itemprop="size">12</span> players</p>

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
  --------------------------------------------------------------------------------------------
  Specification
  --------------------------------------------------------------------------------------------
  [HTML Standard\
  [\#
  attr-itemref]{.small}](https://html.spec.whatwg.org/multipage/microdata.html#attr-itemref)

  --------------------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
              Desktop                                                         Mobile                                                                                   
  ----------- --------- ------ --------- ------------------- ------- -------- ----------------- ---------------- --------------------- --------------- --------------- ------------------
              Chrome    Edge   Firefox   Internet Explorer   Opera   Safari   WebView Android   Chrome Android   Firefox for Android   Opera Android   Safari on IOS   Samsung Internet
  `itemref`   Yes       12     Yes       Yes                 Yes     Yes      Yes               Yes              Yes                   Yes             Yes             Yes
:::

## See also {#see_also}

::: section-content
-   [Other different global attributes](../global_attributes)
-   Other microdata related global attributes:
    -   [`itemid`](itemid)
    -   [`itemprop`](itemprop)
    -   [`itemscope`](itemscope)
    -   [`itemtype`](itemtype)
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/itemref](https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/itemref){._attribution-link}
:::
