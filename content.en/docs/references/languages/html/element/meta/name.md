

# Standard metadata names



::: section-content
The [`<meta>`](../meta) element can be used to provide document metadata
in terms of name-value pairs, with the [`name`](../meta#name) attribute
giving the metadata name, and the [`content`](../meta#content) attribute
giving the value.
:::

### Standard metadata names defined in the HTML specification {#standard_metadata_names_defined_in_the_html_specification}

::: section-content
The HTML specification defines the following set of standard metadata
names:

-   `application-name`: the name of the application running in the web
    page.

    ::: {#sect1 .notecard .note}
    **Note:**

    -   Browsers may use this to identify the application. It is
        different from the [`<title>`](../title) element, which usually
        contain the application name, but may also contain information
        like the document name or a status.
    -   Simple web pages shouldn\'t define an application-name.
    :::
-   `author`: the name of the document\'s author.
-   `description`: a short and accurate summary of the content of the
    page. Several browsers, like Firefox and Opera, use this as the
    default description of bookmarked pages.
-   `generator`: the identifier of the software that generated the page.
-   `keywords`: words relevant to the page\'s content separated by
    commas.
-   `referrer`: controls the HTTP
    [`Referer`](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Referer)
    header of requests sent from the document:
    <figure class="table-container">
    <div class="_table">
    <table class="standard-table">
    <caption>Values for the <code>content</code> attribute of
    <code>&lt;meta name="referrer"&gt;</code></caption>
    <tbody>
    <tr class="odd">
    <td><code>no-referrer</code></td>
    <td>Do not send a HTTP <a
    href="https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Referer"><code>Referer</code></a>
    header.</td>
    </tr>
    <tr class="even">
    <td><code>origin</code></td>
    <td>Send the <a
    href="https://developer.mozilla.org/en-US/docs/Glossary/Origin">origin</a>
    of the document.</td>
    </tr>
    <tr class="odd">
    <td><code>no-referrer-when-downgrade</code></td>
    <td>Send the full URL when the destination is at least as secure as the
    current page (HTTP(S)→HTTPS), but send no referrer when it's less secure
    (HTTPS→HTTP). This is the default behavior.</td>
    </tr>
    <tr class="even">
    <td><code>origin-when-cross-origin</code></td>
    <td>Send the full URL (stripped of parameters) for same-origin requests,
    but only send the origin for other cases.</td>
    </tr>
    <tr class="odd">
    <td><code>same-origin</code></td>
    <td>Send the full URL (stripped of parameters) for same-origin requests.
    Cross-origin requests will contain no referrer header.</td>
    </tr>
    <tr class="even">
    <td><code>strict-origin</code></td>
    <td>Send the origin when the destination is at least as secure as the
    current page (HTTP(S)→HTTPS), but send no referrer when it's less secure
    (HTTPS→HTTP).</td>
    </tr>
    <tr class="odd">
    <td><code>strict-origin-when-cross-origin</code></td>
    <td>Send the full URL (stripped of parameters) for same-origin requests.
    Send the origin when the destination is at least as secure as the
    current page (HTTP(S)→HTTPS). Otherwise, send no referrer.</td>
    </tr>
    <tr class="even">
    <td><code>unsafe-URL</code></td>
    <td>Send the full URL (stripped of parameters) for same-origin or
    cross-origin requests.</td>
    </tr>
    </tbody>
    </table>
    
    </figure>

    ::: {#sect2 .notecard .note}
    **Note:**

    -   Dynamically inserting `<meta name="referrer">` (with
        [`document.write()`](https://developer.mozilla.org/en-US/docs/Web/API/Document/write)
        or
        [`appendChild()`](https://developer.mozilla.org/en-US/docs/Web/API/Node/appendChild))
        makes the referrer behavior unpredictable.
    -   When several conflicting policies are defined, the `no-referrer`
        policy is applied.
    :::
-   [`theme-color`](name/theme-color): indicates a suggested color that
    user agents should use to customize the display of the page or of
    the surrounding user interface. The `content` attribute contains a
    valid CSS
    [`<color>`](https://developer.mozilla.org/en-US/docs/Web/CSS/color_value).
    The `media` attribute with a valid media query list can be included
    to set the media the theme color metadata applies to.
-   `color-scheme`: specifies one or more color schemes with which the
    document is compatible. The browser will use this information in
    tandem with the user\'s browser or device settings to determine what
    colors to use for everything from background and foregrounds to form
    controls and scrollbars. The primary use for
    `<meta name="color-scheme">` is to indicate compatibility with---and
    order of preference for---light and dark color modes. The value of
    the [`content`](../meta#content) property for `color-scheme` may be
    one of the following:

    [`normal`](#normal)

    :   The document is unaware of color schemes and should be rendered
        using the default color palette.

    [\[](#sect3)`light` \| `dark`\]+

    :   One or more color schemes supported by the document. Specifying
        the same color scheme more than once has the same effect as
        specifying it only once. Indicating multiple color schemes
        indicates that the first scheme is preferred by the document,
        but that the second specified scheme is acceptable if the user
        prefers it.

    [`only light`](#only_light)

    :   Indicates that the document *only* supports light mode, with a
        light background and dark foreground colors. By specification,
        `only dark` *is not valid*, because forcing a document to render
        in dark mode when it isn\'t truly compatible with it can result
        in unreadable content; all major browsers default to light mode
        if not otherwise configured.

    For example, to indicate that a document prefers dark mode but does
    render functionally in light mode as well:

    ::: code-example
    [html]{.language-name}

    ``` {signature="0w0L++l4RuA3mMDJx2WP4P5IvHUqhkh7+LHZnzh6nHc=" data-language="html"}
    <meta name="color-scheme" content="dark light" />
    ```
    :::

    This works at the document level in the same way that the CSS
    [`color-scheme`](https://developer.mozilla.org/en-US/docs/Web/CSS/color-scheme)
    property lets individual elements specify their preferred and
    accepted color schemes. Your styles can adapt to the current color
    scheme using the
    [`prefers-color-scheme`](https://developer.mozilla.org/en-US/docs/Web/CSS/@media/prefers-color-scheme)
    CSS media feature.
:::

### Standard metadata names defined in other specifications {#standard_metadata_names_defined_in_other_specifications}

::: section-content
The CSS Device Adaptation specification defines the following metadata
name:

-   `viewport`: gives hints about the size of the initial size of the
    [viewport](https://developer.mozilla.org/en-US/docs/Glossary/Viewport).
    <figure class="table-container">
    <div class="_table">
    <table class="fullwidth-table">
    <caption>Values for the content of
    <code>&lt;meta name="viewport"&gt;</code></caption>
    <colgroup>
    <col style="width: 33%" />
    <col style="width: 33%" />
    <col style="width: 33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th scope="col">Value</th>
    <th scope="col">Possible subvalues</th>
    <th scope="col">Description</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><code>width</code></td>
    <td>A positive integer number, or the text
    <code>device-width</code></td>
    <td>Defines the pixel width of the viewport that you want the website to
    be rendered at.</td>
    </tr>
    <tr class="even">
    <td><code>height</code></td>
    <td>A positive integer, or the text <code>device-height</code></td>
    <td>Defines the height of the viewport. Not used by any browser.</td>
    </tr>
    <tr class="odd">
    <td><code>initial-scale</code></td>
    <td>A positive number between <code>0.0</code> and
    <code>10.0</code></td>
    <td>Defines the ratio between the device width
    (<code>device-width</code> in portrait mode or
    <code>device-height</code> in landscape mode) and the viewport
    size.</td>
    </tr>
    <tr class="even">
    <td><code>maximum-scale</code></td>
    <td>A positive number between <code>0.0</code> and
    <code>10.0</code></td>
    <td>Defines the maximum amount to zoom in. It must be greater or equal
    to the <code>minimum-scale</code> or the behavior is undefined. Browser
    settings can ignore this rule and iOS10+ ignores it by default.</td>
    </tr>
    <tr class="odd">
    <td><code>minimum-scale</code></td>
    <td>A positive number between <code>0.0</code> and
    <code>10.0</code></td>
    <td>Defines the minimum zoom level. It must be smaller or equal to the
    <code>maximum-scale</code> or the behavior is undefined. Browser
    settings can ignore this rule and iOS10+ ignores it by default.</td>
    </tr>
    <tr class="even">
    <td><code>user-scalable</code></td>
    <td><code>yes</code> or <code>no</code></td>
    <td>If set to <code>no</code>, the user is not able to zoom in the
    webpage. The default is <code>yes</code>. Browser settings can ignore
    this rule, and iOS10+ ignores it by default.</td>
    </tr>
    <tr class="odd">
    <td><code>viewport-fit</code></td>
    <td><code>auto</code>, <code>contain</code> or <code>cover</code></td>
    <td><p>The <code>auto</code> value doesn't affect the initial layout
    viewport, and the whole web page is viewable.</p>
    <p>The <code>contain</code> value means that the viewport is scaled to
    fit the largest rectangle inscribed within the display.</p>
    <p>The <code>cover</code> value means that the viewport is scaled to
    fill the device display. It is highly recommended to make use of the <a
    href="https://developer.mozilla.org/en-US/docs/Web/CSS/env">safe area
    inset</a> variables to ensure that important content doesn't end up
    outside the display.</p></td>
    </tr>
    </tbody>
    </table>
    
    </figure>

    ::: {#sect4 .notecard .warning}
    **Warning:**

    Disabling zooming capabilities by setting `user-scalable` to a value
    of `no` prevents people experiencing low vision conditions from
    being able to read and understand page content.

    -   [MDN Understanding WCAG, Guideline 1.4
        explanations](https://developer.mozilla.org/en-US/docs/Web/Accessibility/Understanding_WCAG/Perceivable#guideline_1.4_make_it_easier_for_users_to_see_and_hear_content_including_separating_foreground_from_background)
    -   [Understanding Success Criterion 1.4.4 \| W3C Understanding WCAG
        2.0](https://www.w3.org/TR/UNDERSTANDING-WCAG20/visual-audio-contrast-scale.html){target="_blank"}
    :::
:::

### Other metadata names {#other_metadata_names}

::: section-content
The [WHATWG Wiki MetaExtensions
page](https://wiki.whatwg.org/wiki/MetaExtensions){target="_blank"}
contains a large set of non-standard metadata names that have not been
formally accepted yet; however, some of the names included there are
already used quite commonly in practice --- including the following:

-   `creator`: the name of the creator of the document, such as an
    organization or institution. If there are more than one, several
    [`<meta>`](../meta) elements should be used.
-   `googlebot`, a synonym of `robots`, is only followed by Googlebot
    (the indexing crawler for Google).
-   `publisher`: the name of the document\'s publisher.
-   `robots`: the behavior that cooperative crawlers, or \"robots\",
    should use with the page. It is a comma-separated list of the values
    below:
    <figure class="table-container">
    <div class="_table">
    <table>
    <thead>
    <tr class="header">
    <th>Value</th>
    <th>Description</th>
    <th>Used by</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><code>index</code></td>
    <td>Allows the robot to index the page (default).</td>
    <td>All</td>
    </tr>
    <tr class="even">
    <td><code>noindex</code></td>
    <td>Requests the robot to not index the page.</td>
    <td>All</td>
    </tr>
    <tr class="odd">
    <td><code>follow</code></td>
    <td>Allows the robot to follow the links on the page (default).</td>
    <td>All</td>
    </tr>
    <tr class="even">
    <td><code>nofollow</code></td>
    <td>Requests the robot to not follow the links on the page.</td>
    <td>All</td>
    </tr>
    <tr class="odd">
    <td><code>all</code></td>
    <td>Equivalent to <code>index, follow</code></td>
    <td><a
    href="https://developers.google.com/search/docs/advanced/crawling/special-tags?visit_id=637855965067987211-415685194&amp;rd=1"
    target="_blank">Google</a></td>
    </tr>
    <tr class="even">
    <td><code>none</code></td>
    <td>Equivalent to <code>noindex, nofollow</code></td>
    <td><a
    href="https://developers.google.com/search/docs/advanced/crawling/special-tags?visit_id=637855965074074862-574753619&amp;rd=1"
    target="_blank">Google</a></td>
    </tr>
    <tr class="odd">
    <td><code>noarchive</code></td>
    <td>Requests the search engine not to cache the page content.</td>
    <td><a
    href="https://developers.google.com/search/docs/advanced/robots/robots_meta_tag"
    target="_blank">Google</a>, <a
    href="https://help.yahoo.com/kb/search-for-desktop/SLN2213.html"
    target="_blank">Yahoo</a>, <a
    href="https://www.bing.com/webmasters/help/which-robots-metatags-does-bing-support-5198d240"
    target="_blank">Bing</a></td>
    </tr>
    <tr class="even">
    <td><code>nosnippet</code></td>
    <td>Prevents displaying any description of the page in search engine
    results.</td>
    <td><a
    href="https://developers.google.com/search/docs/advanced/robots/robots_meta_tag"
    target="_blank">Google</a>, <a
    href="https://www.bing.com/webmasters/help/which-robots-metatags-does-bing-support-5198d240"
    target="_blank">Bing</a></td>
    </tr>
    <tr class="odd">
    <td><code>noimageindex</code></td>
    <td>Requests this page not to appear as the referring page of an indexed
    image.</td>
    <td><a
    href="https://developers.google.com/search/docs/advanced/robots/robots_meta_tag"
    target="_blank">Google</a></td>
    </tr>
    <tr class="even">
    <td><code>nocache</code></td>
    <td>Synonym of <code>noarchive</code>.</td>
    <td><a
    href="https://www.bing.com/webmasters/help/which-robots-metatags-does-bing-support-5198d240"
    target="_blank">Bing</a></td>
    </tr>
    </tbody>
    </table>
    
    </figure>

    ::: {#sect5 .notecard .note}
    **Note:**

    -   Only cooperative robots follow these rules. Do not expect to
        prevent email harvesters with them.
    -   The robot still needs to access the page in order to read these
        rules. To prevent bandwidth consumption, use a
        *[robots.txt](https://developer.mozilla.org/en-US/docs/Glossary/Robots.txt)*
        file.
    -   If you want to remove a page, `noindex` will work, but only
        after the robot visits the page again. Ensure that the
        `robots.txt` file is not preventing revisits.
    -   Some values are mutually exclusive, like `index` and `noindex`,
        or `follow` and `nofollow`. In these cases the robot\'s behavior
        is undefined and may vary between them.
    -   Some crawler robots, like Google, Yahoo and Bing, support the
        same values for the HTTP header `X-Robots-Tag`; this allows
        non-HTML documents like images to use these rules.
    :::
:::

## Specifications

::: _table
  -------------------------------------------------------------------------------------------------------------------------
  Specification
  -------------------------------------------------------------------------------------------------------------------------
  [HTML Standard\
  [\# standard-metadata-names]{.small}](https://html.spec.whatwg.org/multipage/semantics.html#standard-metadata-names)

  [Referrer Policy\
  [\#
  referrer-policy-delivery-meta]{.small}](https://w3c.github.io/webappsec-referrer-policy/#referrer-policy-delivery-meta)
  -------------------------------------------------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
  ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
                   Desktop                                                                                                              Mobile                                                      
  ---------------- ------------- ------------- ------------ ---------------------------------------------------- ------------- -------- ------------- ------------- ------------ --------- -------- -------------
                   Chrome        Edge          Firefox      Internet Explorer                                    Opera         Safari   WebView       Chrome        Firefox for  Opera     Safari   Samsung
                                                                                                                                        Android       Android       Android      Android   on IOS   Internet

  `name`           1             12            1            ≤6                                                   ≤12.1         ≤4       4.4           18            4            ≤12.1     ≤3.2     1.0

  `color-scheme`   81            81            96           No                                                   68            12.1     81            81            96           No        12.2     13.0

  `referrer`       17            79            36           11                                                   15            11.1     37            18            36           No        12       1.0
                                                                                                                                                                                                    
                   Until Chrome                The          Browsers initially supported an [early               Until Opera            Until Chrome  Until Chrome  The                             Until Samsung
                   46, `content`               `referrer`   draft](https://wiki.whatwg.org/wiki/Meta_referrer)   46, `content`          46, `content` 46, `content` `referrer`                      Internet 5.0,
                   values                      value        of the specification which can only use a meta tag   values                 values        values        value                           `content`
                   weren\'t                    wasn\'t      and is only compatible with the `origin` value from  weren\'t               weren\'t      weren\'t      wasn\'t                         values
                   constrained                 taken into   the new spec.                                        constrained            constrained   constrained   taken into                      weren\'t
                   to the values               account when                                                      to the values          to the values to the values account when                    constrained
                   listed in the               navigation                                                        listed in the          listed in the listed in the navigation                      to the values
                   spec.                       was                                                               spec.                  spec.         spec.         was                             listed in the
                                               happening                                                                                                            happening                       spec.
                                               via the                                                                                                              via the                         
                                               context menu                                                                                                         context menu                    
                                               or middle                                                                                                            or middle                       
                                               click until                                                                                                          click until                     
                                               Firefox 39.                                                                                                          Firefox 39.                     

  `scheme`         1             12            1            ≤6                                                   ≤12.1         ≤4       4.4           18            4            ≤12.1     ≤3.2     1.0

  `theme-color`    73            79            No           No                                                   No            15       No            80            No           No        15       6.2
                                                                                                                                                                                                    
                   Chrome uses   Edge uses the                                                                                                        Chrome for                                    
                   the color     color only on                                                                                                        Android does                                  
                   only on       installed                                                                                                            not use the                                   
                   installed     progressive                                                                                                          color on                                      
                   progressive   web apps.                                                                                                            devices with                                  
                   web apps.                                                                                                                          native dark                                   
                                                                                                                                                      mode enabled.                                 
                   39--72                                                                                                                                                                           
                                                                                                                                                                                                    
                   Chrome                                                                                                                                                                           
                   reports                                                                                                                                                                          
                   support, but                                                                                                                                                                     
                   does not                                                                                                                                                                         
                   actually use                                                                                                                                                                     
                   the color                                                                                                                                                                        
                   anywhere.                                                                                                                                                                        
  ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
:::

## See also {#see_also}

::: section-content
-   [Viewport `<meta>` tag](../../viewport_meta_tag)
-   [Metadata: the `<meta>`
    element](https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/The_head_metadata_in_HTML#metadata_the_meta_element)
    in [What\'s in the head? Metadata in
    HTML](https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/The_head_metadata_in_HTML)
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Element/meta/name](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/meta/name){._attribution-link}
:::
