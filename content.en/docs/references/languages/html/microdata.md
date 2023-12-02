

# Microdata



::: section-content
Microdata is part of the
[WHATWG](https://developer.mozilla.org/en-US/docs/Glossary/WHATWG) HTML
Standard and is used to nest metadata within existing content on web
pages. Search engines and web crawlers can extract and process microdata
from a web page and use it to provide a richer browsing experience for
users. Search engines benefit greatly from direct access to this
structured data because it allows search engines to understand the
information on web pages and provide more relevant results to users.
Microdata uses a supporting vocabulary to describe an item and
name-value pairs to assign values to its properties. Microdata is an
attempt to provide a simpler way of annotating HTML elements with
machine-readable tags than the similar approaches of using RDFa and
classic microformats.

At a high level, microdata consists of a group of name-value pairs. The
groups are called items, and each name-value pair is a property. Items
and properties are represented by regular elements.

-   To create an item, the `itemscope` attribute is used.
-   To add a property to an item, the `itemprop` attribute is used on
    one of the item\'s descendants.
:::

## Vocabularies

::: section-content
Google and other major search engines support the
[Schema.org](https://schema.org){target="_blank"} vocabulary for
structured data. This vocabulary defines a standard set of type names
and property names, for example, [Schema.org Music
Event](https://schema.org/MusicEvent){target="_blank"} indicates a
concert performance, with
[`startDate`](https://schema.org/startDate){target="_blank"} and
[`location`](https://schema.org/location){target="_blank"} properties to
specify the concert\'s key details. In this case, [Schema.org Music
Event](https://schema.org/MusicEvent){target="_blank"} would be the URL
used by `itemtype` and `startDate` and location would be `itemprop`\'s
that [Schema.org Music
Event](https://schema.org/MusicEvent){target="_blank"} defines.

::: {#sect1 .notecard .note}
**Note:** More about itemtype attributes can be found at
[https://schema.org/Thing](https://schema.org/Thing){target="_blank"}.
:::

Microdata vocabularies provide the semantics or meaning of an *`Item`*.
Web developers can design a custom vocabulary or use vocabularies
available on the web, such as the widely used
[schema.org](https://schema.org){target="_blank"} vocabulary. A
collection of commonly used markup vocabularies are provided by
Schema.org.

Commonly used vocabularies:

-   Creative works:
    [CreativeWork](https://schema.org/CreativeWork){target="_blank"},
    [Book](https://schema.org/Book){target="_blank"},
    [Movie](https://schema.org/Movie){target="_blank"},
    [MusicRecording](https://schema.org/MusicRecording){target="_blank"},
    [Recipe](https://schema.org/Recipe){target="_blank"},
    [TVSeries](https://schema.org/TVSeries){target="_blank"}
-   Embedded non-text objects:
    [AudioObject](https://schema.org/AudioObject){target="_blank"},
    [ImageObject](https://schema.org/ImageObject){target="_blank"},
    [VideoObject](https://schema.org/VideoObject){target="_blank"}
-   [`Event`](https://schema.org/Event){target="_blank"}
-   [Health and medical
    types](https://schema.org/docs/meddocs.html){target="_blank"}: Notes
    on the health and medical types under
    [MedicalEntity](https://schema.org/MedicalEntity){target="_blank"}
-   [`Organization`](https://schema.org/Organization){target="_blank"}
-   [`Person`](https://schema.org/Person){target="_blank"}
-   [`Place`](https://schema.org/Place){target="_blank"},
    [LocalBusiness](https://schema.org/LocalBusiness){target="_blank"},
    [Restaurant](https://schema.org/Restaurant){target="_blank"}
-   [`Product`](https://schema.org/Product){target="_blank"},
    [Offer](https://schema.org/Offer){target="_blank"},
    [AggregateOffer](https://schema.org/AggregateOffer){target="_blank"}
-   [`Review`](https://schema.org/Review){target="_blank"},
    [AggregateRating](https://schema.org/AggregateRating){target="_blank"}
-   [`Action`](https://schema.org/Action){target="_blank"}
-   [`Thing`](https://schema.org/Thing){target="_blank"}
-   [`Intangible`](https://schema.org/Intangible){target="_blank"}

Major search engine operators like Google, Microsoft, and Yahoo! rely on
the [schema.org](https://schema.org/){target="_blank"} vocabulary to
improve search results. For some purposes, an ad hoc vocabulary is
adequate. For others, a vocabulary will need to be designed. Where
possible, authors are encouraged to re-use existing vocabularies, as
this makes content re-use easier.
:::

## Localization

::: section-content
In some cases, search engines covering specific regions may provide
locally-specific extensions of microdata. For example,
[Yandex](https://yandex.com/){target="_blank"}, a major search engine in
Russia, supports microformats such as `hCard` (company contact
information), `hRecipe` (food recipe), `hReview` (market reviews) and
`hProduct` (product data) and provides its own format for the definition
of the terms and encyclopedic articles. This extension was made to solve
transliteration problems between the Cyrillic and Latin alphabets. Due
to the implementation of additional marking parameters of Schema\'s
vocabulary, the indexation of information in Russian-language web-pages
became considerably more successful.
:::

## Global attributes {#global_attributes}

::: section-content
[`itemid`](global_attributes/itemid) -- The unique, global identifier of
an item.

[`itemprop`](global_attributes/itemprop) -- Used to add properties to an
item. Every HTML element may have an `itemprop` attribute specified,
where an `itemprop` consists of a name and value pair.

[`itemref`](global_attributes/itemref) -- Properties that are not
descendants of an element with the `itemscope` attribute can be
associated with the item using an **itemref**. `itemref` provides a list
of element ids (not `itemid`s) with additional properties elsewhere in
the document.

[`itemscope`](global_attributes/itemscope) -- The `itemscope` attribute
(usually) works along with [`itemtype`](global_attributes/itemtype) to
specify that the HTML contained in a block is about a particular item.
The `itemscope` attribute creates the *`Item`* and defines the scope of
the itemtype associated with it. The `itemtype` attribute is a valid URL
of a vocabulary (such as
[schema.org](https://schema.org/){target="_blank"}) that describes the
item and its properties context.

[`itemtype`](global_attributes/itemtype) -- Specifies the URL of the
vocabulary that will be used to define `itemprop`\'s (item properties)
in the data structure. The [`itemscope`](global_attributes/itemscope)
attribute is used to set the scope of where in the data structure the
vocabulary set by `itemtype` will be active.
:::

## Example

### HTML

::: section-content
::: code-example
[html]{.language-name}

``` {signature="Ai8NwsrfDCmuLxRS+UVZfScghNaShUWGeBEb5Ltc+Ow=" data-language="html"}
<div itemscope itemtype="https://schema.org/SoftwareApplication">
  <span itemprop="name">Angry Birds</span> - REQUIRES
  <span itemprop="operatingSystem">ANDROID</span><br />
  <link
    itemprop="applicationCategory"
    href="https://schema.org/GameApplication" />

  <div
    itemprop="aggregateRating"
    itemscope
    itemtype="https://schema.org/AggregateRating">
    RATING:
    <span itemprop="ratingValue">4.6</span> (
    <span itemprop="ratingCount">8864</span> ratings )
  

  <div itemprop="offers" itemscope itemtype="https://schema.org/Offer">
    Price: $<span itemprop="price">1.00</span>
    <meta itemprop="priceCurrency" content="USD" />
  

```
:::
:::

### Structured data {#structured_data}

::: section-content
<figure class="table-container">
<div class="_table">
<table class="standard-table">
<tbody>
<tr class="odd">
<td rowspan="4">itemscope</td>
<td>itemtype</td>
<td colspan="2">SoftwareApplication
(https://schema.org/SoftwareApplication)</td>
</tr>
<tr class="even">
<td>itemprop</td>
<td>name</td>
<td>Angry Birds</td>
</tr>
<tr class="odd">
<td>itemprop</td>
<td>operatingSystem</td>
<td>ANDROID</td>
</tr>
<tr class="even">
<td>itemprop</td>
<td>applicationCategory</td>
<td>GameApplication (https://schema.org/GameApplication)</td>
</tr>
<tr class="odd">
<td rowspan="3">itemscope</td>
<td>itemprop[itemtype]</td>
<td colspan="2">aggregateRating [AggregateRating]</td>
</tr>
<tr class="even">
<td>itemprop</td>
<td>ratingValue</td>
<td>4.6</td>
</tr>
<tr class="odd">
<td>itemprop</td>
<td>ratingCount</td>
<td>8864</td>
</tr>
<tr class="even">
<td rowspan="3">itemscope</td>
<td>itemprop[itemtype]</td>
<td colspan="2">offers [Offer]</td>
</tr>
<tr class="odd">
<td>itemprop</td>
<td>price</td>
<td>1.00</td>
</tr>
<tr class="even">
<td>itemprop</td>
<td>priceCurrency</td>
<td>USD</td>
</tr>
</tbody>
</table>

</figure>
:::

### Result

::: section-content
::: {#sect2 .code-example}
::: iframe
:::
:::

::: {#sect3 .notecard .note}
**Note:** A handy tool for extracting microdata structures from HTML is
Google\'s [Structured Data Testing
Tool](https://developers.google.com/search/docs/advanced/structured-data/intro-structured-data){target="_blank"}.
Try it on the HTML shown above.
:::
:::

## Browser compatibility {#browser_compatibility}

::: section-content
Supported in Firefox 16. Removed in Firefox 49.
:::

## See also {#see_also}

::: section-content
-   [Global Attributes](global_attributes)
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Microdata](https://developer.mozilla.org/en-US/docs/Web/HTML/Microdata){._attribution-link}
:::
