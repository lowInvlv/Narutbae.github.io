

# itemprop



::: section-content
The `itemprop` [global attribute](../global_attributes) is used to add
properties to an item. Every HTML element can have an `itemprop`
attribute specified, and an `itemprop` consists of a name-value pair.
Each name-value pair is called a **property**, and a group of one or
more properties forms an **item**. Property values are either a string
or a URL and can be associated with a very wide range of elements
including [`<audio>`](../element/audio), [`<embed>`](../element/embed),
[`<iframe>`](../element/iframe), [`<img>`](../element/img),
[`<link>`](../element/link), [`<object>`](../element/object),
[`<source>`](../element/source), [`<track>`](../element/track), and
[`<video>`](../element/video).
:::

## Examples

::: section-content
The example below shows the source for a set of elements marked up with
`itemprop` attributes, followed by a table showing the resulting
structured data.
:::

### HTML

::: section-content
::: code-example
[html]{.language-name}

``` {signature="4fuEhewfYMp+3G7M8XVB6uclEuXkZu9JMHb8FeS6W7Y=" data-language="html"}
<div itemscope itemtype="http://schema.org/Movie">
  <h1 itemprop="name">Avatar</h1>
  <span>
    Director:
    <span itemprop="director">James Cameron</span>
    (born August 16, 1954)
  </span>
  <span itemprop="genre">Science fiction</span>
  <a href="../movies/avatar-theatrical-trailer.html" itemprop="trailer">
    Trailer
  </a>

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
<td rowspan="2"></td>
<td colspan="2"><strong>Item</strong></td>
</tr>
<tr class="even">
<td><strong>itemprop name</strong></td>
<td><strong>itemprop value</strong></td>
</tr>
<tr class="odd">
<td>itemprop</td>
<td>name</td>
<td>Avatar</td>
</tr>
<tr class="even">
<td>itemprop</td>
<td>director</td>
<td>James Cameron</td>
</tr>
<tr class="odd">
<td>itemprop</td>
<td>genre</td>
<td>Science fiction</td>
</tr>
<tr class="even">
<td>itemprop</td>
<td>trailer</td>
<td>../movies/avatar-theatrical-trailer.html</td>
</tr>
</tbody>
</table>

</figure>
:::

## Properties

::: section-content
Properties have values that are either a string or a URL. When a string
value is a URL, it is expressed using the [`<a>`](../element/a) element
and its [`href`](../element/a#href) attribute, the
[`<img>`](../element/img) element and its [`src`](../element/img#src)
attribute, or other elements that link to or embed external resources.
:::

### Three properties with values that are strings {#three_properties_with_values_that_are_strings}

::: section-content
::: code-example
[html]{.language-name}

``` {signature="7CpSR2jQhdqT8T1cVJbFJuqi3EjPdT+65hjcTxoGvao=" data-language="html"}
<div itemscope>
  <p>My name is <span itemprop="name">Neil</span>.</p>
  <p>My band is called <span itemprop="band">Four Parts Water</span>.</p>
  <p>I am <span itemprop="nationality">British</span>.</p>

```
:::
:::

### One property, \"image\", whose value is a URL {#one_property_image_whose_value_is_a_url}

::: section-content
::: code-example
[html]{.language-name}

``` {signature="VMW0F1UxX+d/26dePnZsAR56t+VujRwCg7jESb5ku6A=" data-language="html"}
<div itemscope>
  <img itemprop="image" src="google-logo.png" alt="Google" />

```
:::

When a string value can\'t be easily read and understood by a person
(e.g., a long string of numbers and letters), it can be displayed using
the value attribute of the data element, with the more
easily-understood-by-a human-version given in the element\'s contents
(which is not part of the structured data - see example below).
:::

### An item with a property whose value is a product ID {#an_item_with_a_property_whose_value_is_a_product_id}

::: section-content
The ID is not human-friendly, so the product\'s name is used instead.

::: code-example
[html]{.language-name}

``` {signature="BRvMnyrFG+L13D1acTXYX/N/kFoy2hI+jZaLy62RSUY=" data-language="html"}
<h1 itemscope>
  <data itemprop="product-id" value="9678AOU879">The Instigator 2000</data>
