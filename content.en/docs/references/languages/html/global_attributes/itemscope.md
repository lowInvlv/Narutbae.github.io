

# itemscope



::: section-content
`itemscope` is a boolean [global attribute](../global_attributes) that
defines the scope of associated metadata. Specifying the `itemscope`
attribute for an element creates a new item, which results in a number
of name-value pairs that are associated with the element.

A related attribute, [`itemtype`](itemtype), is used to specify the
valid URL of a vocabulary (such as
[schema.org](https://schema.org/){target="_blank"}) that describes the
item and its properties context. In each of the following examples, the
vocabulary is from [schema.org](https://schema.org/){target="_blank"}.

Every HTML element may have an `itemscope` attribute specified. An
`itemscope` element that does not have an associated `itemtype` must
have an associated `itemref`.

::: {#sect1 .notecard .note}
**Note:** Find more about `itemtype` attributes at
[https://schema.org/Thing](https://schema.org/Thing){target="_blank"}
:::
:::

### itemscope id attributes {#itemscope_id_attributes}

::: section-content
When you specify the `itemscope` attribute for an element, a new item is
created. The item consists of a group of name-value pairs. For elements
with an `itemscope` attribute and an `itemtype` attribute, you may also
specify an [`id`](../global_attributes#id) attribute. You can use the
`id` attribute to set a global identifier for the new item. A global
identifier allows the item to relate to other items found on pages
across the Web.
:::

## Examples

### Representing structured data for a movie {#representing_structured_data_for_a_movie}

::: section-content
The following example specifies the `itemtype` as
\"[http://schema.org/Movie](https://schema.org/Movie){target="_blank"}\",
and specifies four related `itemprop` attributes.

<figure class="table-container">
<div class="_table">
<table class="standard-table">
<tbody>
<tr class="odd">
<td rowspan="6">itemscope</td>
<td>Itemtype</td>
<td colspan="2">Movie</td>
</tr>
<tr class="even">
<td>itemprop</td>
<td>(itemprop name)</td>
<td>(itemprop value)</td>
</tr>
<tr class="odd">
<td>itemprop</td>
<td>director</td>
<td>James Cameron</td>
</tr>
<tr class="even">
<td>itemprop</td>
<td>genre</td>
<td>Science Fiction</td>
</tr>
<tr class="odd">
<td>itemprop</td>
<td>name</td>
<td>Avatar</td>
</tr>
<tr class="even">
<td>itemprop</td>
<td>Trailer</td>
<td>https://youtu.be/0AY1XIkX7bY</td>
</tr>
</tbody>
</table>

</figure>

::: code-example
[html]{.language-name}

``` {signature="/jnmuaB40gNQHsxKvvBlo9HFqLfh1j4lgexitkqw0Ek=" data-language="html"}
<div itemscope itemtype="https://schema.org/Movie">
  <h1 itemprop="name">Avatar</h1>
  <span>
    Director: <span itemprop="director">James Cameron</span> (born August 16,
    1954)
  </span>
  <span itemprop="genre">Science fiction</span>
  <a href="https://youtu.be/0AY1XIkX7bY" itemprop="trailer">Trailer</a>

```
:::
:::

### Representing structured data for a recipe {#representing_structured_data_for_a_recipe}

::: section-content
There are four `itemscope` attributes in the following example. Each
`itemscope` attribute sets the scope of its corresponding `itemtype`
attribute. The `itemtype`s, `Recipe`, `AggregateRating`, and
`NutritionInformation` in the following example are part of the
[schema.org](https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/www.schema.org)
structured data for a recipe, as specified by the first `itemtype`,
`http://schema.org/Recipe`.

<figure class="table-container">
<div class="_table">
<table class="standard-table">
<tbody>
<tr class="odd">
<td rowspan="14">itemscope</td>
<td>itemtype</td>
<td colspan="2">Recipe</td>
</tr>
<tr class="even">
<td>itemprop</td>
<td>name</td>
<td>Grandma's Holiday Apple Pie</td>
</tr>
<tr class="odd">
<td>itemprop</td>
<td>image</td>
<td>https://c1.staticflickr.com/1/30/42759561_8631e2f905_n.jpg</td>
</tr>
<tr class="even">
<td>itemprop</td>
<td>datePublished</td>
<td>2022-11-05</td>
</tr>
<tr class="odd">
<td>itemprop</td>
<td>description</td>
<td>This is my grandmother's apple pie recipe. I like to add a dash of
nutmeg.</td>
</tr>
<tr class="even">
<td>itemprop</td>
<td>prepTime</td>
<td>PT30M</td>
</tr>
<tr class="odd">
<td>itemprop</td>
<td>cookTime</td>
<td>PT1H</td>
</tr>
<tr class="even">
<td>itemprop</td>
<td>totalTime</td>
<td>PT1H30M</td>
</tr>
<tr class="odd">
<td>itemprop</td>
<td>recipeYield</td>
<td>1 9" pie (8 servings)</td>
</tr>
<tr class="even">
<td>itemprop</td>
<td>recipeIngredient</td>
<td>Thinly-sliced apples: 6 cups</td>
</tr>
<tr class="odd">
<td>itemprop</td>
<td>recipeIngredient</td>
<td>White sugar: 3/4 cup</td>
</tr>
<tr class="even">
<td>itemprop</td>
<td>recipeInstructions</td>
<td>1. Cut and peel apples 2. Mix sugar and cinnamon. Use additional
sugar for tart apples.</td>
</tr>
<tr class="odd">
<td>itemprop</td>
<td colspan="2">author [Person]</td>
</tr>
<tr class="even">
<td>itemprop</td>
<td>name</td>
<td>Carol Smith</td>
</tr>
<tr class="odd">
<td rowspan="3">itemscope</td>
<td>itemprop[itemtype]</td>
<td colspan="2">aggregateRating [AggregateRating]</td>
</tr>
<tr class="even">
<td>itemprop</td>
<td>ratingValue</td>
<td>4.0</td>
</tr>
<tr class="odd">
<td>itemprop</td>
<td>reviewCount</td>
<td>35</td>
</tr>
<tr class="even">
<td rowspan="4">itemscope</td>
<td>itemprop[itemtype]</td>
<td colspan="2">nutrition [NutritionInformation]</td>
</tr>
<tr class="odd">
<td>itemprop</td>
<td>servingSize</td>
<td>1 medium slice</td>
</tr>
<tr class="even">
<td>itemprop</td>
<td>calories</td>
<td>250 cal</td>
</tr>
<tr class="odd">
<td>itemprop</td>
<td>fatContent</td>
<td>12 g</td>
</tr>
</tbody>
</table>

</figure>

::: {#sect2 .notecard .note}
**Note:** A handy tool for extracting microdata structures from HTML is
Google\'s [Rich Results Testing
Tool](https://search.google.com/test/rich-results){target="_blank"}. Try
it on the HTML shown here.
:::

#### HTML

::: code-example
[html]{.language-name}

``` {signature="Nc5+66S0COEP5o5spiAEVMIRBcVtEnRhgAXJYhcguxg=" data-language="html"}
<div itemscope itemtype="https://schema.org/Recipe">
  <h2 itemprop="name">Grandma's Holiday Apple Pie</h2>
  <img
    itemprop="image"
    src="https://c1.staticflickr.com/1/30/42759561_8631e2f905_n.jpg"
    width="50"
    height="50" />
  <p>
    By
    <span itemprop="author" itemscope itemtype="https://schema.org/Person">
      <span itemprop="name">Carol Smith</span>
    </span>
  </p>
  <p>
    Published:
    <time datetime="2022-11-05" itemprop="datePublished">
      November 5, 20022
    </time>
  </p>
  <span itemprop="description">
    This is my grandmother's apple pie recipe. I like to add a dash of nutmeg.
  </span>
  <br />
  <span
    itemprop="aggregateRating"
    itemscope
    itemtype="https://schema.org/AggregateRating">
    <span itemprop="ratingValue">4.0</span> stars based on
    <span itemprop="reviewCount">35</span> reviews
  </span>
  <br />
  Prep time: <time datetime="PT30M" itemprop="prepTime">30 min</time>
  <br />
  Cook time: <time datetime="PT1H" itemprop="cookTime">1 hour</time>
  <br />
  Total time: <time datetime="PT1H30M" itemprop="totalTime">1 hour 30 min</time>
  <br />
  Yield: <span itemprop="recipeYield">1 9" pie (8 servings)</span>
  <br />
  <span
    itemprop="nutrition"
    itemscope
    itemtype="https://schema.org/NutritionInformation">
    Serving size: <span itemprop="servingSize">1 medium slice</span><br />
    Calories per serving: <span itemprop="calories">250 cal</span><br />
    Fat per serving: <span itemprop="fatContent">12 g</span><br />
  </span>
  <p>
    Ingredients:<br />
    <span itemprop="recipeIngredient">Thinly-sliced apples: 6 cups<br /></span>
    <span itemprop="recipeIngredient">White sugar: 3/4 cup<br /></span>
    …
  </p>
  Directions: <br />
  <div itemprop="recipeInstructions">
    1. Cut and peel apples<br />
    2. Mix sugar and cinnamon. Use additional sugar for tart apples. <br />
    …
  

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
  ------------------------------------------------------------------------------------------------
  Specification
  ------------------------------------------------------------------------------------------------
  [HTML Standard\
  [\#
  attr-itemscope]{.small}](https://html.spec.whatwg.org/multipage/microdata.html#attr-itemscope)

  ------------------------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
                Desktop                                                         Mobile                                                                                   
  ------------- --------- ------ --------- ------------------- ------- -------- ----------------- ---------------- --------------------- --------------- --------------- ------------------
                Chrome    Edge   Firefox   Internet Explorer   Opera   Safari   WebView Android   Chrome Android   Firefox for Android   Opera Android   Safari on IOS   Samsung Internet
  `itemscope`   Yes       12     Yes       Yes                 Yes     Yes      Yes               Yes              Yes                   Yes             Yes             Yes
:::

## See also {#see_also}

::: section-content
-   [Other different global attributes](../global_attributes)
-   Other microdata related global attributes:
    -   [`itemid`](itemid)
    -   [`itemprop`](itemprop)
    -   [`itemref`](itemref)
    -   [`itemtype`](itemtype)
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/itemscope](https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/itemscope){._attribution-link}
:::
