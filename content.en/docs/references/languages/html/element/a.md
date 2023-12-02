

# \<a\>: The Anchor element



::: section-content
The `<a>` [HTML](../index) element (or *anchor* element), with [its
`href` attribute](#href), creates a hyperlink to web pages, files, email
addresses, locations in the same page, or anything else a URL can
address.

Content within each `<a>` *should* indicate the link\'s destination. If
the `href` attribute is present, pressing the enter key while focused on
the `<a>` element will activate it.
:::

## Try it {#try_it}

::: section-content
::: iframe
::: {.output-header .border-rounded-top}
#### HTML Demo: \<a\> {#html-demo-a .output-heading}

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
    <p>You can reach Michael at:</p>

    <ul>
      <li><a href="https://example.com">Website</a></li>
      <li><a href="mailto:m.bluth@example.com">Email</a></li>
      <li><a href="tel:+123456789">Phone</a></li>
    </ul>
:::
:::

::: {#css-panel .section .hidden tabindex="0" role="tabpanel" aria-labelledby="css" aria-hidden="true"}
::: {#css-editor}
    li {
      margin-bottom: 0.5rem;
    }
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
:::

## Attributes

::: section-content
This element\'s attributes include the [global
attributes](../global_attributes).

[`download`](#download)

:   Causes the browser to treat the linked URL as a download. Can be
    used with or without a `filename` value:

    -   Without a value, the browser will suggest a filename/extension,
        generated from various sources:
        -   The
            [`Content-Disposition`](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Disposition)
            HTTP header
        -   The final segment in the URL
            [path](https://developer.mozilla.org/en-US/docs/Web/API/URL/pathname)
        -   The [media
            type](https://developer.mozilla.org/en-US/docs/Glossary/MIME_type)
            (from the
            [`Content-Type`](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Type)
            header, the start of a [`data:`
            URL](https://developer.mozilla.org/en-US/docs/Web/HTTP/Basics_of_HTTP/Data_URLs),
            or
            [`Blob.type`](https://developer.mozilla.org/en-US/docs/Web/API/Blob/type)
            for a [`blob:`
            URL](https://developer.mozilla.org/en-US/docs/Web/API/URL/createObjectURL_static))
    -   `filename`: defining a value suggests it as the filename. `/`
        and `\` characters are converted to underscores (`_`).
        Filesystems may forbid other characters in filenames, so
        browsers will adjust the suggested name if necessary.

    ::: {#sect1 .notecard .note}
    **Note:**

    -   `download` only works for [same-origin
        URLs](https://developer.mozilla.org/en-US/docs/Web/Security/Same-origin_policy),
        or the `blob:` and `data:` schemes.
    -   How browsers treat downloads varies by browser, user settings,
        and other factors. The user may be prompted before a download
        starts, or the file may be saved automatically, or it may open
        automatically, either in an external application or in the
        browser itself.
    -   If the `Content-Disposition` header has different information
        from the `download` attribute, resulting behavior may differ:
        -   If the header specifies a `filename`, it takes priority over
            a filename specified in the `download` attribute.
        -   If the header specifies a disposition of `inline`, Chrome
            and Firefox prioritize the attribute and treat it as a
            download. Old Firefox versions (before 82) prioritize the
            header and will display the content inline.
    :::

[`href`](#href)

:   The URL that the hyperlink points to. Links are not restricted to
    HTTP-based URLs --- they can use any URL scheme supported by
    browsers:

    -   Sections of a page with document fragments
    -   Specific text portions with [text
        fragments](https://developer.mozilla.org/en-US/docs/Web/Text_fragments)
    -   Pieces of media files with media fragments
    -   Telephone numbers with `tel:` URLs
    -   Email addresses with `mailto:` URLs
    -   SMS text messages with `sms:` URLs
    -   While web browsers may not support other URL schemes, websites
        can with
        [`registerProtocolHandler()`](https://developer.mozilla.org/en-US/docs/Web/API/Navigator/registerProtocolHandler)

[`hreflang`](#hreflang)

:   Hints at the human language of the linked URL. No built-in
    functionality. Allowed values are the same as [the global `lang`
    attribute](../global_attributes/lang).

[`ping`](#ping)

:   A space-separated list of URLs. When the link is followed, the
    browser will send
    [`POST`](https://developer.mozilla.org/en-US/docs/Web/HTTP/Methods/POST)
    requests with the body `PING` to the URLs. Typically for tracking.

[`referrerpolicy`](#referrerpolicy)

:   How much of the
    [referrer](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Referer)
    to send when following the link.

    -   `no-referrer`: The
        [`Referer`](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Referer)
        header will not be sent.
    -   `no-referrer-when-downgrade`: The
        [`Referer`](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Referer)
        header will not be sent to
        [origin](https://developer.mozilla.org/en-US/docs/Glossary/Origin)s
        without
        [TLS](https://developer.mozilla.org/en-US/docs/Glossary/TLS)
        ([HTTPS](https://developer.mozilla.org/en-US/docs/Glossary/HTTPS)).
    -   `origin`: The sent referrer will be limited to the origin of the
        referring page: its
        [scheme](https://developer.mozilla.org/en-US/docs/Learn/Common_questions/Web_mechanics/What_is_a_URL),
        [host](https://developer.mozilla.org/en-US/docs/Glossary/Host),
        and
        [port](https://developer.mozilla.org/en-US/docs/Glossary/Port).
    -   `origin-when-cross-origin`: The referrer sent to other origins
        will be limited to the scheme, the host, and the port.
        Navigations on the same origin will still include the path.
    -   `same-origin`: A referrer will be sent for [same
        origin](https://developer.mozilla.org/en-US/docs/Glossary/Same-origin_policy),
        but cross-origin requests will contain no referrer information.
    -   `strict-origin`: Only send the origin of the document as the
        referrer when the protocol security level stays the same
        (HTTPS→HTTPS), but don\'t send it to a less secure destination
        (HTTPS→HTTP).
    -   `strict-origin-when-cross-origin` (default): Send a full URL
        when performing a same-origin request, only send the origin when
        the protocol security level stays the same (HTTPS→HTTPS), and
        send no header to a less secure destination (HTTPS→HTTP).
    -   `unsafe-url`: The referrer will include the origin *and* the
        path (but not the
        [fragment](https://developer.mozilla.org/en-US/docs/Web/API/HTMLAnchorElement/hash),
        [password](https://developer.mozilla.org/en-US/docs/Web/API/HTMLAnchorElement/password),
        or
        [username](https://developer.mozilla.org/en-US/docs/Web/API/HTMLAnchorElement/username)).
        **This value is unsafe**, because it leaks origins and paths
        from TLS-protected resources to insecure origins.

[`rel`](#rel)

:   The relationship of the linked URL as space-separated link types.

[`target`](#target)

:   Where to display the linked URL, as the name for a *browsing
    context* (a tab, window, or [`<iframe>`](iframe)). The following
    keywords have special meanings for where to load the URL:

    -   `_self`: the current browsing context. (Default)
    -   `_blank`: usually a new tab, but users can configure browsers to
        open a new window instead.
    -   `_parent`: the parent browsing context of the current one. If no
        parent, behaves as `_self`.
    -   `_top`: the topmost browsing context (the \"highest\" context
        that\'s an ancestor of the current one). If no ancestors,
        behaves as `_self`.

    ::: {#sect2 .notecard .note}
    **Note:** Setting `target="_blank"` on `<a>` elements implicitly
    provides the same `rel` behavior as setting
    [`rel="noopener"`](../attributes/rel/noopener) which does not set
    `window.opener`.
    :::

[`type`](#type)

:   Hints at the linked URL\'s format with a [MIME
    type](https://developer.mozilla.org/en-US/docs/Glossary/MIME_type).
    No built-in functionality.
:::

### Deprecated attributes {#deprecated_attributes}

::: section-content

[`charset`](#charset) [Deprecated]{.visually-hidden}

:   Hinted at the [character
    encoding](https://developer.mozilla.org/en-US/docs/Glossary/Character_encoding)
    of the linked URL.

    ::: {#sect3 .notecard .note}
    **Note:** This attribute is deprecated and **should not be used by
    authors**. Use the HTTP
    [`Content-Type`](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Type)
    header on the linked URL.
    :::

[`coords`](#coords) [Deprecated]{.visually-hidden}

:   Used with [the `shape` attribute](#shape). A comma-separated list of
    coordinates.

[`name`](#name) [Deprecated]{.visually-hidden}

:   Was required to define a possible target location in a page. In HTML
    4.01, `id` and `name` could both be used on `<a>`, as long as they
    had identical values.

    ::: {#sect4 .notecard .note}
    **Note:** Use the global attribute [`id`](../global_attributes#id)
    instead.
    :::

[`rev`](#rev) [Deprecated]{.visually-hidden}

:   Specified a reverse link; the opposite of [the `rel`
    attribute](#rel). Deprecated for being very confusing.

[`shape`](#shape) [Deprecated]{.visually-hidden}

:   The shape of the hyperlink\'s region in an image map.

    ::: {#sect5 .notecard .note}
    **Note:** Use the [`<area>`](area) element for image maps instead.
    :::
:::

## Examples

### Linking to an absolute URL {#linking_to_an_absolute_url}

::: section-content
#### HTML

::: code-example
[html]{.language-name}

``` {signature="O9Xh/Og5khrawRE3A+AxB88YjoxeXDlngvDDwEwKepw=" data-language="html"}
<a href="https://www.mozilla.com">Mozilla</a>
```
:::

#### Result

::: {#sect6 .code-example}
::: iframe
:::
:::
:::

### Linking to relative URLs {#linking_to_relative_urls}

::: section-content
#### HTML {#html_2}

::: code-example
[html]{.language-name}

``` {signature="3OeGwYuyTv/zhlj89WwfcJ+iaiEY3V/wlyHK9bKptfA=" data-language="html"}
<a href="//example.com">Scheme-relative URL</a>
<a href="/en-US/docs/Web/HTML">Origin-relative URL</a>
<a href="./p">Directory-relative URL</a>
```
:::

#### Result {#result_2}

::: {#sect7 .code-example}
::: iframe
:::
:::
:::

### Linking to an element on the same page {#linking_to_an_element_on_the_same_page}

::: section-content
::: code-example
[html]{.language-name}

``` {signature="vjFJ6aoTIjsc4xz/hxRNBu11gJXv8X1tQXAVPfPp1Po=" data-language="html"}
<!-- <a> element links to the section below -->
<p><a href="#Section_further_down">Jump to the heading below</a></p>

<!-- Heading to link to -->
<h2 id="Section_further_down">Section further down</h2>
```
:::

#### Result {#result_3}

::: {#sect8 .code-example}
::: iframe
:::
:::

::: {#sect9 .notecard .note}
**Note:** You can use `href="#top"` or the empty fragment (`href="#"`)
to link to the top of the current page, [as defined in the HTML
specification](https://html.spec.whatwg.org/multipage/browsing-the-web.html#scroll-to-the-fragment-identifier){target="_blank"}.
:::
:::

### Linking to an email address {#linking_to_an_email_address}

::: section-content
To create links that open in the user\'s email program to let them send
a new message, use the `mailto:` scheme:

::: code-example
[html]{.language-name}

``` {signature="Jb6UJm3VQOXjlsLsQlMeor/X7uynoJTFyLd/jZEdjg0=" data-language="html"}
<a href="mailto:nowhere@mozilla.org">Send email to nowhere</a>
```
:::

#### Result {#result_4}

::: {#sect10 .code-example}
::: iframe
:::
:::

For details about `mailto:` URLs, such as including a subject or body,
see [Email
links](https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/Creating_hyperlinks#email_links)
or [RFC
6068](https://datatracker.ietf.org/doc/html/rfc6068){target="_blank"}.
:::

### Linking to telephone numbers {#linking_to_telephone_numbers}

::: section-content
::: code-example
[html]{.language-name}

``` {signature="YeLw9jGA9vg6UYcXkF+BCK9vyMn14M/w7YB18h+ZpeM=" data-language="html"}
<a href="tel:+49.157.0156">+49 157 0156</a>
<a href="tel:+1(800)555-0123">(800) 555-0123</a>
```
:::

#### Result {#result_5}

::: {#sect11 .code-example}
::: iframe
:::
:::

`tel:` link behavior varies with device capabilities:

-   Cellular devices autodial the number.
-   Most operating systems have programs that can make calls, like Skype
    or FaceTime.
-   Websites can make phone calls with
    [`registerProtocolHandler`](https://developer.mozilla.org/en-US/docs/Web/API/Navigator/registerProtocolHandler),
    such as `web.skype.com`.
-   Other behaviors include saving the number to contacts, or sending
    the number to another device.

See [RFC
3966](https://datatracker.ietf.org/doc/html/rfc3966){target="_blank"}
for syntax, additional features, and other details about the `tel:` URL
scheme.
:::

### Using the download attribute to save a \<canvas\> as a PNG {#using_the_download_attribute_to_save_a_canvas_as_a_png}

::: section-content
To save a [`<canvas>`](canvas) element\'s contents as an image, you can
create a link where the `href` is the canvas data as a `data:` URL
created with JavaScript and the `download` attribute provides the file
name for the downloaded PNG file:

#### Example painting app with save link {#example_painting_app_with_save_link}

##### HTML {#html_3}

::: code-example
[html]{.language-name}

``` {signature="ye0L2ExfMb3ZSsS3Y0Yrn6IGMWWc4DAq2ZjTwnJVyNo=" data-language="html"}
<p>
  Paint by holding down the mouse button and moving it.
  <a href="" download="my_painting.png">Download my painting</a>
</p>

<canvas width="300" height="300"></canvas>
```
:::

##### CSS

::: code-example
[css]{.language-name}

``` {signature="WWvZzlFHKimd1W7wsW+bc4hqRbQxnQZk+02xMwVYt+8=" data-language="css"}
html {
  font-family: sans-serif;
}
canvas {
  background: #fff;
  border: 1px dashed;
}
a {
  display: inline-block;
  background: #69c;
  color: #fff;
  padding: 5px 10px;
}
```
:::

##### JavaScript

::: code-example
[js]{.language-name}

``` {signature="qGGr/ZrMV4ggc0OtYRenghLaTrw2TGY8wUZ2+6CfU0o=" data-language="js"}
const canvas = document.querySelector("canvas");
const c = canvas.getContext("2d");
c.fillStyle = "hotpink";
let isDrawing;

function draw(x, y) {
  if (isDrawing) {
    c.beginPath();
    c.arc(x, y, 10, 0, Math.PI * 2);
    c.closePath();
    c.fill();
  }
}

canvas.addEventListener("mousemove", (event) =>
  draw(event.offsetX, event.offsetY),
);
canvas.addEventListener("mousedown", () => (isDrawing = true));
canvas.addEventListener("mouseup", () => (isDrawing = false));

document
  .querySelector("a")
  .addEventListener(
    "click",
    (event) => (event.target.href = canvas.toDataURL()),
  );
```
:::

##### Result {#result_6}

::: {#sect12 .code-example}
::: iframe
:::
:::
:::

## Security and privacy {#security_and_privacy}

::: section-content
`<a>` elements can have consequences for users\' security and privacy.
See [`Referer` header: privacy and security
concerns](https://developer.mozilla.org/en-US/docs/Web/Security/Referer_header:_privacy_and_security_concerns)
for information.

Using `target="_blank"` without
[`rel="noreferrer"`](../attributes/rel/noreferrer) and
[`rel="noopener"`](../attributes/rel/noopener) makes the website
vulnerable to
[`window.opener`](https://developer.mozilla.org/en-US/docs/Web/API/Window/opener)
API exploitation attacks, although note that, in newer browser versions
setting `target="_blank"` implicitly provides the same protection as
setting `rel="noopener"`. See [browser
compatibility](#browser_compatibility) for details.
:::

## Accessibility

### Strong link text {#strong_link_text}

::: section-content
**The content inside a link should indicate where the link goes**, even
out of context.

#### Inaccessible, weak link text {#inaccessible_weak_link_text}

A sadly common mistake is to only link the words \"click here\" or
\"here\":

::: code-example
[html]{.language-name}

``` {signature="PHRPy4Os+xCmHs++LjAUqXt0evtsOO9gsK7cLZOUzA4=" data-language="html"}
<p>Learn more about our products <a href="/products">here</a>.</p>
```
:::

##### Result {#result_7}

::: {#sect13 .code-example}
::: iframe
:::
:::

#### Strong link text {#strong_link_text_2}

Luckily, this is an easy fix, and it\'s actually shorter than the
inaccessible version!

::: code-example
[html]{.language-name}

``` {signature="+Tc5lxAd7W/DPkjpCyQjqGS4WC9YXWwfOqyPVk9WZKk=" data-language="html"}
<p>Learn more <a href="/products">about our products</a>.</p>
```
:::

##### Result {#result_8}

::: {#sect14 .code-example}
::: iframe
:::
:::

Assistive software has shortcuts to list all links on a page. However,
strong link text benefits all users --- the \"list all links\" shortcut
emulates how sighted users quickly scan pages.
:::

### onclick events {#onclick_events}

::: section-content
Anchor elements are often abused as fake buttons by setting their `href`
to `#` or `javascript:void(0)` to prevent the page from refreshing, then
listening for their `click` events .

These bogus `href` values cause unexpected behavior when
copying/dragging links, opening links in a new tab/window, bookmarking,
or when JavaScript is loading, errors, or is disabled. They also convey
incorrect semantics to assistive technologies, like screen readers.

Use a [`<button>`](button) instead. In general, **you should only use a
hyperlink for navigation to a real URL**.
:::

### External links and linking to non-HTML resources {#external_links_and_linking_to_non-html_resources}

::: section-content
Links that open in a new tab/window via `target="_blank"`, or links that
point to a download file should indicate what will happen when the link
is followed.

People experiencing low vision conditions, navigating with the aid of
screen reading technology, or with cognitive concerns may be confused
when a new tab, window, or application opens unexpectedly. Older
screen-reading software may not even announce the behavior.

#### Link that opens a new tab/window {#link_that_opens_a_new_tabwindow}

::: code-example
[html]{.language-name}

``` {signature="G0kd4SKtECA0PLD2iWeWwI7LzlNjuCloPCk5xglhppY=" data-language="html"}
<a target="_blank" href="https://www.wikipedia.org">
  Wikipedia (opens in new tab)
</a>
```
:::

##### Result {#result_9}

::: {#sect15 .code-example}
::: iframe
:::
:::

#### Link to a non-HTML resource {#link_to_a_non-html_resource}

::: code-example
[html]{.language-name}

``` {signature="kAJN9/uxrfFR0zROlEu2QGNIZeSlnVVyW7+K+pY04/I=" data-language="html"}
<a href="2017-annual-report.ppt">2017 Annual Report (PowerPoint)</a>
```
:::

If an icon is used to signify link behavior, make sure it has an [*alt
text*](img#alt):

::: code-example
[html]{.language-name}

``` {signature="KKZ8Fu0KKyYqIaSDzMoSmS9f++1zCQ8+hsZhwDlWy9U=" data-language="html"}
<a target="_blank" href="https://www.wikipedia.org">
  Wikipedia
  <img alt="(opens in new tab)" src="newtab.svg" />
</a>

<a href="2017-annual-report.ppt">
  2017 Annual Report
  <img alt="(PowerPoint file)" src="ppt-icon.svg" />
</a>
```
:::

##### Result {#result_10}

::: {#sect16 .code-example}
::: iframe
:::
:::

-   [WebAIM: Links and Hypertext - Hypertext
    Links](https://webaim.org/techniques/hypertext/hypertext_links){target="_blank"}
-   [MDN / Understanding WCAG, Guideline
    3.2](https://developer.mozilla.org/en-US/docs/Web/Accessibility/Understanding_WCAG/Understandable#guideline_3.2_%E2%80%94_predictable_make_web_pages_appear_and_operate_in_predictable_ways)
-   [G200: Opening new windows and tabs from a link only when
    necessary](https://www.w3.org/TR/WCAG20-TECHS/G200.html){target="_blank"}
-   [G201: Giving users advanced warning when opening a new
    window](https://www.w3.org/TR/WCAG20-TECHS/G201.html){target="_blank"}
:::

### Skip links {#skip_links}

::: section-content
A **skip link** is a link placed as early as possible in
[`<body>`](body) content that points to the beginning of the page\'s
main content. Usually, CSS hides a skip link offscreen until focused.

::: code-example
[html]{.language-name}

``` {signature="uCcEPMWQrwx4WUkNH7CcO5SRVXuFI2PJJYClxIWSaZc=" data-language="html"}
<body>
  <a href="#content" class="skip-link">Skip to main content</a>

  <header>…</header>

  <!-- The skip link jumps to here -->
  <main id="content"></main>
</body>
```
:::

::: code-example
[css]{.language-name}

``` {signature="sjFzqzI63Wkszs87H75n6HCdBZSKnnSjJ4gNU1OSYHE=" data-language="css"}
.skip-link {
  position: absolute;
  top: -3em;
  background: #fff;
}
.skip-link:focus {
  top: 0;
}
```
:::

#### Result {#result_11}

::: {#sect17 .code-example}
::: iframe
:::
:::

Skip links let keyboard users bypass content repeated throughout
multiple pages, such as header navigation.

Skip links are especially useful for people who navigate with the aid of
assistive technology such as switch control, voice command, or mouth
sticks/head wands, where the act of moving through repetitive links can
be laborious.

-   [WebAIM: \"Skip Navigation\"
    Links](https://webaim.org/techniques/skipnav/){target="_blank"}
-   [How-to: Use Skip Navigation
    links](https://www.a11yproject.com/posts/skip-nav-links/){target="_blank"}
-   [MDN / Understanding WCAG, Guideline 2.4
    explanations](https://developer.mozilla.org/en-US/docs/Web/Accessibility/Understanding_WCAG/Operable#guideline_2.4_%e2%80%94_navigable_provide_ways_to_help_users_navigate_find_content_and_determine_where_they_are)
-   [Understanding Success Criterion
    2.4.1](https://www.w3.org/TR/UNDERSTANDING-WCAG20/navigation-mechanisms-skip.html){target="_blank"}
:::

### Size and proximity {#size_and_proximity}

::: section-content
#### Size

Interactive elements, like links, should provide an area large enough
that it is easy to activate them. This helps a variety of people,
including those with motor control issues and those using imprecise
inputs such as a touchscreen. A minimum size of 44×44 [CSS
pixels](https://www.w3.org/TR/WCAG21/#dfn-css-pixels){target="_blank"}
is recommended.

Text-only links in prose content are exempt from this requirement, but
it\'s still a good idea to make sure enough text is hyperlinked to be
easily activated.

-   [Understanding Success Criterion 2.5.5: Target
    Size](https://www.w3.org/WAI/WCAG21/Understanding/target-size.html){target="_blank"}
-   [Target Size and
    2.5.5](https://adrianroselli.com/2019/06/target-size-and-2-5-5.html){target="_blank"}
-   [Quick test: Large touch
    targets](https://www.a11yproject.com/posts/large-touch-targets/){target="_blank"}

#### Proximity

Interactive elements, like links, placed in close visual proximity
should have space separating them. Spacing helps people with motor
control issues, who may otherwise accidentally activate the wrong
interactive content.

Spacing may be created using CSS properties like
[`margin`](https://developer.mozilla.org/en-US/docs/Web/CSS/margin).

-   [Hand tremors and the
    giant-button-problem](https://axesslab.com/hand-tremors/){target="_blank"}
:::

## Technical summary {#technical_summary}

::: section-content
<figure class="table-container">
<div class="_table">
<table class="properties">
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<th scope="row"><a href="../content_categories">Content
categories</a></th>
<td><a href="../content_categories#flow_content">Flow content</a>, <a
href="../content_categories#phrasing_content">phrasing content</a>, <a
href="../content_categories#interactive_content">interactive
content</a>, palpable content.</td>
</tr>
<tr class="even">
<th scope="row">Permitted content</th>
<td><a
href="../content_categories#transparent_content_model">Transparent</a>,
except that no descendant may be <a
href="../content_categories#interactive_content">interactive content</a>
or an <a href="a" aria-current="page">a</a> element, and no descendant
may have a specified <a
href="../global_attributes/tabindex">tabindex</a> attribute.</td>
</tr>
<tr class="odd">
<th scope="row">Tag omission</th>
<td>None, both the starting and ending tag are mandatory.</td>
</tr>
<tr class="even">
<th scope="row">Permitted parents</th>
<td>Any element that accepts <a
href="../content_categories#phrasing_content">phrasing content</a>, or
any element that accepts <a
href="../content_categories#flow_content">flow content</a>, but not
other <code>&lt;a&gt;</code> elements.</td>
</tr>
<tr class="odd">
<th scope="row">Implicit ARIA role</th>
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/link_role"><code>link</code></a>
when <code>href</code> attribute is present, otherwise <a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/generic_role"><code>generic</code></a></td>
</tr>
<tr class="even">
<th scope="row">Permitted ARIA roles</th>
<td><p>When <code>href</code> attribute is present:</p>
<ul>
<li><a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/button_role"><code>button</code></a></li>
<li><a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/checkbox_role"><code>checkbox</code></a></li>
<li><a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/menuitem_role"><code>menuitem</code></a></li>
<li><a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/menuitemcheckbox_role"><code>menuitemcheckbox</code></a></li>
<li><a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/menuitemradio_role"><code>menuitemradio</code></a></li>
<li><a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/option_role"><code>option</code></a></li>
<li><a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/radio_role"><code>radio</code></a></li>
<li><a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/switch_role"><code>switch</code></a></li>
<li><a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/tab_role"><code>tab</code></a></li>
<li><a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/treeitem_role"><code>treeitem</code></a></li>
</ul>
<p>When <code>href</code> attribute is not present:</p>
<ul>
<li>any</li>
</ul></td>
</tr>
<tr class="odd">
<th scope="row">DOM interface</th>
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLAnchorElement"><code>HTMLAnchorElement</code></a></td>
</tr>
</tbody>
</table>

</figure>
:::

## Specifications

::: _table
  ---------------------------------------------------------------------------------------------------------
  Specification
  ---------------------------------------------------------------------------------------------------------
  [HTML Standard\
  [\#
  the-a-element]{.small}](https://html.spec.whatwg.org/multipage/text-level-semantics.html#the-a-element)

  ---------------------------------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
  ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
                        Desktop                                                                                                                                                                             Mobile                                                                                        
  --------------------- -------------- ----------------------------------------------------------------------------------------- --------------------------------------- ---------- -------------- -------- -------------- -------------- --------------------------------------- -------------- -------- --------------
                        Chrome         Edge                                                                                      Firefox                                 Internet   Opera          Safari   WebView        Chrome Android Firefox for Android                     Opera Android  Safari   Samsung
                                                                                                                                                                         Explorer                           Android                                                                              on IOS   Internet

  `a`                   1              12                                                                                        1                                       Yes        15             1        4.4            18             4                                       14             1        1.0
                                                                                                                                                                                                                                                                                                          
                                                                                                                                 Starting with Firefox 41, \<a\> without                                                                  Starting with Firefox 41, \<a\> without                         
                                                                                                                                 `href` attribute is no longer                                                                            `href` attribute is no longer                                   
                                                                                                                                 classified as interactive content:                                                                       classified as interactive content:                              
                                                                                                                                 clicking it inside \<label\> will                                                                        clicking it inside \<label\> will                               
                                                                                                                                 activate labelled content ([bug                                                                          activate labelled content ([bug                                 
                                                                                                                                 1167816](https://bugzil.la/1167816)).                                                                    1167816](https://bugzil.la/1167816)).                           

  `attributionsrc`      117            117                                                                                       No                                      No         103            No       117            117            No                                      No             No       No

  `charset`             1              12                                                                                        1                                       Yes        15             1        4.4            18             4                                       14             1        1.0

  `coords`              No             No                                                                                        1--58                                   No         No             1        No             No             4--58                                   No             1        No
                                                                                                                                                                                                                                                                                                          
                                                                                                                                 You can no longer nest an `<a>` element                                                                  You can no longer nest an `<a>` element                         
                                                                                                                                 inside a `<map>` element to create a                                                                     inside a `<map>` element to create a                            
                                                                                                                                 hotspot region - `coords` and `shape`                                                                    hotspot region - `coords` and `shape`                           
                                                                                                                                 attribute support removed.                                                                               attribute support removed.                                      

  `download`            14             18                                                                                        20                                      No         15             10.1     4.4            18             20                                      14             13       1.0
                                                                                                                                                                                                                                                                                                          
                        Starting in    Starting in Edge 79, cross-origin downloads are not supported on the `<a>` element.                                                          Starting in             Starting in    Starting in                                            Starting in             Starting in
                        Chrome 65,                                                                                                                                                  Opera 52,               Chrome 65,     Chrome 65,                                             Opera 47,               Samsung
                        cross-origin   13                                                                                                                                           cross-origin            cross-origin   cross-origin                                           cross-origin            Internet 9.0,
                        downloads are                                                                                                                                               downloads are           downloads are  downloads are                                          downloads are           cross-origin
                        not supported  \[\"Until Edge 14 (build 14357), attempting to download data URIs caused Edge to crash                                                       not supported           not supported  not supported                                          not supported           downloads are
                        on the `<a>`   ([bug                                                                                                                                        on the `<a>`            on the `<a>`   on the `<a>`                                           on the `<a>`            not supported
                        element.       7160092](https://developer.microsoft.com/microsoft-edge/platform/issues/7160092/)).\",                                                       element.                element.       element.                                               element.                on the `<a>`
                                       \"Edge 17 or older didn\'t follow the attributes\' value to determine filename ([bug                                                                                                                                                                               element.
                                       7260192](https://developer.microsoft.com/microsoft-edge/platform/issues/7260192/)).\"\]                                                                                                                                                                            

  `href`                1              12                                                                                        1                                       Yes        15             1        4.4            18             4                                       14             1        1.0

  `href_sms`            No             No                                                                                        12                                      No         No             No       No             No             14                                      No             No       No

  `hreflang`            1              12                                                                                        1                                       Yes        15             1        4.4            18             4                                       14             1        1.0

  `implicit_noopener`   88             88                                                                                        79                                      No         74             12.1     No             88             79                                      Yes            12.2     15.0

  `name`                1              12                                                                                        1                                       Yes        15             1        4.4            18             4                                       14             1        1.0

  `ping`                12             17                                                                                        1                                       No         15             6        ≤37            18             No                                      14             6        1.0

  `referrerpolicy`      51             79                                                                                        50                                      No         38             14       51             51             50                                      41             14       7.2

  `rel`                 1              12                                                                                        1                                       Yes        15             1        4.4            18             4                                       14             1        1.0

  `rev`                 1              12                                                                                        1                                       Yes        15             1        4.4            18             4                                       14             1        1.0

  `shape`               No             No                                                                                        1--58                                   No         No             1        No             No             4--58                                   No             1        No
                                                                                                                                                                                                                                                                                                          
                                                                                                                                 You can no longer nest an `<a>` element                                                                  You can no longer nest an `<a>` element                         
                                                                                                                                 inside a `<map>` element to create a                                                                     inside a `<map>` element to create a                            
                                                                                                                                 hotspot region - `coords` and `shape`                                                                    hotspot region - `coords` and `shape`                           
                                                                                                                                 attribute support removed.                                                                               attribute support removed.                                      

  `target`              1              12                                                                                        1                                       Yes        15             1        4.4            18             4                                       14             1        1.0

  `text_fragments`      80             80                                                                                        No                                      No         67             16.1     80             80             No                                      57             16.1     13.0

  `type`                1              12                                                                                        1                                       Yes        15             1        4.4            18             4                                       14             1        1.0
  ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
:::

## See also {#see_also}

::: section-content
-   [`<link>`](link) is similar to `<a>`, but for metadata hyperlinks
    that are invisible to users.
-   [`:link`](https://developer.mozilla.org/en-US/docs/Web/CSS/:link) is
    a CSS pseudo-class that will match `<a>` elements with URL in `href`
    attribute that was not yet visited by the user.
-   [`:visited`](https://developer.mozilla.org/en-US/docs/Web/CSS/:visited)
    is a CSS pseudo-class that will match `<a>` elements with URL in
    `href` attribute that was visited by the user in the past.
-   [`:any-link`](https://developer.mozilla.org/en-US/docs/Web/CSS/:any-link)
    is a CSS pseudo-class that will match `<a>` elements with `href`
    attribute.
-   [Text
    fragments](https://developer.mozilla.org/en-US/docs/Web/Text_fragments)
    are user-agent instructions added to URLs that allow content authors
    to link to specific text on a page, without IDs being required.
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Element/a](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/a){._attribution-link}
:::