</h1>
```
:::

For numeric data, the meter element and its value attribute can be used.
:::

### A meter element {#a_meter_element}

::: section-content
::: code-example
[html]{.language-name}

``` {signature="An1ZhPBlng5iXkcIm2kTsBw9TeDmAr75137WES5DWlA=" data-language="html"}
<div itemscope itemtype="http://schema.org/Product">
  <span itemprop="name">Panasonic White 60L Refrigerator</span>
  <img src="panasonic-fridge-60l-white.jpg" alt="" />
  <div
    itemprop="aggregateRating"
    itemscope
    itemtype="http://schema.org/AggregateRating">
    <meter itemprop="ratingValue" min="0" value="3.5" max="5">
      Rated 3.5/5
    </meter>
    (based on <span itemprop="reviewCount">11</span>
    customer reviews)
  

```
:::

Similarly, for date- and time-related data, the time element and its
datetime attribute can be used.
:::

### An item with one property, \"birthday\", whose value is a date {#an_item_with_one_property_birthday_whose_value_is_a_date}

::: section-content
::: code-example
[html]{.language-name}

``` {signature="DhjGMgjX0HCrnaEbQrOYT1Iot1KZvXbbCXxfN+4VuBo=" data-language="html"}
<div itemscope>
  I was born on
  <time itemprop="birthday" datetime="1984-05-10">May 10th 1984</time>.

```
:::

Properties can also be groups of name-value pairs, by putting the
itemscope attribute on the element that declares the property. Each
value is either a string or a group of name-value pairs (i.e. an item).
:::

### An outer item representing a person, and an inner one representing a band {#an_outer_item_representing_a_person_and_an_inner_one_representing_a_band}

::: section-content
::: code-example
[html]{.language-name}

``` {signature="Y2XVKZR1OjKcoOBOcB+g+xl51P48HpA0MpXuGI+pizU=" data-language="html"}
<div itemscope>
  <p>Name: <span itemprop="name">Amanda</span></p>
  <p>
    Band:
    <span itemprop="band" itemscope>
      <span itemprop="name">Jazz Band</span>
      (<span itemprop="size">12</span> players)
    </span>
  </p>

```
:::

The outer item above has two properties, \"name\" and \"band\". The
\"name\" is \"Amanda\", and the \"band\" is an item in its own right,
with two properties, \"name\" and \"size\". The \"name\" of the band is
\"Jazz Band\", and the \"size\" is \"12\". The outer item in this
example is a top-level microdata item. Items that are not part of others
are called top-level microdata items.
:::

### All the properties separated from their items {#all_the_properties_separated_from_their_items}

::: section-content
This example is the same as the previous one, but all the properties are
separated from their items.

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

This gives the same result as the previous example. The first item has
two properties, \"name\", set to \"Amanda\", and \"band\", set to
another item. That second item has two further properties, \"name\", set
to \"Jazz Band\", and \"size\", set to \"12\".

An item can have multiple properties with the same name and different
values.
:::

### Ice cream with two flavors {#ice_cream_with_two_flavors}

::: section-content
::: code-example
[html]{.language-name}

``` {signature="qYOFkSpFyZhIskxvtcVszptf3YtWQuLmTxecvh29mdU=" data-language="html"}
<div itemscope>
  <p>Flavors in my favorite ice cream:</p>
  <ul>
    <li itemprop="flavor">Lemon sorbet</li>
    <li itemprop="flavor">Apricot sorbet</li>
  </ul>

```
:::

This results in an item with two properties, both with the name
\"flavor\" and having the values \"Lemon sorbet\" and \"Apricot
sorbet\".

An element introducing a property can also introduce multiple properties
at once, to avoid duplication when some of the properties have the same
value.
:::

### An item with two properties, \"favorite-color\" and \"favorite-fruit\", both set to the value \"orange\" {#an_item_with_two_properties_favorite-color_and_favorite-fruit_both_set_to_the_value_orange}

::: section-content
::: code-example
[html]{.language-name}

``` {signature="dmOoDllG+lhLl6KHvWbk37PxXpcRVbehXXfkQa7tpbc=" data-language="html"}
<div itemscope>
  <span
    itemprop="favorite-color
    favorite-fruit"
    >orange
  </span>

