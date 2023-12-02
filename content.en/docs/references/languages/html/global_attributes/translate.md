

# translate



::: section-content
The `translate` [global attribute](../global_attributes) is an
[enumerated](https://developer.mozilla.org/en-US/docs/Glossary/Enumerated)
attribute that is used to specify whether an element\'s *translatable
attribute* values and its
[`Text`](https://developer.mozilla.org/en-US/docs/Web/API/Text) node
children should be translated when the page is localized, or whether to
leave them unchanged.

It can have the following values:

-   empty string or `yes`, which indicates that the element should be
    translated when the page is localized.
-   `no`, which indicates that the element must not be translated.

Although not all browsers recognize this attribute, it is respected by
automatic translation systems such as Google Translate, and may also be
respected by tools used by human translators. As such it\'s important
that web authors use this attribute to mark content that should not be
translated.
:::

## Examples

::: section-content
In this example, the `translate` attribute is used to ask translation
tools not to translate the company\'s brand name in the footer.

::: code-example
[html]{.language-name}

``` {signature="YUR8JX+HWnFFzd5xwMM0gCS0CxT53hVfauSW2dh1TGM=" data-language="html"}
<footer>
  <small>© 2020 <span translate="no">BrandName</span></small>
</footer>
```
:::
:::

## Specifications

::: _table
  ------------------------------------------------------------------------------------------
  Specification
  ------------------------------------------------------------------------------------------
  [HTML Standard\
  [\#
  attr-translate]{.small}](https://html.spec.whatwg.org/multipage/dom.html#attr-translate)

  ------------------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
                Desktop                                                         Mobile                                                                                   
  ------------- --------- ------ --------- ------------------- ------- -------- ----------------- ---------------- --------------------- --------------- --------------- ------------------
                Chrome    Edge   Firefox   Internet Explorer   Opera   Safari   WebView Android   Chrome Android   Firefox for Android   Opera Android   Safari on IOS   Samsung Internet
  `translate`   19        79     111       No                  15      6        4.4               25               111                   14              6               1.5
:::

## See also {#see_also}

::: section-content
-   All [global attributes](../global_attributes).
-   The [`HTMLElement.translate`]{.page-not-created} property that
    reflects this attribute.
-   [Using HTML\'s translate
    attribute](https://www.w3.org/International/questions/qa-translate-flag){target="_blank"}.
-   HTML [`lang`](../global_attributes#lang) attribute
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/translate](https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/translate){._attribution-link}
:::
