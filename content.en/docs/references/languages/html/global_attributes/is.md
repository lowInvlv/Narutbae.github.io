

# is



::: section-content
The `is` [global attribute](../global_attributes) allows you to specify
that a standard HTML element should behave like a defined custom
built-in element (see [Using custom
elements](https://developer.mozilla.org/en-US/docs/Web/API/Web_components/Using_custom_elements)
for more details).

This attribute can only be used if the specified custom element name has
been successfully
[defined](https://developer.mozilla.org/en-US/docs/Web/API/CustomElementRegistry/define)
in the current document, and extends the element type it is being
applied to.
:::

## Examples

::: section-content
The following code is taken from our
[word-count-web-component](https://github.com/mdn/web-components-examples/tree/main/word-count-web-component){target="_blank"}
example ([see it live
also](https://mdn.github.io/web-components-examples/word-count-web-component/){target="_blank"}).

::: code-example
[js]{.language-name}

``` {signature="jVc95/umnT02cy/WQ+QXP/GX79Q/NzKV4VzHQjCaIMo=" data-language="js"}
// Create a class for the element
class WordCount extends HTMLParagraphElement {
  constructor() {
    // Always call super first in constructor
    super();

    // Constructor contents omitted for brevity
    // …
  }
}

// Define the new element
customElements.define("word-count", WordCount, { extends: "p" });
```
:::

::: code-example
[html]{.language-name}

``` {signature="2HWc9XXr7N6633Peud0V5KO5Agg7fFBZQXZH96uYCqM=" data-language="html"}
<p is="word-count"></p>
```
:::
:::

## Specifications

::: _table
  ----------------------------------------------------------------------------------------
  Specification
  ----------------------------------------------------------------------------------------
  [HTML Standard\
  [\#
  attr-is]{.small}](https://html.spec.whatwg.org/multipage/custom-elements.html#attr-is)

  ----------------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
         Desktop                                                         Mobile                                                                                   
  ------ --------- ------ --------- ------------------- ------- -------- ----------------- ---------------- --------------------- --------------- --------------- ------------------
         Chrome    Edge   Firefox   Internet Explorer   Opera   Safari   WebView Android   Chrome Android   Firefox for Android   Opera Android   Safari on IOS   Samsung Internet
  `is`   67        79     63        No                  54      No       67                67               63                    48              No              9.0
:::

## See also {#see_also}

::: section-content
-   All [global attributes](../global_attributes).
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/is](https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/is){._attribution-link}
:::