```
:::

::: {#sect1 .notecard .note}
**Note:** There is no relationship between the microdata and the content
of the document where the microdata is marked up.
:::
:::

### Same structured data marked up in two different ways {#same_structured_data_marked_up_in_two_different_ways}

::: section-content
There is no semantic difference between the following two examples

::: code-example
[html]{.language-name}

``` {signature="DmljQtPRP07RmRxNp9VdamudRlGT4pbyDLBkXPWhx0U=" data-language="html"}
<figure>
  <img src="castle.jpeg" />
  <figcaption>
    <span itemscope><span itemprop="name">The Castle</span></span> (1986)
  </figcaption>
</figure>
```
:::

::: code-example
[html]{.language-name}

``` {signature="GTRWXkDpmrOZK2601BooMYzFKoYBc9D1/N1DlhJ9ZfE=" data-language="html"}
<span itemscope><meta itemprop="name" content="The Castle" /></span>
<figure>
  <img src="castle.jpeg" />
  <figcaption>The Castle (1986)</figcaption>
</figure>
```
:::

Both have a figure with a caption, and both, completely unrelated to the
figure, have an item with a name-value pair with the name \"name\" and
the value \"The Castle\". The only difference is that if the user drags
the figcaption out of the document, the item will be included in the
drag-and-drop data. The image associated with the item won\'t be
included.
:::

## Names and values {#names_and_values}

::: section-content
A property is an unordered set of unique tokens that are case-sensitive
and represent the name-value pairs. The property value must have at
least one token. In the example below, each data cell is a token.
:::

### Names examples {#names_examples}

::: section-content
<figure class="table-container">
<div class="_table">
<table class="standard-table">
<thead>
<tr class="header">
<th rowspan="2" scope="col"></th>
<th colspan="2" scope="col">Item</th>
</tr>
<tr class="odd">
<th scope="col">itemprop <strong>name</strong></th>
<th scope="col">itemprop <strong>value</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<th>itemprop</th>
<td>country</td>
<td>Ireland</td>
</tr>
<tr class="even">
<th>itemprop</th>
<td>Option</td>
<td>2</td>
</tr>
<tr class="odd">
<th>itemprop</th>
<td>https://www.flickr.com/photos/nlireland/6992065114/</td>
<td>Ring of Kerry</td>
</tr>
<tr class="even">
<th>itemprop</th>
<td>img</td>
<td>https://www.flickr.com/photos/nlireland/6992065114/</td>
</tr>
<tr class="odd">
<th>itemprop</th>
<td>website</td>
<td>flickr</td>
</tr>
<tr class="even">
<th>itemprop</th>
<td>(token)</td>
<td>(token)</td>
</tr>
</tbody>
</table>

</figure>

**Tokens** are either strings or URL\'s. An item is called a **typed
item** if it is a URL. Otherwise, it is a string. Strings cannot contain
a period or a colon (see below).

1.  If the item is a typed item it must be either:
    1.  A defined property name, or
    2.  A valid URL, which refers to the vocabulary definition, or
    3.  A valid URL that is used as a proprietary item property name
        (i.e. one not defined in a public specification), or
2.  If the item is not a typed item it must be:
    1.  A string that contains no \"`.`\" (U+002E FULL STOP) characters
        and no \"`:`\" characters (U+003A COLON) and is used as a
        proprietary item property name (again, one not defined in a
        public specification).

::: {#sect2 .notecard .note}
**Note:** The rules above disallow \":\" characters in non-URL values
because otherwise they could not be distinguished from URLs. Values with
\".\" characters are reserved for future extensions. Space characters
are disallowed because otherwise the values would be parsed as multiple
tokens.
:::
:::

## Values

::: section-content
The property value of a name-value pair is as given for the first
matching case in the following list:

-   If the element has an `itemscope` attribute
    -   The value is the **item** created by the element
-   If the element is a `meta` element
    -   The value is the value of the element\'s `content` attribute
-   If the element is an `audio`, `embed`, `iframe`, `img`, `source`,
    `track`, or `video` element
    -   The value is the resulting URL string that results from parsing
        the value of the element\'s src attribute relative to the node
        document (part of the [Microdata DOM API](../microdata)) of the
        element at the time the attribute is set
-   If the element is an `a`, `area`, or `link` element
    -   The value is the resulting URL string that results from parsing
        the value of the element\'s href attribute relative to the node
        document of the element at the time the attribute is set
-   If the element is an `object` element
    -   The value is the resulting URL string that results from parsing
        the value of the element\'s data attribute relative to the node
        document of the element at the time the attribute is set
-   If the element is a `data` element
    -   The value is the value of the element\'s value attribute
-   If the element is a `meter` element
    -   The value is the value of the element\'s `value` attribute
-   If the element is a `time` element
    -   The value is the element\'s `datetime` value

Otherwise

-   The value is the element\'s *textContent*.

If a property\'s value is a `URL`, the property must be specified using
a URL property element. The URL property elements are the `a`, `area`,
`audio`, `embed`, `iframe`, `img`, `link`, `object`, `source`, `track`,
and `video` elements.
:::

### Name order {#name_order}

::: section-content
Names are unordered relative to each other, but if a particular name has
multiple values, they do have a relative order.

In the following example, the \"a\" property has the values \"1\" and
\"2\", *in that order*, but whether the \"a\" property comes before the
\"b\" property or not is not important.

::: code-example
[html]{.language-name}

``` {signature="xFEqWjkjo6ilJyJ9W5e8BGTubU7PaQ3/I6tUAichAb4=" data-language="html"}
<div itemscope>
  <p itemprop="a">1</p>
  <p itemprop="a">2</p>
  <p itemprop="b">test</p>

