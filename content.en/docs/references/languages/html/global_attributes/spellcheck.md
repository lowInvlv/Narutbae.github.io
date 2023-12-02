

# spellcheck



::: section-content
The `spellcheck` [global attribute](../global_attributes) is an
[enumerated](https://developer.mozilla.org/en-US/docs/Glossary/Enumerated)
attribute that defines whether the element may be checked for spelling
errors.
:::

## Try it {#try_it}

::: section-content
::: iframe
::: {.output-header .border-rounded-top}
#### HTML Demo: spellcheck {#html-demo-spellcheck .output-heading}

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

::: {#editor-container .editor-container .tabbed-shorter .hidden .border-rounded-bottom editor-type="tabbed"}
::: {#tab-container .section .tabs}
::: {#tablist .tab-list role="tablist"}
HTML

CSS

JavaScript
:::

::: {#html-panel .section .hidden tabindex="0" role="tabpanel" aria-labelledby="html" aria-hidden="true"}
::: {#html-editor}
    <p contenteditable spellcheck="true">This exampull will be checkd fur spellung when you try to edit it.</p>

    <p contenteditable spellcheck="false">This exampull will nut be checkd fur spellung when you try to edit it.</p>
:::
:::

::: {#css-panel .section .hidden tabindex="0" role="tabpanel" aria-labelledby="css" aria-hidden="true"}
::: {#css-editor}
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

It may have the following values:

-   empty string or `true`, which indicates that the element should be,
    if possible, checked for spelling errors;
-   `false`, which indicates that the element should not be checked for
    spelling errors.

If this attribute is not set, its default value is element-type and
browser-defined. This default value may also be *inherited*, which means
that the element content will be checked for spelling errors only if its
nearest ancestor has a *spellcheck* state of `true`.

This attribute is merely a hint for the browser: browsers are not
required to check for spelling errors. Typically non-editable elements
are not checked for spelling errors, even if the `spellcheck` attribute
is set to `true` and the browser supports spellchecking.
:::

## Security and privacy concerns {#security_and_privacy_concerns}

::: section-content
Using spellchecking can have consequences for users\' security and
privacy. The specification does not regulate *how* spellchecking is done
and the content of the element may be sent to a third party for
spellchecking results (see [enhanced spellchecking and
\"spell-jacking\"](https://www.otto-js.com/news/article/chrome-and-edge-enhanced-spellcheck-features-expose-pii-even-your-passwords){target="_blank"}).

You should consider setting `spellcheck` to `false` for elements that
can contain sensitive information.
:::

## Specifications

::: _table
  ----------------------------------------------------------------------------------------------------
  Specification
  ----------------------------------------------------------------------------------------------------
  [HTML Standard\
  [\#
  attr-spellcheck]{.small}](https://html.spec.whatwg.org/multipage/interaction.html#attr-spellcheck)

  ----------------------------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
                 Desktop                                                         Mobile                                                                                   
  -------------- --------- ------ --------- ------------------- ------- -------- ----------------- ---------------- --------------------- --------------- --------------- ------------------
                 Chrome    Edge   Firefox   Internet Explorer   Opera   Safari   WebView Android   Chrome Android   Firefox for Android   Opera Android   Safari on IOS   Samsung Internet
  `spellcheck`   9         12     Yes       11                  Yes     Yes      47                47               57                    37              9.3             5.0
:::

## See also {#see_also}

::: section-content
-   All [global attributes](../global_attributes).
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/spellcheck](https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/spellcheck){._attribution-link}
:::