```
:::

Here are several equivalent examples:

::: code-example
[html]{.language-name}

``` {signature="5oJkjkkRVdfIindRa1uY2M7971unAirwKKALwl0KTtA=" data-language="html"}
<div itemscope>
  <p itemprop="b">test</p>
  <p itemprop="a">1</p>
  <p itemprop="a">2</p>

```
:::

::: code-example
[html]{.language-name}

``` {signature="JZ+bX5t1B7XvrGwvNGoW/Ezsp55AO1dxmjjX9pSO6G0=" data-language="html"}
<div itemscope>
  <p itemprop="a">1</p>
  <p itemprop="b">test</p>
  <p itemprop="a">2</p>

```
:::

::: code-example
[html]{.language-name}

``` {signature="u9HP93CW5GobFWZWWWQsD0UfiwjQ8IRW5iRKdpVbGlU=" data-language="html"}
<div id="x">
  <p itemprop="a">1</p>

<div itemscope itemref="x">
  <p itemprop="b">test</p>
  <p itemprop="a">2</p>

```
:::
:::

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

#### HTML {#html_2}

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

::: {#sect3 .code-example}
::: iframe
:::
:::
:::

## Specifications

::: _table
  ------------------------------------------------------------------------------------------------------------------------------
  Specification
  ------------------------------------------------------------------------------------------------------------------------------
  [HTML Standard\
  [\#
  names:-the-itemprop-attribute]{.small}](https://html.spec.whatwg.org/multipage/microdata.html#names:-the-itemprop-attribute)

  ------------------------------------------------------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
               Desktop                                                         Mobile                                                                                   
  ------------ --------- ------ --------- ------------------- ------- -------- ----------------- ---------------- --------------------- --------------- --------------- ------------------
               Chrome    Edge   Firefox   Internet Explorer   Opera   Safari   WebView Android   Chrome Android   Firefox for Android   Opera Android   Safari on IOS   Samsung Internet
  `itemprop`   Yes       12     Yes       Yes                 Yes     Yes      Yes               Yes              Yes                   Yes             Yes             Yes
:::

## See also {#see_also}

::: section-content
-   [Other different global attributes](../global_attributes)
-   Other microdata related global attributes:
    -   [`itemid`](itemid)
    -   [`itemref`](itemref)
    -   [`itemscope`](itemscope)
    -   [`itemtype`](itemtype)
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/itemprop](https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/itemprop){._attribution-link}
:::
